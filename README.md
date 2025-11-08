# 🧾 Store Inventory — Version 3.2.5

**Status:** Major Update (Unified Feature Release)  
**Type:** Offline Inventory Management System  
**Author:** James

---

## 📘 About This Project

**Store Inventory — Version 3.2.5** is a single-file, **offline-first inventory system** built entirely with **HTML, CSS, and JavaScript**.  
It’s lightweight, runs directly in your browser, and saves data using `localStorage` — no installation, database, or internet required.

This version unifies all major improvements from previous builds for better usability, visibility, and control.

---

## 💡 Key Features

### 🖥️ Interface & Display
- Sticky (fixed) product table headers  
- Table height automatically adjusts to screen size  
- Dark mode toggle 🌙  
- Wider **green Save button** for visibility  
- Centered columns for **Cost**, **Sell Price**, and **Suggested Sell Price**  
- Negative numbers shown in **red font**  
- **Sell Price** always displayed in **bold font**  

### 💰 Data & Display Behavior
- If Sell Price is `0`, display it as **blank** instead of `0.00`  
- Dropdown filters for **Category** and **Remarks**  
- Combined text + dropdown search functionality  

### 🧾 Purchase List Enhancements
- Displays the **loaded purchase list filename** at the top (bold)  
- Ability to **Unload/Clear** the current list  
- Auto PDF filename format: **“Purchase List - [Date and Time]”**  
- Automatically saves the purchase list on print  

### 🧰 Data Tools
- Manual **Backup / Restore** (via JSON file)  
- **Reset all data** with confirmation  
- **Safe import from older versions**  
- Optional **CSV backup archive**  

### ☁️ Import / Export
- Import and Export data as CSV files  
- Upsert logic: updates existing items (by barcode or name) or adds new ones  
- Includes all item details — category, remarks, notes, etc.  

---

## ⚙️ Technical Overview

| Feature | Technology |
|----------|-------------|
| Frontend | HTML5, CSS3, Vanilla JavaScript |
| Storage | Browser localStorage |
| Optional Sync | Google Drive API (optional, hidden integration) |
| File Handling | CSV import/export, JSON backup |
| Print Layout | Receipt-style, timestamped, PDF-ready |

---

## 🧱 Project Structure

```
store_inventory_v3_2_5.html
├── Dashboard / Product Table
├── Add/Edit/Delete Item Modal
├── Categories & Remarks Management
├── Purchase List (Auto-save + Print)
├── Data Tools (Backup / Restore / Reset)
└── LocalStorage + CSV Logic
```

---

## 🖨️ Printing

When printing the purchase list:
- The filename automatically becomes **“Purchase List - [Date and Time]”**
- Each item’s **Remarks** appear in the Notes section if available
- Clean, receipt-style layout ideal for A4 or thermal printing

---

## 🚀 How to Use

1. **Download** `store_inventory_v3_2_5.html`
2. **Open** it in your browser (Chrome recommended)
3. Add or edit products — all data is saved locally
4. Create purchase lists and print receipts instantly
5. Optionally import/export data via CSV or JSON backups

---

## 🧮 Tips & Notes
- Use **Backup** in Data Tools regularly to save your inventory snapshot.
- Enable **Dark Mode** for night viewing.  
- Use **Category** and **Remarks** filters for faster product lookup.  
- Negative prices highlight in red for easy tracking.

---

## 📜 License

Free to use and modify for personal or small business purposes.  
Attribution is appreciated but not required.

---

## ❤️ Credits

Developed by **James** — for small stores and local entrepreneurs who need a simple, reliable, and fully offline inventory system.
