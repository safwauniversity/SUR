**Product Requirements Document: Online University Management System - Library Page**

**1. Introduction**

**1.1. Purpose**

This page serves as a central repository for educational resources, supporting both public users and enrolled students.

**1.2. Goals**

*   Provide a user-friendly interface for accessing and managing a wide range of library resources.
*   Offer a clear distinction between publicly accessible resources (Global Library) and program-specific materials.
*   Enable easy searching, browsing, and filtering of library content.
*   Support multiple file formats (primarily PDF) and viewing options.
*   Ensure a secure and reliable platform for resource storage and access.

**1.3 Target Audience**
	•	Public users (not logged in)
	•	Registered Users (Users who have registered and are logged in)
	•	Enrolled Students: (Users who are registered, logged in, and enrolled in a program)

**2. Overall Description**

**2.1. Product Perspective**

The Library Page is an integral component of the larger online university management system. It interacts with other modules, such as:

*  **User Authentication:** To differentiate between public users and enrolled students, controlling access to program-specific resources.
*  **Program Management:** To link resources to specific programs and courses.
*  **Content Management:** For uploading, organizing, and managing library files.

**2.2. Functions**

*   **Resource Downloading:** Users can download resources to their local devices.
*   **Access Control:** The system restricts access to program-specific materials to enrolled students.

**2.3. User Classes and Characteristics**

*   **Public Users (Non-Logged-In):** Can access the Global Library section, browse public resources, view/download permitted files.
*   **Enrolled Students:** Can access all public resources, plus program-specific materials and lectures.
*   **Administrators:** Can manage all aspects of the Library, including uploading, organizing, and categorizing resources.

**3. Specific Requirements**

**3.1. Functional Requirements**

*   **Resource Organization:**
    *   The system shall organize resources into three main categories:
        *       Program-Specific Library: Resources related to specific courses within programs.
        *       Global Library: University-wide resources accessible to all users.
        *       Written Lectures: Lecture notes and materials, organized by academic year, semester, or course.
*  **Public Access:**
    * The system shall allow public users (non-logged-in) to access the Global Library section.
    * Public users shall be able to browse, view, and download permitted global resources.
*   **Student Access:**
    *   Enrolled students shall have access to all public resources plus program-specific resources and lectures.
*   **Search Functionality:**
    *   The system shall provide a search bar to allow users to search for resources by keywords.
*   **Filtering:** (Optional)
        The library may include options to filter by category, popularity, or other relevent attributes.
*   **Resource Viewing:**
    *   The system shall support viewing PDF resources directly within the browser.
    *   An option for an external document viewer (like Google Docs Viewer) should be considered.
*   **Resource Downloading:**
    *   The system shall allow users to download resources.
*   **Resource Display:**
    *  The system MUST use visually distinct "Book Cards".
    *   Book Cards shall display:
        *   Title
        *   Author(s)
        *   Thumbnail Image (optional, but highly recommended).
        *	Short Description (Optional)
        *   View Online Option (If applicable)
        *   Download Button.

**3.2. User Interface Requirements**

*   **Page Layout:**
    *   Clear headings for each section (Program-Specific Library, Global Library, Lecture Notes).
    *       Expandable sections for course-specific resources within the Program-Specific Library.
    *       Expandable sections or categories within the Global Library.
    *   Clear visual separation between sections.

* **Book Card Design:**
    *   Consistent visual style for all book cards.
    *   Clear visual hierarchy (title, author, etc.).
    *  Ample white space and modern design.
    *   Interactive hover effects (card highlighting, description preview).

*   **Accessibility:**
    *   The interface shall adhere to WCAG guidelines (e.g., sufficient contrast, keyboard navigation, screen reader compatibility).

* **Responsiveness:**
    *	The interface shall be responsive and work as intended on all devices.

**3.3. Performance Requirements**

*   **Response Time:** The Library Page shall load within 3 seconds.
*   **Search Speed:** Search results shall be displayed within 2 seconds.
*   **Scalability:** The system shall be able to handle a large number of concurrent users and a growing library of resources.

**3.4. Security Requirements**

*   **Access Control:** The system shall enforce access control to ensure that only authorized users can access program-specific content.
*   **Data Protection:** The system shall protect sensitive data (user information, resource files) from unauthorized access.
*   **Secure Storage:** All resources shall be stored securely.

**4.  Diagram**

```
+----------------------------------------+
|               Library Page             |
+----------------------------------------+
| Welcome to University Library          |
| (Public Access Section) Global Resources|
|   +-----------------------+             |
|   |  Category 1           |             |
|   +-----------------------+             |
|      [Book Card 1]                    |
|      [Book Card 2]                    |
|   +-----------------------+             |
|   |  Category 2           |             |
|   +-----------------------+             |
|      [Book Card 3]                    |
| Program-Specific Library              |
|   +-----------------------+             |
|   |  Course 1             |             |
|   +-----------------------+             |
|      [Book Card 1]                    |
      [Book Card 2]
| Lecture Notes                          |
|   [Academic Year 1] (Expandable)       |      |
|                                        |
| [Login for Full Access]                |
+----------------------------------------+
```
