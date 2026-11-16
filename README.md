# Reviewing-Unallocated-Space-Extracting-Data-with-Tools-Digital-Investigation-Processes
## AIM:
To review unallocated space in a disk image, extract data using forensic tools, and understand the digital investigation process.
## REQUIREMENTS
- Autopsy or FTK Imager
- Sleuth Kit (TSK)
- Hex Editor (e.g., HxD)
- Operating System: Windows 10/11 or Linux (Kali preferred)
## ARCHITECTURE DIAGRAM
```mermaid
flowchart TD
    A[Disk Image / Physical Drive] --> B[Load into Autopsy or Sleuth Kit]
    B --> C[Identify Unallocated Space]
    C --> D[Scan for Data Signatures]
    D --> E[Carve and Recover Files]
    E --> F[Analyze Recovered Data]
    F --> G[Document Findings in Report]
```
## DESIGN STEPS:
### Step 1 (Acquire Evidence Image):
- Obtain the disk image in ```.dd``` or ```.E01``` format from a trusted forensic acquisition process.
- Verify hash values (MD5/SHA256) to maintain integrity.

### Step 2(Load Image into Forensic Tool):
- Open Autopsy or FTK Imager.
- Create a new case and add the evidence image.

### Step 3(Locate Unallocated Space):
- Navigate to the partition structure view.
- Identify sectors not assigned to any partition (unallocated).
### Step 4(Analyze & Carve Data):
- Use built-in data carving tools to search for file signatures (JPEG, DOCX, PDF, etc.).
- Preview carved files for relevance.
  
## PROGRAM:
| Step | Action                     | Tool Used                   | Output                       |
| ---- | -------------------------- | --------------------------- | ---------------------------- |
| 1    | Load disk image            | Autopsy / FTK Imager        | Partition & unallocated view |
| 2    | Identify unallocated space | Autopsy File System View    | Sector ranges                |
| 3    | Data carving               | Autopsy Data Carving Module | Recovered files              |
| 4    | Export evidence            | Autopsy Export Option       | File copies for analysis     |


## OUTPUT:
Unallocated Space Analysis and Extracted Data Report

<img width="704" height="580" alt="493289057-b6b583df-c3fb-41a0-b32f-3c0a8148a596" src="https://github.com/user-attachments/assets/239d6744-39fd-4bc9-87f8-66bb29327ff9" />
<img width="1340" height="985" alt="493289120-34a70492-aafc-45ea-a5b0-6acb200ea130" src="https://github.com/user-attachments/assets/74eaf85e-a7e0-4291-91af-66908fb4b800" />
<img width="1289" height="494" alt="493289194-a0dcedea-1e3b-4ce3-9c84-5002477f87fa" src="https://github.com/user-attachments/assets/a5c6946b-49da-4c52-a73e-3ed1866b984c" />
<img width="1269" height="643" alt="499675890-351baaee-0966-42b8-8ea6-53f28b0f9f57" src="https://github.com/user-attachments/assets/f7aec43f-edb9-4cd6-8032-dabe22a8809e" />
<img width="1260" height="648" alt="499676049-7cbe3fc4-21a6-4dd9-b0fa-44e6508871be" src="https://github.com/user-attachments/assets/aaae11df-fbf1-4d7a-844c-2b7ac38697ff" />


## RESULT:
The unallocated space was successfully analyzed, data was extracted, and the digital investigation process was followed effectively.

