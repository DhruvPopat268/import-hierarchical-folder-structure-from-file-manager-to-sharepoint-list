# import-hierarchical-folder-structure-from-file-manager-to-sharepoint-list

# SharePoint Online Document Library Automation

## Overview

This PowerShell script automates the creation of a *SharePoint Online Document Library, generates a **hierarchical folder structure, and uploads **PDF files* from a local directory.

## Features

- ✅ *Creates a Document Library* in SharePoint (if not already present).
- ✅ *Adds custom columns* (FolderCount, PageCount).
- ✅ *Renames the 'Title' column* to 'Name'.
- ✅ *Recursively creates folders* in SharePoint to match the local folder structure.
- ✅ *Uploads PDF files* inside their respective SharePoint folders.

## Prerequisites

### 1. Install PnP PowerShell

If not already installed, run the following command in PowerShell:

powershell
Install-Module -Name PnP.PowerShell -Scope CurrentUser -Force


### 2. Set Execution Policy (if restricted)

Enable running PowerShell scripts using:

powershell
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser


### 3. Required Permissions

Ensure you have *Admin or Owner access* to the SharePoint site.

## Configuration

Before running the script, update the following variables in the script:

powershell
$siteUrl = "https://yourtenant.sharepoint.com/sites/YourSite"
$libraryName = "YourLibraryName"
$libraryDisplayName = "Your Library Display Name"
$localPath = "C:\Your\Local\Path"


Ensure that $localPath is correctly set to your *local folder path* containing the files.

## Usage

### 1. Open PowerShell as Administrator.

### 2. Run the script:

powershell
.\YourScriptName.ps1


### 3. Authenticate with SharePoint.

The script will:

- Connect to SharePoint.
- Create the document library (if missing).
- Add required columns and rename the Title field.
- Create the entire folder structure.
- Upload all PDF files to their respective folders.

## Expected Output

The script will display logs similar to this:


Creating document library: Custom Document Library...
Document library 'Custom Document Library' already exists.
Adding custom columns...
Renaming 'Title' column to 'Name'...
Creating folder in SharePoint: A1/B1/C1
Uploading file: Example.pdf to CustomDocumentLibrary/A1/B1/C1
Process completed successfully!


## Troubleshooting

### ❌ Error: "Access Denied"

🔹 Ensure you have *Owner/Admin permissions* in SharePoint.

### ❌ Error: "File Not Found"

🔹 Check that your $localPath is correct and contains folders/files.

### ❌ Error: "Module Not Found"

🔹 Run Install-Module -Name PnP.PowerShell to install the required module.

## Author

📌 *Created by:* [Your Name]\
📌 *Last Updated:* [Date]

---

✅ **Now just copy-paste this file as ****README.md**** in your project!** 🚀

thank you
