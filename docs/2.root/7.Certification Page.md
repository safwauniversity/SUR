**Product Requirements Document (PRD): Certification Page**

This page is where students can view, download, share, and, if applicable, verify their earned certificates for completed programs and academic years.

**1.2 Goals**

-   **Professional Presentation:**  Display certificates in a professional and credible manner.
-   **Security and Authenticity:** Ensure the security and authenticity of issued certificates.
-   **Personalization:** Allow students to customize their display name (within acceptable limits) and preferred language. the name can't be changed after certificate issue


**2.  Features**

**2.1 Core Features**

-   **Certificate Listing:** Display a list of all certificates earned by the student.
-   **Certificate Preview:** Show a high-quality visual preview of each certificate.
-   **Certificate Download:** Provide a prominent button to download each certificate as a PDF file.
-   **Certificate Details:**  Display key information for each certificate:
    -   Student's Verified Name (as it appears on the certificate)
    -   Program Name
    -   Academic Year (if applicable)
    -   Completion Date
    -   Issuing Institution (University Name)
    -   Certificate ID (unique identifier)
    -   QR Code linking to a verification page.
-   **Tabbed Interface (if applicable):** Organize certificates using tabs based on:
    -   Program (if the student is enrolled in multiple programs)
    -   Certificate Type (e.g., Academic Year, Program Completion, Abstract Course)

**2.2  Enhanced Features (Optional, Phase 2)**

-   **Social Media Sharing:**  Provide buttons to easily share certificates on professional networking platforms (e.g., LinkedIn) and other social media.
-   **Certificate Verification:**
    -   A system that allows third parties (e.g., employers) to verify the authenticity of a certificate.
    -   This could involve entering a Certificate ID on a verification page.
    -   Or, a QR code on the certificate could link directly to a verification page displaying the certificate details.
- **Blockchain Verification (Optional & Advanced, Phase 2):** Implement blockchain technology to make certificates immutable and easily verfiable

**2.3  Identity Verification (Prerequisite to Certification)**

-   **Name Customization (Limited):**
    -   Allow students to specify their preferred name for display on certificates.
    -   Limit customization to prevent misuse (e.g., prevent completely changing the name).
    -   Support for both Arabic and English names.
-   **Government ID Verification:**
    -   Require students to upload a copy of their government-issued ID (passport, national ID card).
    -   **Verification Options:**
        -   **Manual Verification:**  Admins review uploaded IDs and approve/reject requests.  Consider gender-matched administrators for this process for cultural sensitivity.
        -   **Automated Verification (AI-powered):**  Use AI to analyze uploaded IDs, check for authenticity, and match the name to the student's provided name. This could flag potentially fraudulent uploads for manual review.  *This is a desirable, but potentially advanced, feature.*
-   **Status Indicators:**
    -   Display clear status messages indicating the verification status to the students (e.g., "Pending Verification," "Verification Successful," "Verification Failed - Please Resubmit").
- **Gender-based verification (Optional):**
	- Student will choose gender 
	- Gender matched administrators review

**3. User Interface (UI) Design**

**3.1  Layout and Structure**

-   **Page Title:**  "My Certificates" or "Earned Certificates"
-   **Tabbed Interface (if applicable):**
    -   Tabs are displayed horizontally at the top of the page.
    -   Tab labels are clear and concise (e.g., "[Program Name]," "Academic Year Certificates," "Abstract Course Certificates").
    -   The active tab is visually highlighted.
-   **Certificate Cards:**
    -   Each certificate is presented as a distinct card.
    -   Layout options:
        -   **List View:** Certificates listed vertically, one below the other.
        -   **Grid View:** Certificates arranged in a grid format.  (Suitable if you use high-quality preview images).
    -   Each card includes:
        -   Certificate Preview (thumbnail).
        -   Certificate Details (Name, Program, Date, etc.).
        -   Download Button.
        -   Share Buttons (Optional).
-   **Verification Status:**  Displayed prominently on each certificate card if verification is required (e.g., "Pending Verification").

**3.2 Example Wireframe (List View):**

```
+-----------------------------------------------------+
|                  My Certificates                    |
+-----------------------------------------------------+
|  +----------------+ +-----------------------+      |
|  |  [Program 1]   | | [Abstract Course Certs] |      |  (Tabs)
|  +----------------+ +-----------------------+      |
|                                                     |
| +-------------------------------------------------+ |
| | [Certificate Preview Thumbnail]                  | |
| |  Student Name                                     | |
| |  Program Name: [Program Name]                   | |
| |  Academic Year: [Year]                           | |
| |  Completion Date: [Date]                        | |
| |  Certificate ID: [ID]                            | |
| |                                                 | |
| |  [Download Certificate]  [Share (Optional)]       | |
| +-------------------------------------------------+ |
|                                                     |
| +-------------------------------------------------+ |
| | [Certificate Preview Thumbnail]                  | |
| |  Student Name                                     | |
| |  Program Name: [Program Name]                   | |
| |  Academic Year: [Year]                           | |
| |  Completion Date: [Date]                        | |
| |  Certificate ID: [ID]                            | |
| |  [Verification Status]                           | |
| |  [Download Certificate]  [Share (Optional)]       | |
| +-------------------------------------------------+ |
| (More Certificate Cards)                           |
+-----------------------------------------------------+

```
**4.  User Flows**

**4.1  Viewing Certificates:**

1.  Student logs into the platform.
2.  Student navigates to the "Certification" page (e.g., from their dashboard or user menu).
3.  The page displays a list of the student's earned certificates, organized by tabs (if applicable).
4.  The student can see preview images and details for each certificate.

**4.2 Downloading Certificates:**

1.  Student locates the certificate they want to download.
2.  Student clicks the "Download Certificate" button.
3.  The certificate is downloaded as a PDF file.

**4.3  Sharing Certificates (Optional):**

1.  Student locates the certificate they want to share.
2.  Student clicks the "Share" button.
3.  A menu appears with options to share on different platforms (e.g., LinkedIn, Facebook).
4.  The student selects a platform and follows the prompts to share the certificate.

**4.4  Verifying Certificates (Optional):**

1.  An employer (or other external party) receives a certificate from a student.
2.  The employer navigates to the university's certificate verification page (link provided on the certificate or through a QR code).
3.  The employer enters the Certificate ID (or scans the QR code).
4.  The verification system confirms the authenticity of the certificate and displays the relevant details.

**4.5  Identity Verification Flow:**

1. Student navigates to the profile or settings page, or to a certificate.
2. System prompts the student to verify their identity before a certificate can be issued.
3. Student is instructed to upload a government-issued ID.
4. Student selects their gender.
5. Student uploads the ID.
6. The uploaded ID is reviewed (either manually by a gender-matched administrator or automatically by an AI system).
7. The student is notified of the verification result (Approved, Rejected, Pending).
8. If approved, future certificates will be automatically issued upon completion of requirements.


**6. Technical Requirements**

-   **PDF Generation:**  A robust PDF generation library/service (e.g., iText, Apache PDFBox, jsPDF) to create high-quality, secure certificates.
-   **Multi-language Support:**  Support for Arabic and English, including right-to-left (RTL) layout for Arabic.  Certificates should be rendered in the student's selected language.
-   **Gender Specific**
