# 🏗️ Step 1: Create a Meta App

This is where we create the "bridge" between Facebook/Instagram and your Perfex CRM. Don't worry — it's free, and you **don't** need to be a developer! 😊

***

## 🧠 What Is a "Meta App"?

Think of it like this:

```
Facebook/Instagram  ←→  🌉 Your Meta App  ←→  Your Perfex CRM
```

The Meta App is just a **bridge** that allows Facebook to send lead data to your CRM. It's not a mobile app or a website — it's just a configuration on Meta's developer platform.

> 💡 **Key point:** Each person using this module creates their **own** Meta App. It takes 3 minutes and it's completely free.

***

## 📝 Let's Create the App!

### 1️⃣ Go to Meta for Developers

Open this link in a new tab:

👉 [**https://developers.facebook.com/apps/create/**](https://developers.facebook.com/apps/create/)

> 🔑 You'll need to log in with your **Facebook account**. If you haven't used Meta for Developers before, you might be asked to register — just follow the prompts, it's instant.

***

### 2️⃣ Select App Type

You'll see a page asking you to choose what kind of app to create.

**Here's what to do:**

1. On the left sidebar, you'll see filter options
2. Click **"Other"** to filter by "Other" category 👈
3. Scroll down to the bottom of the list
4. Select **"Create an app without a use case"** (it's the last option) ✅

> ⚠️ **Don't select "Business"** or any other option! You specifically want **"Create an app without a use case"** — this gives you the most flexibility.

***

### 3️⃣ Business Portfolio

On the next screen, you'll be asked about connecting a business portfolio:

1. Select **"I don't want to connect a business portfolio yet."** ✅
2. Click **Next**

> 💡 **Why?** You can always connect a business portfolio later if needed. For now, keeping it simple is best.

***

### 4️⃣ Enter App Details

Now fill in the basic details:

| Field | What to Enter | Example |
| --- | --- | --- |
| **App Name** | A friendly name for your app | `My CRM Leads` |
| **Contact Email** | Your email address | `you@yourcompany.com` |

> 💡 **Tip for the app name:** Use something descriptive like "Your Company CRM Leads" or "My Business Leads". This name is only visible to you in the Meta developer portal.

Click **Create** ✅

***

### 5️⃣ You're In! 🎉

You should now see your **App Dashboard**. It looks something like this:

```
┌──────────────────────────────────────┐
│  Your App Dashboard                   │
│                                       │
│  App ID: 123456789012345             │
│  Status: In Development              │
│                                       │
│  Products:                           │
│  [+ Add Product]                     │
└──────────────────────────────────────┘
```

***

## 🔑 Get Your App ID and App Secret

Now we need two pieces of information from your app. Think of them as your app's **username** and **password**.

### Finding Your App ID

1. Look at the top of the page — you'll see **"App ID: XXXXXXXXXXX"**
2. Copy this number 📋

> 💡 The App ID is also visible in the URL bar: `https://developers.facebook.com/apps/YOUR_APP_ID/dashboard/`

### Finding Your App Secret

1. In the left sidebar, click **App settings** → **Basic**
2. You'll see:
   - **App ID** (already have this ✅)
   - **App Secret** — click **"Show"** next to it
3. Enter your Facebook password when asked
4. Copy the App Secret 📋

> 🔒 **KEEP YOUR APP SECRET... SECRET!** 🤫
> 
> Never share it publicly, never put it in client-side code, never post it on forums. If someone gets your App Secret, they can impersonate your app. If it's ever exposed, you can reset it from this same page.

***

## 📝 Save These Credentials

You now have two important values. Keep them handy — you'll need them in the next steps!

| Credential | Value | Looks Like |
| --- | --- | --- |
| **App ID** | `_______________` | `123456789012345` |
| **App Secret** | `_______________` | `abc123def456ghi789jkl012` |

***

## ❓ Do I Need to Set the App to "Live" Mode?

**No!** 🎉 Here's the deal:

| Mode | Who Can Use It | Needs Review? |
| --- | --- | --- |
| **Development** (default) | Only you (the app admin/developer) | ❌ No |
| **Live** | Anyone with a Facebook account | ✅ Yes |

Since **you** are creating the app and **you** are connecting your own pages:

> ✅ **Development Mode is perfectly fine!** You do NOT need to submit for app review or switch to Live mode.

This is the standard approach used by self-hosted integrations everywhere — WordPress plugins, CRM modules, Zapier connectors, etc.

***

## ⚠️ Common Mistakes to Avoid

| Mistake | Why It's Wrong | What to Do |
| --- | --- | --- |
| 🚫 Selecting "Business" app type | Adds unnecessary restrictions | Select "Other" → "Create an app without a use case" |
| 🚫 Connecting a business portfolio | Not needed, adds complexity | Select "I don't want to connect a business portfolio yet" |
| 🚫 Sharing your App Secret | Security risk! | Keep it private, store it only in your module settings |
| 🚫 Trying to go "Live" right away | Not needed for your own pages | Stay in Development mode |

***

**Got your App ID and App Secret? Great! Let's set up the webhook! 👉** [**Configure Webhooks**](configure-webhooks.md)
