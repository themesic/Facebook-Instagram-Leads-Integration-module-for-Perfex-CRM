# 🔀 Field Mapping

Field mapping is how you tell the module: "When Facebook sends a field called `email`, put it in the **Email** field in Perfex CRM." 🗂️

***

## 🔗 How to Access

Go to **Meta Leads** → **Field Mapping** in the sidebar.

Or navigate to: `https://yourcrm.com/admin/facebookleadsintegration/field_mapping`

***

## 🧠 How Field Mapping Works

When someone fills out your Lead Form on Facebook/Instagram, the data looks like this:

```json
{
  "full_name": "John Smith",
  "email": "john@example.com",
  "phone_number": "+1234567890",
  "company_name": "Acme Corp",
  "city": "New York"
}
```

The module needs to know **where to put each value** in Perfex CRM:

```
Facebook Field          →    Perfex CRM Field
─────────────────────────────────────────────
full_name               →    Lead Name
email                   →    Email
phone_number            →    Phone
company_name            →    Company
city                    →    City
```

***

## 🔄 Default Mappings (Automatic!)

**Good news!** The module comes with **built-in default mappings** for common Facebook fields. These work automatically — no configuration needed! 🎉

| Facebook Field | Perfex CRM Field | Auto-Mapped? |
| --- | --- | --- |
| `full_name` | Lead Name | ✅ Yes |
| `first_name` + `last_name` | Lead Name | ✅ Yes |
| `email` | Email | ✅ Yes |
| `phone_number` | Phone | ✅ Yes |
| `company_name` | Company | ✅ Yes |
| `street_address` | Address | ✅ Yes |
| `city` | City | ✅ Yes |
| `state` | State | ✅ Yes |
| `country` | Country | ✅ Yes |
| `zip_code` | Zip Code | ✅ Yes |
| `website` | Website | ✅ Yes |
| `job_title` | Position | ✅ Yes |

> 💡 If your Lead Form uses these standard Facebook field names, **everything maps automatically!** You don't need to configure anything.

***

## ✏️ Custom Field Mappings

For any **non-standard** fields (custom questions in your Lead Form), you can create custom mappings.

### Adding a Custom Mapping

1. Go to **Field Mapping** page
2. Click **"Add Mapping"** ➕
3. Fill in:

| Column | What to Enter | Example |
| --- | --- | --- |
| **Facebook Field** (left box) | The field name from your Lead Form | `budget` |
| **Perfex CRM Field** (right dropdown) | Where to store it in Perfex | "Description" or a custom field |

4. Click **"Save Mappings"** 💾

### Example: Custom Questions

Say your Lead Form asks: *"What's your monthly budget?"*

If you named the field `monthly_budget` in your Lead Form:

```
Facebook Field: monthly_budget    →    Perfex CRM Field: Description
```

Or if you have a custom field in Perfex:

```
Facebook Field: monthly_budget    →    Perfex CRM Field: leads_budget (custom)
```

***

## 🏷️ Using Perfex CRM Custom Fields

If you've created **custom fields** for leads in Perfex CRM, they'll appear in the dropdown under **"Custom Fields"**.

### How to Create a Custom Field:

1. In Perfex CRM, go to **Setup** → **Custom Fields**
2. Click **New Custom Field**
3. Set:
   - **Field Belongs To:** Leads
   - **Field Name:** e.g., "Budget"
   - **Slug:** e.g., `leads_budget`
4. Save

This custom field will now appear in the Field Mapping dropdown! 🎉

> 💡 **Pro tip:** Name your Facebook form fields using the **same slug** as your Perfex custom fields (e.g., `leads_budget`), and they'll be automatically mapped without any manual configuration!

***

## 🔍 Finding Your Facebook Field Names

Not sure what your Facebook form fields are called? Here's how to find out:

### Method 1: Check the Lead Form in Ads Manager

1. Go to [Facebook Ads Manager](https://business.facebook.com/adsmanager)
2. Open your campaign → Ad set → Ad
3. Click on the Lead Form
4. Look at the field names (the "Field Name" or "Question ID")

### Method 2: Check a Test Lead

1. Send a test lead from the module (**Settings** → **"Send Test Lead"**)
2. Go to **Sync History**
3. Click on the test lead entry
4. You'll see the exact field names Facebook sent

### Method 3: Use Facebook's Lead Ads Testing Tool

1. Go to [Lead Ads Testing Tool](https://developers.facebook.com/tools/lead-ads-testing/)
2. Select your Page and Form
3. Create a test lead
4. Check **Sync History** for the field names

***

## 🗑️ Removing Mappings

To remove a custom mapping:

1. Click the red **✕** button next to the mapping row
2. Click **"Save Mappings"** 💾

> ⚠️ Removing a mapping doesn't delete existing leads — it only affects **future** leads.

***

## 📋 Mapping Priority

When a lead comes in, the module processes fields in this order:

1. 🥇 **Custom mappings** (your manual configurations) — checked first
2. 🥈 **Default mappings** (built-in standard fields) — used as fallback
3. 🥉 **Auto-detection** (if field name matches a Perfex custom field slug)

> This means your custom mappings always take priority over default ones!

***

## ⚠️ Common Questions

### "What if I don't configure any mappings?"

The default mappings will handle all standard fields automatically. You only need custom mappings for custom questions in your Lead Forms.

### "What if Facebook sends a field I haven't mapped?"

It will be stored in the lead's **Description** field as additional data, so you never lose information.

### "Can I map one Facebook field to multiple Perfex fields?"

Not directly — each Facebook field maps to one Perfex field. If you need this, use Perfex CRM's workflow automations.

***

**Ready to learn about Lead Ads? 👉** [**What Are Lead Ads?**](../lead-ads/what-are-lead-ads.md)
