# Blufig Contact Org Chart — Zoho CRM Widget

A fully functional Contact Org Chart widget for Zoho CRM.
Displays contacts under an Account as an interactive visual hierarchy.

---

## Features
- Visual tree chart of contacts with reporting lines
- Sentiment badges: Supportive / Neutral / Against / Unknown
- List view toggle with hierarchy indentation
- Zoom in / out / reset on tree view
- Hover tooltips with name, title, email, phone
- Click any node to open the Contact record directly
- Works from the Account's Related List

---

## Prerequisites
- Zoho CRM **Professional, Enterprise, or Ultimate** edition
- Developer Permissions enabled in your CRM profile
- Contacts must have:
  - **Account Name** linked to the Account
  - **Reporting To** field filled in (for hierarchy lines)
  - *(Optional)* **Contact Friendliness** / **Friendliness** custom field for sentiment badges

---

## Installation Steps

### Option A — Upload as a Widget (Fastest for internal use)

1. **Zip** this folder:
   ```
   blufig-org-chart/
   ├── plugin-manifest.json
   └── app/
       └── widget.html
   ```
   Zip command (Mac/Linux): `zip -r blufig-org-chart.zip blufig-org-chart/`

2. In Zoho CRM go to:
   `Setup → Developer Hub → Widgets → New Widget`

3. Fill in:
   - **Name:** Contact Org Chart
   - **Hosting:** Zoho (upload the zip)
   - Upload the ZIP file

4. Click **Save**.

5. Now add it as a **Related List** on the Account layout:
   `Setup → Customization → Layouts & Fields → Accounts → [Edit Layout]`
   → Drag in **Custom Related List** → select your widget

6. Click **Save Layout**.

---

### Option B — Publish via Zoho Developer Console (for Marketplace / org-wide)

1. Go to [https://marketplace.zoho.com/developer](https://marketplace.zoho.com/developer)
2. Create a new **Extension for Zoho CRM**
3. Upload the zip under your extension's widget section
4. Configure it as a **Related List** widget on the **Accounts** module
5. Test, then publish privately to your org or publicly to the Marketplace

---

## Adding the Sentiment / Friendliness Field (Optional)

To show Supportive / Neutral / Against badges, create a **picklist custom field** on the Contacts module:

- **Field Name:** Contact Friendliness  
- **API Name:** Contact_Friendliness  
- **Values:** Supportive, Neutral, Against  

---

## File Structure

```
blufig-org-chart/
├── plugin-manifest.json    ← Extension config
└── app/
    └── widget.html         ← All UI, logic, and styles (self-contained)
```

---

## Support
Built by Blufig Digital — https://blufig.digital
