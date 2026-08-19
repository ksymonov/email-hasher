# Instruction: Data Hashing Script

## 1. Preparation
- Download the script files to your computer. Click the green "Code" button at the top of this repository and select "Download ZIP".
- Extract the downloaded archive into a new folder. (Note: Ignore invisible macOS system files like __MACOSX or .DS_Store).
- Prepare your database in a .csv format using test_contacts.csv as a template. It must strictly contain two columns separated by a comma: cid and email.
- **Important note for Excel users (Long CIDs):** If your cid values are longer than 11 characters, Excel converts them into scientific notation (e.g., 1.23E+11). Press Ctrl + A, change the cell format to "Text" *before* saving.
- Save your prepared database file in the same folder as input.csv.
- ⚠️ **CRITICAL WARNING:** Once saved as input.csv, **do not open it again in Excel**, or it will silently break the formatting again.

---

## 2. How to Run on Windows (PowerShell)
1. Open the folder containing the extracted scripts and your input.csv.
2. Click on the address bar at the top of File Explorer, type `powershell`, and press Enter.
<img width="1280" height="194" alt="photo_1_2026-08-19_12-19-56" src="https://github.com/user-attachments/assets/bb500579-a97a-4db6-9d8b-f40b40073f59" />
<img width="1280" height="202" alt="photo_2_2026-08-19_12-19-56" src="https://github.com/user-attachments/assets/338195be-067d-4d87-ad52-3113af936991" />
<img width="1113" height="625" alt="photo_3_2026-08-19_12-19-56" src="https://github.com/user-attachments/assets/0b0d2f0c-d6e5-41a5-9324-9e25702eb290" />
3. Run the following command:

```powershell
.\hasher.ps1 .\input.csv

```

4. **Troubleshooting (Script execution error):** If execution is disabled by Windows security, run this command instead to bypass it for the current session:

```powershell
powershell -ExecutionPolicy Bypass -File .\hasher.ps1 .\input.csv

```

---

## 3. How to Run on macOS (Terminal)

1. Open the Terminal application.
2. Type `cd ` (with a space after it), drag and drop the extracted folder into Terminal, and press Enter.
3. Make the script executable by running:

```bash
chmod +x hasher.sh

```

4. Run the script:

```bash
./hasher.sh input.csv

```

---

## 4. The Result

Once the script finishes processing, a new file named `emails_hashed.csv` will automatically be generated in the same folder. This file contains your securely hashed data and is completely safe to send to our team.
