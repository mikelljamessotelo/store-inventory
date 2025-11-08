# 🧾 Mattmat’s Inventory — Simple (Drive Enabled)

**Version:** v3.2.4  
**Status:** Stable Build  
**Type:** Offline Inventory Management System  
**Author:** James

---

## 📘 About This Project

**Mattmat’s Inventory — Simple** is a **complete offline-first inventory system** built using **HTML, CSS, and vanilla JavaScript**.  
It runs entirely in your browser — **no installation, no server, no database** — and can optionally **sync with Google Drive** for backup.

This system is designed for **small businesses, sari-sari stores, and personal use**, offering a clean and practical way to track stock, costs, and purchases.

---

## 💡 Key Features

- 📦 **Item Management**
  - Add, edit, or delete products with barcode, category, and remarks.
  - Remarks include ready-to-use tags: *New, Fast Moving, Discontinued*.
  - Auto-calculates cost, markup, and suggested sell price.

- ☁️ **Google Drive Sync**
  - Import or export inventory backups from your Google Drive.
  - Automatically updates existing Drive files instead of creating duplicates.

- 📂 **CSV Import & Export**
  - Supports upsert logic — updates existing items by **barcode or name**, adds new ones if missing.
  - Includes all data fields (category, barcode, name, remarks, etc.).

- 🏷️ **Category & Remarks Manager**
  - Manage both categories and remarks in a unified view.
  - Import or export each as separate CSV tables.

- 🛒 **Purchase List**
  - Mark items to include in your purchase list.
  - Auto-saves each printed list with the date and time as its name.
  - Lists are importable/exportable as CSV.

- 💾 **Offline-Ready**
  - Fully functional without an internet connection — powered by `localStorage`.
  - Data persists even after closing your browser.

---

## ⚙️ Technical Overview

| Feature | Technology |
|----------|-------------|
| Frontend | HTML5, CSS3, Vanilla JavaScript |
| Storage | Browser localStorage |
| Cloud Sync | Google Drive API (optional) |
| File Handling | CSV import/export |
| Print Layout | Receipt-style, optimized for A4/thermal print |

---

## 🧱 Project Structure

```
mattmat_inventory_v3_2_4.html
├── Dashboard / Product Table
├── Add/Edit Item Modal (with Delete)
├── Categories & Remarks Management
├── Purchase List (Auto-save + Print)
└── LocalStorage + Drive Sync Engine
```

---

## 🖨️ Print Sample

Each purchase list prints in a **clean, receipt-like format**, showing:
- Category
- Product Name
- Cost per Pack
- Remarks (if any)
- Additional Notes (editable before print)

---

## 🔐 Data Behavior

| Action | Behavior |
|---------|-----------|
| Import CSV | Updates existing items by barcode or name; adds new ones |
| Export CSV | Includes all products with remarks and notes |
| Print Purchase List | Auto-saves list with timestamp |
| Delete Item | Removes the product permanently from localStorage |

---

## 🚀 How to Use

1. **Download** the latest HTML file (`mattmat_inventory_v3_2_4.html`).
2. **Open it in your browser** (Chrome recommended).
3. Add products, edit costs, and create purchase lists.
4. Optionally connect your Google Drive for cloud backup.
5. Export or print when needed — your data remains saved offline.

---

## 📜 License

This project is **free to use and modify** for personal or small business purposes.  
Attribution is appreciated but not required.

---

## ❤️ Credits

Developed by **James**, for small stores that need reliable, offline-ready tools.

---

### 🪄 Tip

For best performance:
- Keep your browser updated.
- Export your data regularly as a CSV backup.
- Enable Drive sync if you want cloud copies.
