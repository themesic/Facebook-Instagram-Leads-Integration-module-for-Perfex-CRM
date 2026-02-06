# 🔗 Step 2: Configure Webhooks

Now we'll tell Facebook **where** to send the lead data. This is called a "webhook" — it's like giving Facebook your CRM's mailing address. 📬

***

## 🧠 What Is a Webhook?

In simple terms:

```
Someone fills out your Lead Form on Facebook/Instagram
         ↓
Facebook says: "Hey, I got a new lead!"
         ↓
Facebook sends the lead data to YOUR webhook URL
         ↓
Your module receives it and creates the lead in Perfex CRM
```

A webhook is just a **URL on your server** that Facebook sends data to. The module creates this URL automatically — you just need to tell Facebook about it.

***

## 📋 Get Your Webhook Details from Perfex

Before going to Facebook, let's grab the details from your module:

1. Log into **Perfex CRM**
2. Go to **Meta Leads** → **Settings** in the sidebar
3. First, enter your **App ID** and **App Secret** (from Step 1) and click **Save Settings**
4. Scroll down to the **Webhook Settings** section
5. You'll see two values:

| Field | Example | What It Is |
| --- | --- | --- |
| **Webhook Callback URL** | `https://yourcrm.com/facebookleadsintegration/webhook` | Where Facebook sends data |
| **Verify Token** | `a1b2c3d4e5f6g7h8i9j0` | A secret code to verify the connection |

6. Click the 📋 **Copy** button next to each value

> ⚠️ **The Callback URL MUST start with `https://`** — Facebook requires SSL! If your URL starts with `http://`, you need to install an SSL certificate first.

***

## 🔧 Add Webhooks to Your Meta App

### 1️⃣ Open Your Meta App Dashboard

Go to your app at:

👉 [**https://developers.facebook.com/apps/**](https://developers.facebook.com/apps/)

Click on your app to open it.

***

### 2️⃣ Add the Webhooks Product

1. In the left sidebar, look for **"Add Product"** or scroll down on the dashboard
2. Find **"Webhooks"** in the product list
3. Click **"Set Up"** or **"Configure"**

> 💡 If you already see "Webhooks" in the left sidebar, click on it directly — no need to add it again.

***

### 3️⃣ Select "Page" as the Object Type

1. On the Webhooks page, you'll see a dropdown that says **"User"** by default
2. Change this dropdown to **"Page"** 📄

> ⚠️ **This is critical!** You MUST select "Page" — not "User", not "Application", not anything else. Lead data comes through Page subscriptions.

***

### 4️⃣ Subscribe to the Webhook

1. Click the **"Subscribe to this object"** button (or **"Edit Subscription"** if already configured)
2. A dialog box will appear asking for two values:

| Field | What to Enter |
| --- | --- |
| **Callback URL** | Paste your Webhook URL from the module (e.g., `https://yourcrm.com/facebookleadsintegration/webhook`) |
| **Verify Token** | Paste your Verify Token from the module |

3. Click **"Verify and Save"** ✅

***

### 5️⃣ What Happens When You Click "Verify and Save"

Facebook will immediately send a **verification request** to your webhook URL:

```
Facebook: "Hey, is this really your server?"
Your Module: "Yes! Here's the verify token to prove it!"
Facebook: "Great, verified! ✅"
```

**If it works:** You'll see a success message and the dialog closes. 🎉

**If it fails:** See the [Troubleshooting](../troubleshooting/troubleshooting.md) section for common fixes.

***

### 6️⃣ Subscribe to "leadgen" Events

After verification, you need to tell Facebook **what** events to send:

1. You'll see a list of event types under "Page" subscriptions
2. Find **"leadgen"** in the list (you might need to scroll)
3. Click the **"Subscribe"** toggle/checkbox next to "leadgen" ✅

> 💡 **"leadgen" is the ONLY event you need.** You don't need to subscribe to any other events (like "messages" or "feed"). Just "leadgen".

***

## ✅ Verification Successful!

Your webhook configuration should now look like this:

```
Webhooks
├── Object: Page
├── Callback URL: https://yourcrm.com/facebookleadsintegration/webhook ✅
├── Verify Token: ✅ Verified
└── Subscriptions:
    └── ✅ leadgen (subscribed)
```

Back in your **Perfex CRM module**, the webhook status indicator should now show **green/Verified**! 🟢

***

## 🔍 How to Test the Webhook

Want to make sure the webhook is working? 

1. Go to your **Perfex CRM** → **Meta Leads** → **Settings**
2. Click the **"Test Connection"** button
3. You should see all green checkmarks ✅

We'll do more thorough testing later in the [Testing Leads](../lead-ads/testing-leads.md) section.

***

## ⚠️ Common Mistakes to Avoid

| Mistake | Fix |
| --- | --- |
| 🚫 Selected "User" instead of "Page" | Change the dropdown to "Page" |
| 🚫 Forgot to subscribe to "leadgen" | Find "leadgen" in the list and subscribe |
| 🚫 Using HTTP instead of HTTPS | Install SSL certificate on your server |
| 🚫 Typo in the Callback URL | Copy-paste directly from the module settings |
| 🚫 "Callback URL couldn't be validated" | Check [Troubleshooting](../troubleshooting/troubleshooting.md#webhook-verification-fails) |

***

**Webhook configured? Awesome! Let's connect your Facebook Pages! 👉** [**Connect Your Pages**](connect-pages.md)
