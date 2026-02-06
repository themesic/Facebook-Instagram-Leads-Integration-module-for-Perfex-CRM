# 📄 Step 3: Connect Your Pages

Almost there! Now we need to tell your Meta App **which Facebook Pages** to monitor for leads. 🎯

***

## 🧠 Why Do I Need to Connect a Page?

Lead Ads run on **Facebook Pages** (and linked Instagram accounts). Your Meta App needs permission to access a specific Page's lead data.

Think of it this way:

```
Your Meta App:  "Facebook, can I have the leads from Page XYZ?"
Facebook:       "Sure, let me check... ✅ You're the admin. Here you go!"
```

***

## 📱 Connect Your Facebook Account

### 1️⃣ Go to Module Settings

1. In Perfex CRM, go to **Meta Leads** → **Settings**
2. Scroll down to the **"Connected Pages"** section
3. Click the **"Connect with Facebook"** button 🔵

***

### 2️⃣ Log In & Grant Permissions

A Facebook popup window will appear:

1. **Log in** with the Facebook account that manages your Page
2. You'll see a list of **permissions** the app is requesting:

| Permission | What It Means | Why We Need It |
| --- | --- | --- |
| **Pages: Show list** | See your list of Pages | To know which Pages you manage |
| **Pages: Read engagement** | Read Page data | To access Page information |
| **Leads retrieval** | Access lead form data | 🎯 This is the main one! Retrieves submitted leads |
| **Page ads management** | Manage Page ads | To subscribe to lead notifications |
| **Ads management** | Manage ad campaigns | To interact with Lead Ad campaigns |

3. Click **"Continue"** or **"Allow"** ✅

> ⚠️ **Grant ALL permissions!** If you skip any, the module won't work correctly. You can always change permissions later in [Facebook Settings → Apps and Websites](https://www.facebook.com/settings?tab=applications).

***

### 3️⃣ Select Pages (if prompted)

Facebook might ask you **which Pages** to grant access to:

- ✅ Select **all Pages** you want to monitor for leads
- Or at minimum, select the Page(s) you'll run Lead Ads on

Click **Done** ✅

***

## 📋 Subscribe to Your Page

After connecting, you'll see a table with your Facebook Pages:

```
┌──────────────────┬────────────┬────────────────┬──────────┐
│ Page Name        │ Status     │ Leads Received │ Action   │
├──────────────────┼────────────┼────────────────┼──────────┤
│ My Business Page │ Not Active │ 0              │[Subscribe]│
│ Test Page        │ Not Active │ 0              │[Subscribe]│
└──────────────────┴────────────┴────────────────┴──────────┘
```

### For Each Page You Want to Monitor:

1. Click the green **"Subscribe"** button (or "Monitor") ✅
2. Wait a moment... ⏳
3. The status should change to **"Monitoring"** 🟢

> 🎉 **That's it!** This Page is now connected. Any Lead Ads running on this Page will automatically send leads to your Perfex CRM.

***

## 📸 What About Instagram?

**Great news — Instagram is automatic!** 🎉

If your Facebook Page is linked to an Instagram Business account (which is required for Instagram ads anyway), lead data from **Instagram Lead Ads** will flow through the **same Page webhook**. 

You don't need to do anything extra for Instagram. Same setup, both platforms. ✨

### How to check if Instagram is linked to your Page:

1. Go to your Facebook Page
2. Click **Settings** → **Linked Accounts** (or **Instagram**)
3. If you see your Instagram account linked, you're good to go!

***

## ✅ Multiple Pages

You can subscribe to **multiple Pages** at once! Just click "Subscribe" on each Page you want to monitor.

Each Page operates independently — you can subscribe/unsubscribe at any time.

***

## 🔄 Refreshing the Page List

If you create a new Facebook Page after the initial setup:

1. Go to **Meta Leads** → **Settings**
2. Click **"Connect with Facebook"** again
3. Grant access to the new Page
4. Subscribe to it

***

## ✅ Connection Complete!

At this point, your setup looks like this:

```
✅ Meta App created
✅ App ID & Secret configured
✅ Webhook verified
✅ Page(s) subscribed and monitoring

🎉 You're ready to receive leads!
```

***

## 🧪 Quick Test

Before moving on, let's verify everything works:

1. Go to **Meta Leads** → **Settings**
2. Click **"Test Connection"**
3. You should see:
   - ✅ App Credentials: Valid
   - ✅ Access Token: Valid
   - ✅ Permissions: All granted
4. Click **"Send Test Lead"**
5. Check if a test lead appears in **Perfex CRM → Leads** 🎉

> 💡 **Test lead not appearing?** Check the [Troubleshooting](../troubleshooting/troubleshooting.md) page.

***

**Pages connected! Want to learn about App Review (for advanced use cases)? 👉** [**App Review & Permissions**](app-review.md)

**Or skip ahead to configure the module 👉** [**Settings Page**](../module-configuration/settings.md)
