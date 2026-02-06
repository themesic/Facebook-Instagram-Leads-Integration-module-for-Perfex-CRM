# 💡 What Are Lead Ads?

If you're new to Facebook/Instagram Lead Ads, this page explains everything you need to know. If you're already familiar, feel free to skip to [Create Your First Campaign](create-first-campaign.md)! 🚀

***

## 🤔 The Short Answer

**Lead Ads are a special type of Facebook/Instagram ad that includes a built-in form.** Users can submit their contact information **without ever leaving Facebook or Instagram**.

***

## 📱 How They Look to Users

Here's what a user sees:

```
┌─────────────────────────────────────────┐
│ 📱 Facebook/Instagram Feed              │
│                                         │
│  ┌─────────────────────────────────┐    │
│  │  Your Business                   │    │
│  │  Sponsored                       │    │
│  │                                  │    │
│  │  🖼️ [Your Ad Image/Video]       │    │
│  │                                  │    │
│  │  "Get a free quote today!"       │    │
│  │                                  │    │
│  │  [    Sign Up    ] ← CTA button │    │
│  └─────────────────────────────────┘    │
│                                         │
│  User taps "Sign Up"...                 │
│                                         │
│  ┌─────────────────────────────────┐    │
│  │  📝 Lead Form (inside Facebook)  │    │
│  │                                  │    │
│  │  Name:  [John Smith     ] ✅     │    │
│  │  Email: [john@email.com ] ✅     │    │
│  │  Phone: [+1 555-1234   ] ✅     │    │
│  │                                  │    │
│  │  ✨ Auto-filled from profile!    │    │
│  │                                  │    │
│  │  [      Submit      ]            │    │
│  └─────────────────────────────────┘    │
│                                         │
└─────────────────────────────────────────┘
```

### Key Points:

- 📱 The form opens **inside** Facebook/Instagram (no website needed!)
- ✨ Fields are **auto-filled** from the user's profile (name, email, phone)
- ⚡ Users can submit in **2 taps** (open form → submit)
- 📈 This makes conversion rates **much higher** than regular landing pages

***

## 🆚 Lead Ads vs Regular Ads

| Feature | Regular Ad | Lead Ad |
| --- | --- | --- |
| **Where user goes** | Your website | Stays on Facebook/Instagram |
| **Form location** | Your landing page | Built into Facebook |
| **User experience** | Load website → Find form → Fill in | Tap → Auto-filled → Submit |
| **Conversion rate** | Lower (more steps) | Higher (fewer steps) |
| **Need a website?** | Yes | No! |
| **Auto-fill** | No | Yes (from profile) |
| **Works with this module** | ❌ | ✅ |

> 🎯 **Lead Ads are the ONLY type of ad that works with this module.** Regular ads that send users to your website don't generate webhook data.

***

## 🔄 The Complete Flow

Here's what happens from start to finish:

```
1️⃣  You create a Lead Ad campaign in Facebook Ads Manager
         ↓
2️⃣  Your ad appears in users' Facebook/Instagram feeds
         ↓
3️⃣  A user taps your ad → Lead Form opens (inside Facebook)
         ↓
4️⃣  User fills out the form and taps "Submit"
         ↓
5️⃣  Facebook sends the lead data to your webhook (instantly!)
         ↓
6️⃣  Your module receives the data
         ↓
7️⃣  Module creates a new lead in Perfex CRM
         ↓
8️⃣  (Optional) Email notification sent to assigned staff
         ↓
9️⃣  You follow up with the lead! 🎉
```

**Steps 5-8 happen in SECONDS — fully automatically!** ⚡

***

## 💰 Do Lead Ads Cost Money?

**Yes.** Lead Ads are a form of Facebook advertising, so you need an **ad budget**. However:

| Cost Factor | Details |
| --- | --- |
| **Minimum budget** | As low as $1/day |
| **Average cost per lead** | $2-$15 (varies by industry) |
| **Billing** | You're charged per impression or per lead |
| **No cost to set up** | Creating the form is free — you only pay when ads run |

> 💡 **You don't need to spend money to test!** Facebook provides a free [Lead Ads Testing Tool](https://developers.facebook.com/tools/lead-ads-testing/) to send test leads without running real ads.

***

## 🎯 What Can You Ask in a Lead Form?

### Standard Fields (Auto-Filled)

These are pulled from the user's Facebook profile:

- 👤 Full Name / First Name / Last Name
- 📧 Email Address
- 📱 Phone Number
- 🏢 Company Name
- 💼 Job Title
- 📍 City, State, Country, Zip Code
- 🎂 Date of Birth
- ⚧️ Gender
- 🎖️ Military Status
- 💍 Marital Status

### Custom Questions

You can also add custom questions like:

- "What's your budget?"
- "When are you looking to purchase?"
- "What product are you interested in?"
- Multiple choice questions
- Short answer questions
- Conditional questions

> 💡 All these fields can be mapped to Perfex CRM fields using the [Field Mapping](../module-configuration/field-mapping.md) feature!

***

## 📺 Where Do Lead Ads Appear?

Your Lead Ads can appear in:

| Placement | Platform |
| --- | --- |
| 📰 News Feed | Facebook |
| 📖 Stories | Facebook |
| 🎬 Reels | Facebook |
| 📰 Feed | Instagram |
| 📖 Stories | Instagram |
| 🎬 Reels | Instagram |
| 🔍 Explore | Instagram |
| 📱 Messenger | Facebook Messenger |
| 🌐 Audience Network | Third-party apps |

> 💡 Facebook automatically optimizes placements for the best results. You can also manually choose where your ads appear.

***

## ✅ Summary

- **Lead Ads** = Special ads with built-in forms on Facebook/Instagram
- **No website needed** for the form (it's inside Facebook)
- **Auto-filled** from user profiles = higher conversion rates
- **Leads sent automatically** to your CRM via webhook
- **Cost money** to run (Facebook advertising), but free to test
- **This module** handles the automatic sync between Lead Ads and Perfex CRM

***

**Ready to create your first campaign? 👉** [**Create Your First Campaign**](create-first-campaign.md)
