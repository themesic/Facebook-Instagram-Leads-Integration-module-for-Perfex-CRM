# ✅ App Review & Permissions

**TL;DR: You almost certainly do NOT need App Review.** 🎉 But let's explain why, so you're 100% clear.

***

## 🤔 What Is App Review?

App Review is a process where Meta (Facebook) reviews your app to make sure it follows their policies. It's required when an app wants to access **other people's data**.

***

## ❓ Do I Need App Review?

### ❌ NO — If You're Using the App for Your OWN Pages

This is the most common scenario. You create the app, you connect your own Page, you access your own leads.

| Scenario | App Review Needed? |
| --- | --- |
| You run Lead Ads on **your own** Facebook Page | ❌ No |
| You access leads from **your own** Page | ❌ No |
| You're the admin of both the App and the Page | ❌ No |
| Your app is in **Development Mode** | ❌ No |
| You have 1-5 Pages, all yours | ❌ No |

> 🎯 **This is you!** If you bought this module for your own business, you do NOT need App Review. Period.

### ✅ YES — Only If You're Building for Other People

App Review is only needed if:

| Scenario | App Review Needed? |
| --- | --- |
| You want strangers to connect their Pages to YOUR app | ✅ Yes |
| You're building a SaaS platform that accesses other people's data | ✅ Yes |
| You want more than ~2000 users using your app | ✅ Yes |

> 💡 **This module doesn't do that.** Each user creates their OWN app. Your app never touches anyone else's data.

***

## 🏗️ The Self-Hosted Model

Here's how this module works — and why App Review is not needed:

```
👤 Webmaster A                    👤 Webmaster B
   │                                 │
   ├── Creates OWN Meta App          ├── Creates OWN Meta App
   ├── Connects OWN Page             ├── Connects OWN Page
   ├── Accesses OWN leads            ├── Accesses OWN leads
   └── ✅ No review needed           └── ✅ No review needed
```

Each user:
1. Creates their **own** Meta App
2. Connects their **own** Facebook Page
3. Accesses their **own** lead data

Since everyone accesses only their own data through their own app, no review is needed. 🎉

> 📝 **This is the same model used by:**
> - WordPress plugins (WPForms, Gravity Forms)
> - Zapier integrations
> - Self-hosted CRM modules
> - Most SaaS Facebook integrations

***

## 🔑 Understanding Permissions

Your Meta App uses these permissions:

| Permission | What It Does | Review Needed? |
| --- | --- | --- |
| `pages_show_list` | List your Pages | ❌ No (for your own account) |
| `pages_read_engagement` | Read Page data | ❌ No (for your own Pages) |
| `leads_retrieval` | Access lead form submissions | ❌ No (for your own Pages) |
| `pages_manage_ads` | Manage Page ads | ❌ No (for your own Pages) |
| `ads_management` | Manage ad campaigns | ❌ No (for your own Pages) |

> 🔑 **All these permissions work in Development Mode** when you're the app admin/developer accessing your own Pages.

***

## 🛡️ Development Mode vs Live Mode

| Feature | 🔧 Development Mode | 🌐 Live Mode |
| --- | --- | --- |
| **Who can use it** | Only app admins/developers/testers | Anyone |
| **App Review required** | ❌ No | ✅ Yes |
| **Access your own data** | ✅ Yes | ✅ Yes |
| **Access others' data** | ❌ No | ✅ Yes (after review) |
| **Rate limits** | Lower (but fine for CRM use) | Higher |
| **What you should use** | ✅ **This one!** | Only if you need it |

> 🎯 **Stay in Development Mode.** It's all you need.

***

## 🚀 If You Ever DO Need App Review

Just in case you're curious, here's what the process looks like:

### What You'd Need:

1. **Business Verification** — Verify your business with Meta
2. **Privacy Policy URL** — A page explaining how you handle user data
3. **App Purpose** — Explain what your app does and why it needs each permission
4. **Screen Recording** — A video showing how your app uses the data
5. **Wait Time** — 1-5 business days for review

### How to Submit:

1. Go to [developers.facebook.com](https://developers.facebook.com)
2. Open your app
3. Click **"App Review"** in the left sidebar
4. Click **"Permissions and Features"**
5. Request each permission individually
6. Provide the required documentation
7. Submit for review

> ⚠️ **But again — you don't need this for using the module with your own Pages!**

***

## ✅ Summary

| Question | Answer |
| --- | --- |
| Do I need App Review? | **No** (for your own Pages) |
| Should I switch to Live mode? | **No** (Development is fine) |
| Can I access my own leads? | **Yes** ✅ |
| Can others use my app? | No (they create their own) |
| Is this normal? | **Yes!** This is industry standard |

***

**Ready to configure the module? 👉** [**Setup Wizard**](../module-configuration/setup-wizard.md)
