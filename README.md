Instruction

1. Preparation
  
  1.1 Download the script files to your computer. The easiest way is to click the green "Code" button at the top of this repository page and select "Download ZIP"
  
  1.2 Extract the downloaded archive into a new folder on your computer. (Note: If you see a folder named __MACOSX or files starting with ._ or .DS_Store, simply ignore them. These are invisible macOS system files).
  
  1.3 Prepare your database in a .csv format. You can use the provided test_contacts.csv as a template. The file must strictly contain two columns separated by a comma (no spaces or quotes): cid and email.
  
  1.4 Important note for Excel users (Long CIDs): If your cid values are longer than 11 characters, Excel will automatically convert them into scientific notation (e.g., 1.23E+11), which will corrupt the data. To prevent this, press Ctrl + A to select all cells and change the cell format to "Text" before saving the file.
  
  1.5 Save your prepared database file in the same folder as the scripts. Let's assume you named it input.csv.
  
  1.6 CRITICAL WARNING: Once you have saved the file as input.csv, do not open it again in Excel. Even if you just open it to view the data, Excel will immediately reapply the E+ format to long numbers and silently break your file layout.

2. How to Run on Windows (PowerShell)

  2.1 Open the folder containing the extracted scripts and your input.csv file.
  
  2.2 Click on the address bar at the top of the File Explorer window, type powershell, and press Enter. This will open a command window directly in that folder.
  
  2.3 Type the following command and press Enter: **.\hasher.ps1 .\input.csv**
  
  2.4 Troubleshooting (Script execution error): If you receive a red error message stating that running scripts is disabled on this system, your Windows security settings are blocking the file. To safely bypass this for the current session, run this command instead: **powershell -ExecutionPolicy Bypass -File .\hasher.ps1 .\input.csv**

3. How to Run on macOS (Terminal)

  3.1 Open the Terminal application (you can find it using Spotlight Search)
  
  3.2 Type cd  (make sure to put a space after "cd"). Drag and drop the extracted folder from Finder into the Terminal window, then press Enter.
  
  3.3 Make the bash script executable by running this command: **chmod +x hasher.sh**
  
  3.4 Run the script by specifying your input file: **./hasher.sh input.csv**

4. The Result

  4.1 Once the script finishes processing, a new file named emails_hashed.csv will automatically be generated in the same folder. This file contains your securely hashed data and is completely safe to send to our team.
