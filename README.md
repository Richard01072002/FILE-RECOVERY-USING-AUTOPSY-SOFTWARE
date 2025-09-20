# FILE-RECOVERY-USING-AUTOPSY-SOFTWARE

## AIM
To use **Autopsy Digital Forensics Tool** to retrieve deleted files from a disk image.

---

## REQUIREMENTS
- **Operating System**: Windows 10/11, macOS, or Linux
- **Tool**: [Autopsy Digital Forensics](https://www.autopsy.com/)  
- **Test Data**: Disk image file (`disk.dd`, `disk.img`, `.E01`)

---

## ARCHITECTURE DIAGRAM
```mermaid
flowchart TD
    A[Disk Image / Physical Drive] --> B[Install Autopsy]
    B --> C[Create New Case in Autopsy]
    C --> D[Add Data Source: Disk Image]
    D --> E["Run File System & Data Recovery Modules"]
    E --> F[Locate Deleted Files in Results]
    F --> G[Recover and Export Deleted Files]
```
## DESIGN STEPS:
### Step 1:
Open Autopsy and create a new case with appropriate case details.

### Step 2:
Add a disk image as a data source and let Autopsy analyze the content.

### Step 3:
Navigate to the "Deleted Files" section in Autopsy and examine or recover the deleted files.

## PROGRAM:
### Install Autopsy
```bash
# Download Autopsy from:
# https://www.autopsy.com/
# Install following the setup wizard.
```
### Create a New Case
```
# File → New Case
# Enter Case Name: Deleted_File_Recovery
# Choose Base Directory: C:\Cases\Deleted_File_Recovery
# Click Finish
```
### Add Disk Image
```
# Add Data Source → Disk Image or VM File
# Browse to: C:\forensics\disk.dd
# Click Next
```
### Run Ingest Modules
```# Select:
# - File System Analysis
# - Keyword Search (optional)
# - Data Recovery / Carving
# Click Finish
```
### Locate Deleted Files
```
# Navigate to 'Deleted Files' section in the tree view
# Review metadata (size, hash, timestamps)
```
### Export Deleted Files
```
# Right-click → Extract File(s)
# Save to: C:\forensics\Recovered_Files\
```

## OUTPUT:
Recovered Deleted File List and Details
<img width="1712" height="905" alt="Screenshot 2025-09-06 141957" src="https://github.com/user-attachments/assets/99d60513-f667-4f8a-85db-23f55767ad38" />
<img width="1704" height="905" alt="Screenshot 2025-09-06 142143" src="https://github.com/user-attachments/assets/12f1c486-59cf-4425-a323-dd9241df80b1" />
<img width="1673" height="903" alt="Screenshot 2025-09-06 142229" src="https://github.com/user-attachments/assets/04f94df3-7ba4-4a87-851c-c274d50b50af" />

<img width="1916" height="986" alt="image" src="https://github.com/user-attachments/assets/58c25950-1959-4dc8-856d-299562e573e5" />

<img width="882" height="445" alt="Screenshot 2025-09-20 at 1 52 32 PM" src="https://github.com/user-attachments/assets/cd6b63d9-3278-4a3d-bae2-1a76d61db759" />

<img width="1920" height="1014" alt="image" src="https://github.com/user-attachments/assets/738610a8-00b8-465e-89c8-57e5794ff908" />



## RESULT:
Deleted files were successfully retrieved and analyzed using Autopsy.
