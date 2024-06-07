# ERPNext v15 Preconfigured Installation Guide on Windows Using WSL

This guide will help you install ERPNext v15 on a Windows machine using Windows Subsystem for Linux (WSL).

## Prerequisites

1. **WSL**: Ensure WSL is installed on your Windows machine. If not, you can install it from the Microsoft Store or search for a guide on the internet on how to set up WSL.

## Steps

### 1. Download the File

1. Click on the [Google Drive link](https://drive.google.com/file/d/1PSlsKOUf2cPp-7pnS7xJgA3nb7gBH3pQ/view?usp=drive_link).
2. Download the file and save it.

### 2. Create a Directory for WSL

1. Open File Explorer.
2. Navigate to the `C:` drive.
3. Create a new folder named `WSL`.

### 3. Install ERPNext on WSL Folder

1. Open a terminal (Command Prompt or PowerShell).
2. Run the following command to import the ERPNext image into WSL:

    \`\`\`sh
    wsl.exe --import ERPNext-v15-Ubuntu-24.04 "C:\\WSL\\ERPNext-v15-Ubuntu-24.04" "<path to the downloaded file>"
    \`\`\`

### 4. Configure the Hosts File

1. Open Notepad as an administrator.
2. Open the hosts file located at \`C:\\Windows\\System32\\drivers\\etc\\hosts\`.
3. Add the following line at the end of the file:

    \`\`\`plaintext
    127.0.0.1    test.erpnext.local
    \`\`\`

4. Save the file.

### 5. Access and Setup Default ERPNext Site

1. Open your web browser.
2. Navigate to \`http://test.erpnext.local:8001\`.
3. Log in using the following credentials:
    - **Username**: Administrator
    - **Password**: frappe

## Conclusion

You have successfully installed ERPNext v15 on your Windows machine using WSL. If you encounter any issues or need further assistance, please refer to the official ERPNext documentation or community forums.

The preconfigured file is based on [this GitHub repository](https://github.com/D-codE-Hub/-Frappe-ERPNext-Version-15--in-Ubuntu-24.04-LTS) with additional configurations, such as setting it up as production and using port-based multitenancy.

---

**Note**: All password prompts in the preconfigured image file use "frappe" (e.g., user, MariaDB, administrator).
"""
