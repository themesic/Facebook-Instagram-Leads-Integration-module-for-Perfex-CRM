# ❓ FAQ

Quick answers to the most common questions! 💬

***

## 💰 Costs & Licensing

### How much does the module cost?

The module is a **one-time purchase** on CodeCanyon. Check the [product page](https://codecanyon.net/item/facebook-leads-integration-sync-module-for-perfex-crm/25623248) for current pricing. No monthly fees, no per-lead charges.

### Is the Meta App free?

**Yes!** Creating a Meta App is completely free. You don't pay Meta/Facebook anything for the app itself.

### Do I need to pay for Lead Ads?

**Yes.** Lead Ads are a form of Facebook/Instagram advertising. You set your own budget (can be as low as $1/day). The module itself doesn't cost anything extra per lead.

### Does the license cover multiple CRM installations?

Each purchase code is valid for **one** Perfex CRM installation. For multiple installations, you need separate licenses.

***

## 🔧 Setup & Configuration

### Do I need to be a developer?

**Absolutely not!** 😊 If you can follow a step-by-step guide (which you're reading right now), you can set this up. No coding knowledge required.

### Do I need Facebook App Review?

**No!** Since you're creating your own app to access your own Page's data, you can keep the app in **Development Mode**. See [App Review & Permissions](../facebook-app-setup/app-review.md) for details.

### Do I need to switch my app to "Live" mode?

**No.** Development Mode works perfectly for accessing your own Pages. See [App Review & Permissions](../facebook-app-setup/app-review.md).

### Can I use one Meta App for multiple Pages?

**Yes!** One Meta App can monitor multiple Pages. Just subscribe to each Page in the module settings.

### Do I need a separate setup for Instagram?

**No!** Instagram Lead Ads use the same webhook and setup as Facebook. See [Instagram Lead Ads](../lead-ads/instagram-lead-ads.md).

### Does the module work with Perfex CRM hosted on a subdomain?

**Yes**, as long as the subdomain has an SSL certificate (HTTPS).

### Does the module work with Perfex CRM behind a reverse proxy?

**Yes**, as long as the webhook URL is publicly accessible and reachable by Facebook's servers.

***

## 📱 Lead Ads

### What are Lead Ads?

Special Facebook/Instagram ads with built-in forms. Users submit their info without leaving the platform. See [What Are Lead Ads?](../lead-ads/what-are-lead-ads.md)

### Do Lead Ads work with Instagram?

**Yes!** Both Facebook and Instagram Lead Ads are supported. See [Instagram Lead Ads](../lead-ads/instagram-lead-ads.md).

### Can I use Lead Ads without a website?

**Yes!** The Lead Form is built into Facebook/Instagram. However, you do need:
- A Perfex CRM installation (with HTTPS) for the webhook
- A Privacy Policy URL for the Lead Form

### How fast do leads arrive in my CRM?

**Within seconds!** ⚡ The typical delay is 1-5 seconds from form submission to lead appearing in Perfex CRM.

### Can I test without spending money on ads?

**Yes!** Use the [Facebook Lead Ads Testing Tool](https://developers.facebook.com/tools/lead-ads-testing/) or the module's built-in "Send Test Lead" button. See [Testing Leads](../lead-ads/testing-leads.md).

### What happens if a lead fails to sync?

The module automatically adds it to a **retry queue** and tries again later. You can also manually process the retry queue from the Sync History page.

### Can I control which leads go to which staff member?

**Yes!** 🎯 The module supports **per-page lead assignment**:

1. Set a **Default Assigned Staff** in the module settings (this is the global fallback)
2. In the **Connected Pages** table, each page has its own **"Assign Leads To"** dropdown
3. Select a different staff member for each page — leads from that page will go directly to them!

**Example:** Leads from your "Restaurant Page" go to Alice, leads from your "Real Estate Page" go to Bob. See [Settings Page → Per-Page Lead Assignment](../module-configuration/settings.md#-per-page-lead-assignment) for details.

***

## 🔀 Field Mapping

### Do I need to configure field mapping?

**Not for standard fields!** Common fields like name, email, phone, company, city, etc. are auto-mapped. You only need custom mapping for custom questions in your Lead Form. See [Field Mapping](../module-configuration/field-mapping.md).

### What happens to unmapped fields?

Unmapped fields are stored in the lead's **Description** field, so you never lose data.

### Can I map to Perfex CRM custom fields?

**Yes!** Any custom fields you create for Leads in Perfex CRM will appear in the Field Mapping dropdown.

***

## 🔒 Security

### Is my data secure?

**Yes!** The module uses:
- 🔒 Server-side token exchange (App Secret never exposed in JavaScript)
- 🔒 Webhook signature verification (X-Hub-Signature-256)
- 🔒 CSRF protection on all endpoints
- 🔒 Input validation and sanitization
- 🔒 HTTPS required for all communication

### Is the App Secret visible to users?

**No.** The App Secret is stored in your database and only used server-side. It's never exposed in the HTML or JavaScript.

### Can Facebook access my CRM data?

**No.** Facebook can only **send** data to your webhook. It cannot read, modify, or access any data in your CRM.

***

## 🔄 Updates & Compatibility

### How do I update the module?

1. Download the latest version from CodeCanyon
2. Deactivate the current module in Perfex CRM
3. Upload the new version
4. Activate again
5. Database migrations run automatically

### Will updating lose my settings?

**No!** All settings, field mappings, and sync history are preserved during updates.

### Is the module compatible with Perfex CRM 3.x?

**Yes!** The module supports Perfex CRM v2.3.0 and above, including the latest 3.x versions.

### What Facebook Graph API version does the module use?

The module uses **Graph API v19.0** (latest stable at time of release).

***

## 🏢 Multiple Sites & Reselling

### Can I use this on my clients' CRMs?

Each installation requires its own license (purchase code). You can purchase additional licenses for your clients.

### Can I modify the module?

The module comes with unencrypted source code. You're welcome to modify it for your own use, but redistribution is not permitted per CodeCanyon's license terms.

***

## 💬 Still Have Questions?

- 📧 Email: [support@themesic.com](mailto:support@themesic.com)
- 🌐 Website: [themesic.com/support](https://themesic.com/support)
- 📖 Full docs: You're reading them! 😄

***

**Check the changelog 👉** [**Changelog**](changelog.md)
