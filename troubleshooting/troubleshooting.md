# 🔍 Troubleshooting

Running into issues? Don't worry — most problems have simple fixes! Find your issue below and follow the solution. 🛠️

***

## 🔗 Webhook Verification Fails

**Error:** *"The callback URL or verify token couldn't be validated."*

### Possible Causes & Fixes:

| # | Cause | Fix |
| --- | --- | --- |
| 1️⃣ | URL is not HTTPS | Install an SSL certificate on your server |
| 2️⃣ | Typo in callback URL | Copy-paste directly from the module settings |
| 3️⃣ | Typo in verify token | Copy-paste directly from the module settings |
| 4️⃣ | Server is blocking requests | Check your firewall / security plugins |
| 5️⃣ | .htaccess redirect issues | Make sure the URL doesn't redirect (no www ↔ non-www redirect issues) |
| 6️⃣ | Selected "User" instead of "Page" | Change the dropdown to "Page" in Facebook webhooks |

### How to Debug:

1. Open your browser and visit your webhook URL directly:
   ```
   https://yourcrm.com/facebookleadsintegration/webhook?hub.mode=subscribe&hub.verify_token=YOUR_TOKEN&hub.challenge=test123
   ```
2. If working correctly, you should see `test123` displayed on the page
3. If you see an error page, the issue is on your server side

> 💡 **Still not working?** Check your server's error logs at `/path/to/your/crm/application/logs/`

***

## 🔑 "Invalid Scopes" Error During Facebook Login

**Error:** *"Invalid Scopes: pages_manage_metadata"*

### Fix:

This means the module is requesting a deprecated permission. Make sure you're using the **latest version** of the module (v2.0.0+), which uses the correct permissions:

- `pages_show_list`
- `pages_read_engagement`
- `leads_retrieval`
- `pages_manage_ads`
- `ads_management`

**Update your module** to the latest version to fix this.

***

## 🚫 "Error Accessing App" / "App Not Active"

**Error:** When trying to connect with Facebook, you see *"Error Accessing App"* or *"The app is not active."*

### Possible Causes & Fixes:

| # | Cause | Fix |
| --- | --- | --- |
| 1️⃣ | Wrong App ID in module settings | Double-check the App ID matches your Meta App |
| 2️⃣ | App was deleted or disabled | Check your app at [developers.facebook.com/apps](https://developers.facebook.com/apps) |
| 3️⃣ | You're not an admin/developer of the app | Add yourself in App Roles → Roles |
| 4️⃣ | App restrictions | Check App Settings → Basic → App Restrictions |

***

## 📨 Test Lead Works but Real Leads Don't Arrive

The module's "Send Test Lead" button works, but real leads from Facebook don't appear.

### Check These:

| # | Check | How |
| --- | --- | --- |
| 1️⃣ | Is your Page subscribed? | Settings → Connected Pages → Must show "Monitoring" 🟢 |
| 2️⃣ | Is the webhook verified? | Settings → Connection Status → Webhook must be green 🟢 |
| 3️⃣ | Is "leadgen" subscribed? | Meta App → Webhooks → Page → "leadgen" must be checked ✅ |
| 4️⃣ | Is the ad using the right Page? | Ads Manager → Ad Set → Make sure it uses the subscribed Page |
| 5️⃣ | Is the ad running? | Ads Manager → Campaign status should be "Active" |

### Test with Facebook's Tool:

Use the [Lead Ads Testing Tool](https://developers.facebook.com/tools/lead-ads-testing/) to send a real webhook test lead. If this works but actual ads don't, the issue is likely with your ad campaign setup.

***

## 🔴 500 Error on Module Pages

**Symptom:** Module pages show a blank page or "500 Internal Server Error"

### Fixes:

1. **Check PHP error logs:**
   ```
   /path/to/your/crm/application/logs/log-YYYY-MM-DD.php
   ```

2. **Common causes:**
   - PHP version too old (need 7.4+)
   - Missing PHP extensions (cURL, JSON)
   - File permissions incorrect
   - Module files corrupted during upload

3. **Fix file permissions:**
   ```bash
   find /path/to/modules/facebookleadsintegration -type f -exec chmod 644 {} \;
   find /path/to/modules/facebookleadsintegration -type d -exec chmod 755 {} \;
   ```

4. **Re-upload the module** if files might be corrupted

***

## 📋 Copy Button Not Working

**Symptom:** Clicking the "Copy" button next to webhook URL or verify token does nothing.

### Fix:

- Make sure your CRM is accessed via **HTTPS** — clipboard API requires a secure context
- Try manually selecting the text and pressing **Ctrl+C**
- Check browser console for JavaScript errors (F12 → Console tab)

***

## 🔄 Leads Are Stuck in "Pending Retry"

**Symptom:** Sync History shows leads with "Pending" status that aren't being processed.

### Fixes:

1. **Process manually:** Go to Sync History → Click **"Process Retry Queue"**
2. **Check cron:** The retry queue processes automatically via Perfex CRM's cron job
   - Make sure your cron job is running: **Setup** → **Settings** → **Cron Job**
   - The cron URL should be called every 5 minutes
3. **Check the error message** in Sync History for why the lead failed initially

***

## 🔑 Access Token Expired

**Symptom:** Connection test fails with "Token expired" or leads stop arriving.

### Fix:

The module exchanges short-lived tokens for **long-lived tokens** (valid for ~60 days). To refresh:

1. Go to **Meta Leads** → **Settings**
2. Scroll to **Connected Pages**
3. Click **"Connect with Facebook"** again
4. Log in and grant permissions
5. The token is automatically refreshed ✅

> 💡 **Set a reminder** to reconnect every 50 days to keep the token fresh!

***

## 📝 Fields Not Mapping Correctly

**Symptom:** Lead data appears in the wrong fields or is missing.

### Debug Steps:

1. Go to **Sync History** → Click on a lead entry to see the raw data
2. Check what **field names** Facebook is sending
3. Go to **Field Mapping** → Make sure the Facebook field name matches
4. Remember: Standard fields (email, full_name, phone_number) map automatically

### Common Field Name Issues:

| What You Expect | What Facebook Sends | Solution |
| --- | --- | --- |
| `name` | `full_name` | Already auto-mapped ✅ |
| `phone` | `phone_number` | Already auto-mapped ✅ |
| `company` | `company_name` | Already auto-mapped ✅ |
| `budget` | `custom_question_1` | Create a custom mapping |

***

## 🔧 Module Doesn't Appear After Installation

### Fixes:

1. **Check file location:** Module folder must be at `modules/facebookleadsintegration/`
2. **Check file name:** Main file must be `facebookleadsintegration.php` (all lowercase)
3. **Activate the module:** Go to **Setup** → **Modules** → Click **Activate**
4. **Check permissions:** Files should be readable by the web server (644 for files, 755 for directories)

***

## 🌐 Server-Specific Issues

### Cloudflare Users

If using Cloudflare, whitelist Facebook's webhook IPs:

1. Go to Cloudflare → **WAF** (Web Application Firewall)
2. Create a rule to **Allow** requests from Facebook
3. Or add these to your firewall whitelist:
   - Facebook's webhook IPs can be found at: `https://developers.facebook.com/docs/sharing/webmasters/getting-started/webhooks/`

### Nginx Users

Make sure your Nginx config allows POST requests to the webhook URL and doesn't block Facebook's User-Agent.

### Shared Hosting

Most shared hosting works fine. If you have issues:
- Check if `allow_url_fopen` is enabled in PHP
- Check if `cURL` extension is installed
- Check if your host blocks incoming webhooks (some security-focused hosts do)

***

## 📧 Still Need Help?

If none of the above fixes your issue:

1. 📋 Check the Perfex CRM error logs
2. 📋 Check the module's Sync History for error messages
3. 📋 Take a screenshot of any error messages
4. 📧 Contact us at [support@themesic.com](mailto:support@themesic.com) with:
   - Your Perfex CRM version
   - PHP version
   - The error message
   - Steps to reproduce the issue

***

**Check the FAQ for more answers 👉** [**FAQ**](faq.md)
