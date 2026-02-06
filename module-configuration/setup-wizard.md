# 🧙 Setup Wizard

When you first visit the module, you'll see a guided **Setup Wizard** that walks you through the entire configuration. It's like having a friend hold your hand through the process! 🤝

***

## 🚀 How to Access the Setup Wizard

The wizard appears automatically the first time you open the module:

1. Go to **Meta Leads** → **Settings** in the sidebar
2. If it's your first time, the wizard starts automatically
3. If not, you can access it at: `https://yourcrm.com/admin/facebookleadsintegration/setup_wizard`

***

## 📋 The 5 Steps

### Step 1️⃣: Create Facebook App

The wizard shows instructions for creating your Meta App.

- Follow the on-screen instructions (or the detailed guide at [Create a Meta App](../facebook-app-setup/create-app.md))
- Click the **"Create Facebook App"** link to go directly to Meta
- Once created, click **"Next Step"** ➡️

***

### Step 2️⃣: Enter App Credentials

Enter the credentials from your Meta App:

| Field | Where to Find It |
| --- | --- |
| **App ID** | Meta App → Dashboard (top of page) |
| **App Secret** | Meta App → Settings → Basic → Show |

After entering both:

1. Click **"Validate Credentials"** ✅
2. Wait for the green checkmark
3. Click **"Next Step"** ➡️

> ⚠️ You can't proceed to Step 3 until your credentials are validated!

***

### Step 3️⃣: Configure Webhooks

The wizard displays your unique **Webhook URL** and **Verify Token**:

1. Click the 📋 **Copy** button next to the Webhook URL
2. Click the 📋 **Copy** button next to the Verify Token
3. Open your Meta App and configure the webhook (see [Configure Webhooks](../facebook-app-setup/configure-webhooks.md))
4. Once configured in Facebook, click **"Next Step"** ➡️

***

### Step 4️⃣: Connect Facebook Pages

1. Click the **"Connect with Facebook"** button 🔵
2. Log in with Facebook and grant permissions
3. Your Pages will appear in a table
4. Click **"Subscribe"** on each Page you want to monitor ✅
5. Click **"Next Step"** ➡️

***

### Step 5️⃣: Configure Lead Settings

Set the default values for incoming leads:

| Setting | What It Does | Example |
| --- | --- | --- |
| **Default Assigned** | Staff member assigned to new leads | "John Smith" |
| **Default Source** | Lead source in Perfex CRM | "Facebook" |
| **Default Status** | Initial lead status | "New" |

Click **"Complete Setup"** 🎉

***

## 🎉 Setup Complete!

After completing the wizard, you'll be redirected to the main settings page where you can:

- See your connection status
- Run a test lead
- Fine-tune settings

> 💡 **You can always change these settings later** on the main Settings page!

***

## ⏭️ Skip the Wizard

If you prefer to configure everything manually, click **"Skip setup wizard and configure manually"** at the bottom of the wizard page.

***

**Want to learn about all the settings in detail? 👉** [**Settings Page**](settings.md)
