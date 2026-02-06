# 📝 Changelog

All notable changes to the Facebook & Instagram Leads Integration module are documented here.

***

## 🚀 [2.0.0] — 2026-02-05

### ✨ Added

- 📸 **Instagram Lead Ads Support** — Full support for Instagram Lead Ads (same webhook, automatic)
- 🧙 **Setup Wizard** — Guided 5-step setup wizard for first-time configuration
- 📊 **Sync History Dashboard** — View all lead syncs with status, timestamps, and details
- 🔍 **Connection Test** — One-click button to verify credentials and permissions
- 🧪 **Test Lead** — Send a test lead to verify the integration is working
- 🔍 **Duplicate Detection** — Configurable option to prevent importing the same lead twice
- 🔀 **Field Mapping Interface** — Visual interface to map custom form fields to Perfex CRM fields
- 🔁 **Retry Queue** — Automatic retry mechanism for failed lead syncs
- 📧 **Email Notifications** — Get notified when new leads arrive from Facebook/Instagram
- 🔔 **Webhook Verification Status** — Visual indicator showing if webhook is verified
- 📈 **Statistics Dashboard** — Real-time stats showing sync success/failure rates
- 📋 **Sidebar Navigation** — Easy access to all features from the sidebar
- 📝 **Database Logging** — Comprehensive logging of all sync activities
- 🏷️ **Custom Field Support** — Map to any Perfex CRM custom field

### 🔄 Changed

- 📡 **Graph API Version** — Updated from v5.0 to v19.0 (latest stable)
- 🔒 **Token Exchange** — Moved to server-side for security (App Secret no longer in JavaScript)
- ⚡ **Webhook Handler** — Completely rewritten with async processing and instant 200 response
- 🎨 **Settings Interface** — Modern, intuitive design with better organization
- 📄 **Pages Management** — Improved subscription interface with status indicators and lead counts
- 💬 **Error Handling** — Better error messages and user feedback throughout

### 🐛 Fixed

- 🔴 **Critical:** Fixed missing Facebook PHP SDK reference
- 🔴 **Critical:** Fixed webhook handler session dependency that caused lead loss
- 🔒 **Security:** Removed App Secret from client-side JavaScript
- 🔒 **Security:** Added proper input validation and sanitization
- 🔒 **Security:** Removed debug file writes from production code
- 🔒 **Security:** Added webhook signature verification (X-Hub-Signature-256)
- 🐛 **Bug:** Fixed CSRF exclusion (now uses proper hooks instead of config modification)
- 🐛 **Bug:** Fixed country lookup for international leads

### 🗑️ Removed

- Debug file writing functionality
- Unused GuzzleHttp import
- Legacy settings page view

### 🔒 Security Improvements

- All POST endpoints validate CSRF tokens
- Access tokens no longer exposed in HTML onclick handlers
- App Secret used only server-side
- Webhook signature verification enabled

***

## 📦 [1.0.0] — 2020-01-15

### ✨ Added

- 🎉 Initial release
- 📱 Basic Facebook & Instagram Lead Ads integration
- 🔑 OAuth connect for page access
- 📡 Webhook support for real-time leads
- 📄 Multiple page monitoring
- 🏷️ Custom field synchronization

***

## 🔮 Planned for Future Releases

- 📊 Advanced analytics and reporting
- 🔄 Automatic token refresh
- 📱 Mobile app notifications
- 🌍 Multi-language support
- 🔗 CRM automation triggers on lead import
- 📋 Lead scoring based on form data
