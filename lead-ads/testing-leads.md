# 🧪 Testing Leads

Before going live, let's make sure everything works perfectly! Here are multiple ways to test. 🔬

***

## Method 1: Module's Built-In Test Lead (Easiest! ⭐)

The fastest way to test the complete flow:

1. Go to **Meta Leads** → **Settings**
2. Click **"Send Test Lead"** button 📨
3. A test lead will be created in Perfex CRM
4. You'll be asked: *"Test lead created! Would you like to view it?"*
5. Click **Yes** to see the lead 🎉

### What This Tests:

- ✅ Module is working
- ✅ Lead creation in Perfex CRM
- ✅ Default assignment, source, and status
- ✅ Field mapping for standard fields

### What This Doesn't Test:

- ❌ Facebook webhook delivery
- ❌ Facebook → your server connection
- ❌ Real Facebook form field names

> 💡 Use this for a **quick sanity check**, then move to Method 2 for a full test.

***

## Method 2: Facebook Lead Ads Testing Tool (Recommended! ⭐⭐)

This is the **best way** to test the complete flow — from Facebook all the way to your CRM, without spending any money on ads.

### Step-by-Step:

1. Go to: 👉 [**https://developers.facebook.com/tools/lead-ads-testing/**](https://developers.facebook.com/tools/lead-ads-testing/)

2. **Select your Page** from the dropdown
   - Choose the Page you subscribed in the module

3. **Select a Form** (or create a test form)
   - If you haven't created a Lead Form yet, you'll need to create one first in [Ads Manager](https://business.facebook.com/adsmanager)
   - Or just create a quick test form (see below)

4. Click **"Create Lead"** 🧪

5. **Within seconds**, check your Perfex CRM:
   - Go to **Leads** — you should see a new lead! 🎉
   - Go to **Meta Leads** → **Sync History** — you'll see the sync entry

### What This Tests:

- ✅ **Everything!** The complete real-world flow
- ✅ Facebook sends real webhook data
- ✅ Your server receives and processes it
- ✅ Lead is created in Perfex CRM
- ✅ Field mapping works with real Facebook field names

> 🎯 **This is the definitive test.** If this works, real Lead Ads will work too.

***

## Method 3: Test Connection Button

Tests your credentials and permissions (but not lead delivery):

1. Go to **Meta Leads** → **Settings**
2. Click **"Test Connection"** 🔍
3. You should see:

```
✅ App Credentials: Valid
   App ID is configured and accessible

✅ Access Token: Valid  
   Token is valid and has access to your pages

✅ Permissions: All required permissions granted
   pages_show_list, pages_read_engagement, leads_retrieval, 
   pages_manage_ads, ads_management
```

> ⚠️ If any permission shows as missing, reconnect Facebook (**Connect with Facebook** button in the Pages section).

***

## Method 4: Create a Quick Test Form

If you don't have a Lead Form yet for the Testing Tool:

1. Go to [Ads Manager](https://business.facebook.com/adsmanager)
2. Click **"+ Create"** → Objective: **Leads**
3. Set up a basic ad set (budget, audience — doesn't matter for testing)
4. In the Ad section, click **"Create Form"**
5. Add these basic fields:
   - Full Name
   - Email
   - Phone Number
6. Add a privacy policy URL (any URL works for testing)
7. **Save the form** (you don't need to publish the campaign!)
8. Now go back to the [Testing Tool](https://developers.facebook.com/tools/lead-ads-testing/) — your form will appear in the dropdown

***

## 🔍 Checking Sync History

After any test, check the **Sync History** page:

1. Go to **Meta Leads** → **Sync History**
2. You'll see a table with all sync attempts:

| Column | Example | Meaning |
| --- | --- | --- |
| **Date/Time** | 2026-02-06 10:30:15 | When the lead was received |
| **Meta Lead ID** | 123456789 | Facebook's internal lead ID |
| **Perfex Lead** | #42 — John Smith | The created lead in Perfex (with link) |
| **Status** | ✅ Success | Whether the sync was successful |
| **Message** | Lead created successfully | Details about the sync |

### Status Types:

| Status | Meaning | What to Do |
| --- | --- | --- |
| ✅ **Success** | Lead created in Perfex | Nothing — it worked! 🎉 |
| ❌ **Failed** | Something went wrong | Check the error message |
| ⚠️ **Skipped** | Lead was a duplicate | Expected if duplicate detection is on |
| 🔄 **Pending** | In retry queue | Will be retried automatically |

***

## ✅ Testing Checklist

Run through this checklist to make sure everything works:

- [ ] ✅ **Test Connection** — All green checkmarks
- [ ] ✅ **Send Test Lead** — Lead appears in CRM
- [ ] ✅ **Facebook Testing Tool** — Lead appears in CRM via webhook
- [ ] ✅ **Check Sync History** — Entry shows "Success"
- [ ] ✅ **Check the Lead** — All fields are correctly mapped
- [ ] ✅ **Check Assignment** — Lead is assigned to the right staff member
- [ ] ✅ **Check Source** — Lead has the correct source
- [ ] ✅ **Check Status** — Lead has the correct initial status
- [ ] ✅ **Email Notification** — Email received (if enabled)

***

## 🚨 Test Failed? 

Don't panic! Check the [Troubleshooting](../troubleshooting/troubleshooting.md) page for solutions to common issues.

***

## 🎉 All Tests Passed?

**Congratulations!** 🥳 Your Meta Leads integration is fully set up and working!

Now you can:
1. 🎯 Create and run real Lead Ad campaigns
2. 📊 Monitor leads in Sync History
3. 👤 Follow up with leads in Perfex CRM
4. ☕ Sit back and let automation do the work!

***

**Having issues? Check 👉** [**Troubleshooting**](../troubleshooting/troubleshooting.md)
