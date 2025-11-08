# 🧾 Store Inventory — Version 3.2.8b (Uncheck All Fix)

## 📦 Overview
**Store Inventory** is a single-file, offline-ready HTML inventory system built for sari-sari stores and small retail operations.  
It allows easy tracking of products, purchases, categories, and remarks — all in one page.  

All information is saved locally using **browser localStorage**, so no server or installation is required.  
For cloud backups and synchronization, optional **Google Drive integration** is available (via embedded API key and client ID).

---

## 🧩 Version History

### 🆕 v3.2.8b (November 2025)
**Fixes & UI Enhancements**
- 🧹 **Uncheck All Button**
  - Same height as other buttons  
  - Text stays in a single line (no wrap)  
  - Perfectly aligned vertically for consistent layout  

**Carried over from v3.2.8a**
- ✅ Fixed **+ / − buttons** for Packs and Pcs per Pack (now fully working in Add & Edit modals)
- ☀️ Default **Light Mode** on load
- 📂 **Categories / Remarks** button moved beside 💰 **Edit Cost**
- 🗑️ Removed "Delete Item" from header (now available inside Edit form)
- 🛒 **Purchase List Summary Bar**
  - Displays **file name** (left) and **total cost** (right, bold)
- 🧾 **Print View**
  - Total cost shown at the **bottom** of the table
  - Clean, text-only receipt-style output (white background, no borders)
- 💾 **Wide green “Save” button** for better visibility and touch support
- 📄 Sticky table headers + auto height adjustment for any screen size
- ☁️ Embedded **Google Drive integration** for data backup and restore
- 📂 Retained import/export with **upsert logic** (barcode or name matching)

---

### v3.2.8a
- Fixed `+ / −` numeric control buttons  
- Retained all functions from v3.2.8  
- Added default **Light Mode** behavior  
- Embedded existing Google API Key and Client ID  

### v3.2.8
- Added Purchase List top summary (file name + total cost)  
- Added total row at end of printed purchase list  
- Moved Categories / Remarks button beside Edit Cost  
- Removed Delete Item button from main header (now inside Edit form)  

---

## 🧰 Core Features

### 🏷️ Product Management
- Add, edit, or delete items  
- Auto-computed cost and suggested sell price  
- “Sell Price” blank if value = 0  
- Negative values highlighted in red  
- Editable remarks (e.g., *New, Fast Moving, Discontinued*)

### 🗂️ Categories & Remarks
- Add, edit, or delete categories and remarks  
- Manage both on a single screen  
- Auto-sync to dropdowns in Add/Edit forms  

### 🛒 Purchase List
- Add items to a purchase list via toggle buttons  
- Auto-calculated total cost  
- Save, load, import, or export purchase lists  
- Print purchase lists (receipt-style)  
- Purchase List file names auto-generate with **timestamp**  
- Total appears at the **end** of the printed list  

### 💾 Data Tools
- Backup or restore all data to localStorage  
- Import/export via CSV  
- Safe reset option  
- Google Drive sync: upload/download backups directly to Drive  

### 🌗 Appearance
- **Light mode by default** (dark mode toggle available)  
- Responsive layout for tablets and desktops  
- Sticky headers and dynamic table height  

---

## 💡 Notes & Tips
- Data is saved automatically — no manual save needed.  
- You can close or refresh the browser; your data stays safe in localStorage.  
- Export backups regularly to prevent accidental loss.  
- Works **offline** once loaded.  
- For best performance, use **Google Chrome** or **Microsoft Edge (latest version)**.  

---

## ⚙️ Technical Details
| Key | Description |
|-----|--------------|
| **File Name** | `index.html` |
| **Version** | `3.2.8b` |
| **Author** | James |
| **Project Branch** | Mattmat’s Inventory — Simple |
| **Release Date** | November 2025 |
| **Storage** | Browser localStorage |
| **Cloud Sync** | Google Drive (Drive API v3) |
| **Backup Formats** | CSV, JSON |
| **Suggested Browsers** | Chrome / Edge |
| **Offline Support** | Yes |

---

## ☁️ Google Integration
- **API Key** and **Client ID** embedded from v3.2.7  
- Google Drive upload/download works if authenticated  
- Backups include products, categories, remarks, and purchase lists  

> 🔒 Your Drive data remains private — access is limited to your own account and authorized app scope (`drive.file`).

---

## 🧱 Data Structure (Simplified)
```json
{
  "id": "id_abc123",
  "category": "Snacks",
  "barcode": "4800123456789",
  "name": "Piattos Cheese",
  "packs": 1,
  "pcsPerPack": 12,
  "costPerPack": 120,
  "cost": 10,
  "sellPrice": 12,
  "suggestedSellPrice": 12,
  "markup": 2,
  "checked": false,
  "notes": "",
  "remarks": "Fast Moving"
}
```

---

## 📤 Export / Import Logic
- **Export CSV:** all items, with consistent columns for re-import  
- **Import CSV:** automatically *upserts* (matches existing items by `barcode` or `name`)  
- Fields that don’t exist are safely ignored  
- Compatible with older versions (3.2.x series)  

---

## 🔁 Backup / Restore
- Backup all data to `.json`  
- Restore safely by loading a previous backup file  
- Google Drive can be used for remote backup and restore  

---

## 🧾 Printing Behavior
- Clean receipt-style layout (no borders or shading)  
- Automatically includes timestamped file name as title  
- Total cost line displayed at the end  
- Background forced to **white** for printer consistency  

---

## 🧹 Uncheck All Button
- Works globally to uncheck every item  
- Uniform height and single-line layout for better appearance  
- Confirmation prompt before unchecking  

---

## 📋 Changelog Summary
| Version | Highlights |
|----------|-------------|
| **3.2.8b** | Uncheck All button fix (layout, alignment) |
| **3.2.8a** | Numeric + / − controls fixed |
| **3.2.8** | Purchase list top summary & print total |
| **3.2.7** | Google Drive integration and layout refinements |
| **3.2.6** | Button alignment, pack/pcs auto controls, cost auto-update |
| **3.2.5** | Sticky headers, filters, dark mode, data tools panel |

---

## 👨‍💻 Developer Notes
- Project is fully self-contained: one HTML file (no external dependencies beyond Google APIs).  
- Written in pure **HTML + JavaScript + CSS**, no frameworks.  
- Modularized event bindings and upsert logic for long-term maintenance.  
- Version roadmap tracked up to **v14+** (future builds will expand reporting and analytics).

---

## 🏁 License
This project is proprietary and customized for **Mattmat’s Sari-sari Store System**.  
Distribution or modification is allowed **only with author’s permission**.

---

## ✉️ Author
**James**  
📍 Philippines  
💬 Developer of *Mattmat’s Inventory — Simple* and *Mattmat’s Sari-sari Store System*

---
