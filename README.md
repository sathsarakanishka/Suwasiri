# Suwasiri Ayurvedic Wellness Center — Clinic Management Software

An offline-first local clinic & desktop web application built for **Suwasiri Ayurvedic Wellness Center** (*Natural Healing for a Healthier Tomorrow*).

## Features
- **Patient Registration & Profiles**: Auto-generated Patient IDs (`SW-YYYY-0001`), demographics, contact & emergency details, NIC/Passport, blood group, Ayurvedic **Prakriti** (Dosha constitution), allergies, chronic conditions, and full visit & billing history.
- **Appointments & Daily Queue**: Sequential daily queue tokens (`#01`, `#02`, ...), walk-in and scheduled visits, doctor assignment, status tracking (`Waiting`, `With Doctor`, `Completed`, `Cancelled`, `No Show`), and 1-click transition to billing.
- **Billing, Payments & Printable Receipts**: Consultation fee + Ayurvedic therapies & herbal medicines from inventory, discounts, partial/pending balance settlement, automatic medicine stock deduction, and clean print-ready receipts (`Ctrl+P` / Print Receipt button).
- **Herbal Medicine & Treatment Inventory**: Catalog of Ayurvedic treatments, herbal medicines, and supplements with reorder alerts, expiry tracking, stock adjustments (`Restock`, `Dispense`, `Adjustment`), and movement logs.
- **Staff Accounts & Role Permissions**: Role-based access (`Admin`, `Doctor`, `Receptionist`), clinic receipt settings, and 1-click SQLite database backups.

## Launching on Windows (Desktop App Mode)
1. Double-click **`Suwasiri.bat`** in `d:\Projects\Suwasiri`.
   - Starts the local Node.js + SQLite server on `http://localhost:3456`
   - Opens **Suwasiri** in a standalone desktop application window (via Microsoft Edge / Google Chrome app mode).
2. *(Optional)* Right-click **`Create-Desktop-Shortcut.ps1`** -> **Run with PowerShell** to add a **Suwasiri Clinic** shortcut to the Windows Desktop.

## Starter Staff Accounts
Update each doctor's real name, specialty, and password under **Staff & Settings** after first login:
- **Admin**: `admin` / `admin123`
- **Doctor 1**: `doctor1` / `doctor123`
- **Doctor 2**: `doctor2` / `doctor123`
- **Doctor 3**: `doctor3` / `doctor123`
- **Doctor 4**: `doctor4` / `doctor123`

## Local Database & Backups
- All patient, appointment, inventory, and billing records are stored locally in `data/suwasiri.db`.
- Admins can click **Download DB Backup** inside **Staff & Settings** at any time to save a clean single-file `.db` backup (also saved under `data/backups/`).

## Developer Commands
```bash
npm run install:all   # Install root, server, and client dependencies
npm run dev           # Run Express API + Vite dev server concurrently
npm run typecheck     # Run TypeScript checks on server and client
npm run build         # Build React client and TypeScript server
npm start             # Start production server on http://localhost:3456
```
