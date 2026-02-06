# 📦 Installation

Installing the module is quick and easy. Just upload, activate, and you're ready to configure! 🎉

***

## 📥 Step 1: Download the Module

1. Go to your [CodeCanyon Downloads](https://codecanyon.net/downloads)
2. Find **"Facebook & Instagram Leads Integration for Perfex CRM"**
3. Click **Download** → Choose **"Installable File Only"**
4. You'll get a `.zip` file — **don't extract it yet!** 📁

***

## 📤 Step 2: Upload to Perfex CRM

### Option A: Upload via Admin Panel (Recommended) ✨

1. Log into your **Perfex CRM Admin Panel**
2. Go to **Setup** → **Modules**
3. Click the **📤 Upload Module** button (top right)
4. Select the `.zip` file you downloaded
5. Click **Upload**
6. Wait for the upload to complete ⏳

### Option B: Upload via FTP/File Manager 📂

If the upload button doesn't work (file too large), use this method:

1. **Extract** the `.zip` file on your computer
2. You should see a folder called `facebookleadsintegration`
3. Upload this entire folder to:
   ```
   your-perfex-crm/modules/facebookleadsintegration/
   ```
4. Make sure the structure looks like this:
   ```
   modules/
   └── facebookleadsintegration/
       ├── facebookleadsintegration.php    ← Main file
       ├── controllers/
       ├── views/
       ├── libraries/
       ├── language/
       ├── vendor/
       └── ...
   ```

> ⚠️ **Common mistake:** Don't put the folder inside another folder! The path should be `modules/facebookleadsintegration/facebookleadsintegration.php` — NOT `modules/facebookleadsintegration/facebookleadsintegration/facebookleadsintegration.php`

***

## ✅ Step 3: Activate the Module

1. Go to **Setup** → **Modules**
2. Find **"Facebook & Instagram Leads Integration"** in the list
3. Click the **Activate** button ✅
4. Enter your **Purchase Code** when prompted
   - 🔑 Find it in [CodeCanyon → Downloads → License Certificate](https://help.market.envato.com/hc/en-us/articles/202822600-Where-Is-My-Purchase-Code-)
5. Click **Activate**

> 🎉 **Success!** You should see the module listed as "Active" with a green indicator.

***

## 🔍 Step 4: Verify Installation

After activation, you should see:

1. ✅ **"Meta Leads"** in the left sidebar menu
2. ✅ Three sub-menu items: Settings, Sync History, Field Mapping
3. ✅ The Setup Wizard should appear automatically on first visit

> 💡 **Don't see the sidebar menu?** Make sure your Perfex CRM user has **admin** or **settings** permissions.

***

## 🔄 Updating the Module

To update to a newer version:

1. Download the latest version from CodeCanyon
2. Go to **Setup** → **Modules**
3. **Deactivate** the current module
4. Upload the new version (same as Step 2 above)
5. **Activate** the module again
6. Database migrations will run automatically 🔄

> ⚠️ **Your settings, field mappings, and sync history are preserved during updates.** Nothing gets lost!

***

## 🗑️ Uninstalling

If you ever need to remove the module:

1. Go to **Setup** → **Modules**
2. Click **Deactivate** on the module
3. Optionally delete the `modules/facebookleadsintegration/` folder

> ⚠️ **Note:** Uninstalling does NOT delete your leads from Perfex CRM. Only the module's own data (sync history, field mappings) is affected.

***

**Module installed? Awesome! Let's create your Meta App! 👉** [**Create a Meta App**](../facebook-app-setup/create-app.md)
