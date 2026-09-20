# kaviya-week01
# Cybersecurity Asset Inventory System

A menu-driven Python console application that helps a security
administrator **add, search, update, delete, and display** an
organization's IT assets, classifying each one by asset type, risk
level, and security status.

## Problem Statement
Organizations maintain many IT assets — computers, servers, routers,
switches, and applications. Managing these manually makes it hard to
track their security status and know which ones need urgent
attention. This tool centralizes that tracking in one place.

## Features
- **Add Asset** – enter a new asset with full validation of type, risk
  level, and security status.
- **Search Asset** – look up assets by ID or name (partial match supported).
- **Update Asset** – edit any field of an existing asset; blank fields
  keep their current value.
- **Delete Asset** – remove an asset, with a confirmation prompt.
- **Display All Assets** – view every asset plus a summary of totals
  by risk level and security status.
- **Security Summary Report** – highlights all Critical-risk or
  Vulnerable assets that need immediate attention.
- **Data persistence** – all data is saved to `data/assets.json` and
  reloaded automatically the next time the program runs.
- **Input validation** – Asset Type, Risk Level, and Security Status
  are restricted to their allowed values; empty fields are rejected.

## Project Structure
```
Week-01-Cybersecurity-Asset-Inventory/
│
├── src/
│   └── asset_inventory.py     # Main program
│
├── data/
│   └── assets.json            # Stored asset data
│
├── tests/
│   └── test_cases.md          # Test cases and expected results
│
├── screenshots/                # Screenshots of the program running
│   ├── 01-add-asset.png
│   ├── 02-display-assets.png
│   ├── 03-search-asset.png
│   ├── 04-update-asset.png
│   ├── 05-delete-asset.png
│   ├── 06-security-summary.png
│   └── 07-input-validation.png
│
└── README.md
```

## Asset Fields
| Field | Description |
|---|---|
| Asset ID | Unique identifier for the asset |
| Asset Name | Friendly name of the asset |
| Asset Type | Workstation / Server / Router / Switch / Application |
| IP Address | Network address of the asset |
| Operating System | OS running on the asset |
| Owner/Department | Department responsible for the asset |
| Risk Level | Low / Medium / High / Critical |
| Security Status | Secure / Warning / Vulnerable |

## How to Run
1. Make sure Python 3 is installed (`python --version`).
2. Clone this repository and open a terminal in the project's root folder.
3. Run:
   ```
   python src/asset_inventory.py
   ```
4. Use the on-screen menu (1–7) to manage assets.

## Sample Output
```
=========================================
 CYBERSECURITY ASSET INVENTORY
=========================================
Asset ID     : A101
Asset Name   : HR-PC-01
Asset Type   : Workstation
IP Address   : 192.168.1.10
OS           : Windows 11
Department   : HR
Risk Level   : Medium
Status       : Secure
-----------------------------------------
...
=========================================
Total Assets       : 3
Critical Assets    : 1
High Risk Assets   : 1
Medium Risk Assets : 1
Vulnerable Assets  : 1
=========================================
```

## Testing
See [`tests/test_cases.md`](tests/test_cases.md) for the full list of
test cases covering normal use, edge cases, and input validation.

## Author
Weekly Mini Project – 01, Cybersecurity Asset Inventory System.
