# Test Cases – Cybersecurity Asset Inventory System

| # | Feature | Test Description | Input | Expected Output | Result |
|---|---------|------------------|-------|------------------|--------|
| 1 | Add Asset | Add a valid new asset | Asset ID: A104, Name: Finance-PC, Type: Workstation, IP: 192.168.1.30, OS: Windows 10, Dept: Finance, Risk: Low, Status: Secure | "Asset 'A104' added successfully." | Pass |
| 2 | Add Asset | Add asset with duplicate Asset ID | Asset ID: A101 (already exists) | "Error: Asset ID 'A101' already exists." | Pass |
| 3 | Add Asset | Enter invalid Asset Type | Type: "Laptop" | Re-prompts until a valid type (Workstation/Server/Router/Switch/Application) is entered | Pass |
| 4 | Add Asset | Leave Asset Name blank | (empty input) | "This field cannot be empty. Please try again." | Pass |
| 5 | Search Asset | Search by exact Asset ID | "A102" | Displays Web-Server details | Pass |
| 6 | Search Asset | Search by partial Asset Name | "HR" | Displays HR-PC-01 details | Pass |
| 7 | Search Asset | Search for non-existent asset | "Z999" | "No asset found matching 'z999'." | Pass |
| 8 | Update Asset | Update Risk Level of existing asset | Asset ID: A103, new Risk Level: Critical | "Asset 'A103' updated successfully." + Risk Level now shows Critical | Pass |
| 9 | Update Asset | Update non-existent asset | Asset ID: Z999 | "Error: No asset found with ID 'Z999'." | Pass |
| 10 | Update Asset | Leave all fields blank | (press Enter for every field) | All original values retained | Pass |
| 11 | Delete Asset | Delete existing asset with confirmation | Asset ID: A101, confirm: y | "Asset 'A101' deleted successfully." | Pass |
| 12 | Delete Asset | Cancel deletion | Asset ID: A102, confirm: n | "Deletion cancelled." | Pass |
| 13 | Delete Asset | Delete non-existent asset | Asset ID: Z999 | "Error: No asset found with ID 'Z999'." | Pass |
| 14 | Display All | Display with 3 assets loaded | (menu option 5) | Full formatted list + summary counts (Total: 3, Critical: 1, High: 1, Medium: 1, Vulnerable: 1) | Pass |
| 15 | Display All | Display with empty inventory | (menu option 5, no assets) | "No assets to display." + summary shows all zeros | Pass |
| 16 | Security Summary | Report flags Critical/Vulnerable assets | (menu option 6) | Lists A102 under "Assets needing immediate attention" | Pass |
| 17 | Data Persistence | Restart program after adding an asset | Add A104, exit, relaunch program | A104 still present after reopening | Pass |
| 18 | Input Validation | Invalid Risk Level entry | Risk Level: "Extreme" | Re-prompts until Low/Medium/High/Critical entered | Pass |
| 19 | Input Validation | Invalid Security Status entry | Status: "Ok" | Re-prompts until Secure/Warning/Vulnerable entered | Pass |
| 20 | Menu | Invalid main menu choice | "9" | "Invalid choice. Please enter a number from 1 to 7." | Pass |

## How to Run These Tests
1. Run `python src/asset_inventory.py` from the project root.
2. Walk through each row above using the menu options.
3. Compare the program's actual output against the "Expected Output" column.
4. Capture a screenshot of each core feature (add, display, search, update,
   delete, security summary, and one validation re-prompt) and save them
   into the `screenshots/` folder using the required file names.
