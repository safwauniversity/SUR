# Online University Program Site Context

**1. Introduction**

**1.1 Purpose**

 This context is activated when a student, who is already enrolled in at least one program, selects a specific program to interact with.

**1.2 Definitions, Acronyms, and Abbreviations**

*   **Program Context:** The state of the website after a student has selected a specific program.
*   **Global Context:** The state of the website before a student has selected a specific program.
*   **Cohort:** A group of students progressing through a program together, typically starting at the same time.
*   **Academic Year:** A division of a program, typically lasting one year, composed of semesters.
*   **Semester:** A division of an academic year.
*   **Course:** A specific subject within a semester.
*   **Abstract Course:** A stand-alone course not tied to a specific program.
*   **LMS:** Learning Management System.
* **Action Banner**: element that will prompt user to take required action.

**2. Overall Description**

**2.1 Perspective**

The Program Site Context is a self-contained environment within the larger Online University platform. It is the primary interface for a student's interaction with their chosen program. It acts as a deeply integrated LMS, tailored to the specific program's curriculum, structure, and community.

**2.2 Functions**

*   **Program-Specific Navigation:**  Provides a consistent navbar for accessing all program-related pages.
*   **Content Delivery:**  Presents course materials (lectures, readings, quizzes, assignments) in a structured and sequential manner, reflecting the program's curriculum design.
*   **Progress Tracking:**  Allows students to monitor their progress through the program, including course completion, grades, and earned certificates.
*   **Communication & Community:** Facilitates interaction with instructors and peers through live sessions, discussion forums (linked externally via Telegram), and potentially a messaging system.
*   **Assessment & Feedback:**  Provides access to quizzes and assignments, delivers grades, and allows for feedback from instructors.
*   **Resource Management:**  Offers a program-specific library of learning materials.
* **Action Banner/Item Prompt** To encourage user to take action.

**2.3 User Characteristics**

*  The ability to switch between programs (if enrolled in more than one).

**2.4 Operating Environment**

*   **Web-Based:** Accessible via any modern web browser on desktop and mobile devices.
*   **Responsive Design:**  The UI must adapt to different screen sizes and orientations.
*   **Secure Access:** Authenticated access via user login.

**2.5 Design and Implementation Constraints**

*   **Scalability:** The system must be able to handle a large number of programs, courses, students, and content items.
*   **Performance:**  Fast loading times and smooth navigation are essential.
*   **Accessibility:**  Adherence to WCAG (Web Content Accessibility Guidelines) for inclusivity.
*     **Integration with third-party tools, like** Telegram for community discussions.

**3. Specific Requirements**

**3.1 Program Context Entry Point**

*   **Trigger:** A student, already logged in, selects a specific program from:
    *   A "Select Program" dropdown in the global navigation user menu.
    *   A list of enrolled programs on their global dashboard (not detailed here).
*   **Action:** The website transitions to the Program Context, updating the following:
    *   **Navbar:** Replaces the global navbar with the program-specific navbar.
    *   **Page Content:** Loads the program's "Program Home" (see 3.2).
    * **Action Banner Activation**: If user have to take action to complete the program.

**3.2 Program-Specific Navbar**

*   **Elements:**
    *   **[University Logo]:** Links to the *global* homepage (exits program context).
    *   **[Program Name]:**  Clearly displays the name of the selected program.  This is *not* a link.
    *   **Content:** Links to the Content page.
    *   **Assessment/Quiz:**
    *   **Lectures**
    *   **Materials:** Links to page where course materials and resources
    *   **Assignments:**  
    *   **Live Sessions:** Links to the Live Sessions page.
    *   **Grades:** Links to the Grades page.
    *   **Support** Links to support related content.
    *   **Discussion:**
    *   **[Switch Program Icon]:** Displays the switch icon next to the program name
    *   **[Profile Picture]:**  Opens the same user menu as in the global context, but *keeps* the program context active for options like "My Dashboard"
    * **Certification**
    * **Instructors** (optional)

*   **Mobile Behavior:**  Uses a hamburger menu approach.  The [Program Name] and [Switch Program Icon] should remain visible, even when other links are collapsed.

**Diagram:**

```
+-------------------------------------------------------------+
| [Uni Logo] [Program Name] [Switch Icon] [Content] ... [Profile Pic]  |  (Desktop)
+-------------------------------------------------------------+

+---------------------------------------+
| [Uni Logo] [Program Name] [Switch Icon] [Profile Pic] [Hamburger] | (Mobile)
+---------------------------------------+
```
**3.8 Action Banner and Quiz Attempt Persistence:**

*   If a student has required actions, such as selecting a Specialization within a Specialization Set, a visable call-to-action banner should appear. This will disappear when the task is complete.
*    The system will auto save the student's work. If there is an issue with the students pc, on refreshing or logging back in, their work is saved to where they left off.

**3.3 Program Home (within Program Context)**

*   **Purpose:** Serves as the main entry point and overview for the selected program.  This is different from a student's global dashboard.  This is a *program-specific* dashboard.
*   **Name** Student hub
*   **Content:**
    *   **Welcome Message:**  Personalized welcome (e.g., "Welcome to the [Program Name] Program, [Student Name]!").
    *   **Program Progress:**  A prominent visual representation of the student's overall progress through the program (percentage completed, years/semesters remaining).
    *   **Upcoming Deadlines:**  A list or calendar view of upcoming assignments, quizzes, and live sessions within the program.
    *   **Recent Announcements:** Displays program-level announcements (not course-specific).
    *   **Action Items:**  A dedicated section highlighting any required actions the student needs to take (e.g., "Choose your specialization," "Select your elective courses").
    *    **Recent Activity:**  Shows recent actions (e.g.,  "You completed Lecture 'Introduction to...' in Course 'X'").
    *   **Featured Abstract Course Widget (Optional):**  Displays a *relevant* abstract course that might be of interest to students in this program.

**Diagram:**

```
+------------------------------------------+
|        Program Home (Student Hub)       |
+------------------------------------------+
|  Welcome Message                         |
|  Program Progress Bar                   |
|                                          |
|  Upcoming Deadlines                      |
|  Recent Announcements                    |
|                                          |
|  Action Items                            |
|                                          |
|  Recent Activity                        |
|  Featured Abstract Course (Optional)    |
+------------------------------------------+
```

**3.4 Content Page**

*   **Purpose:**  Provides access to all learning materials for the program, organized according to the program's structure.
*   **Structure:**
*   **Nested Tabs:**
        *   **[Academic Year Tabs]:**  Top-level tabs for each academic year of the program (e.g., "Year 1," "Year 2").
        *   **[Semester Tabs]:**  Nested tabs within each year for the corresponding semesters (e.g., "Semester 1," "Semester 2").

    *   **Course Cards:**  Within each semester tab, display "Course Cards" representing individual courses within that semester. 
    * **Lecture Card** Contains, title, desc, content.
*   **Course Card Content:** 
    *   Course Name:  Clearly displayed.
    *   Thumbnail Image:  (Optional) An image representing the course.
    *   Instructor: (Optional) Name of Course Instructor.
    *   Progress Indicator:  A visual indicator (e.g., a progress bar) showing the student's completion status for the course. 
    *   "Continue Learning" Button/Link:  Takes the student to the Course Page for that specific course.

*  **Dynamic Content:**
    *   *Only* shows years/semesters/courses relevant to the student's current progress and cohort. For example, a first-year student in their first semester will only see Year 1, Semester 1, and the courses within that semester.
    *   Completed years/semesters/courses remain accessible for review, but are visually distinguished (e.g., grayed out, with a checkmark icon).
    *   Future years/semesters/courses are *not* visible until the student meets the prerequisites.
*  **Exclusive Course Handling** If the semester have the choice based exclusive courses option, the page will only display to the students, the course they haev selected.

**Diagram:**

```
+--------------------------------------------+
|               Content Page                 |
+--------------------------------------------+
|  +----------+ +----------+ +----------+    |
|  | Year 1   | | Year 2   | | Year 3   |    |  <-- Academic Year Tabs
|  +----------+ +----------+ +----------+    |
|                                            |
|   +-------------+ +-------------+         |
|   | Semester 1  | | Semester 2  |         |  <-- Semester Tabs (within Year 1)
|   +-------------+ +-------------+         |
|     [Course Card 1]                       |
|     [Course Card 2]                       |
|     [Course Card 3]                       |
|     (Courses for the selected semester)    |
|                                            |
+--------------------------------------------+
```

**3.5 Grades Page**

*   **Purpose:**  Displays the student's grades within the selected program.
*   **Structure:**
    *   **Overall Program Grade:**  Displayed at the top, showing the cumulative grade across all completed courses.
    *   **Expandable Sections:**
        *   **Academic Year:** Top-level expandable sections for each year.
        *   **Semester:** Nested sections within each year, showing semester grades.
        *   **Course:**  Individual course grades within each semester.
    * **Abstract Course Grades:**  (If applicable)  A *separate* section at the bottom of the page showing grades for any *completed* abstract courses.

*   **Grade Display:**
    *   Numerical grade or letter grade (as defined by the university).
    *   Progress bar or visual representation of the grade.
    *   Optional:  Grade distribution (histogram/chart) showing how the student's grade compares to others.

**Diagram:** See previous extensive Grades Page document for a full visualization.

**3.6 Certification Page**

*   **Purpose:** Allows students to access and manage their earned certificates.
*   **Content:**
    *   **Tabs:**
        *   **[Academic Year 1 Certificate]:**  A tab for each completed academic year that grants a certificate.
        *   **[Program Certificate]:** A tab for the overall program completion certificate.
        * **Abstract courses:** A tab that will contain the certificate if relevent for each completed abstract course.
    *   **Certificate Preview:**  Displays a preview image of the certificate.
    *   **Download Button:**  Allows the student to download a PDF version.
    *   **Share Buttons (Optional):**  Buttons to share the certificate on social media.
    *   **Verification Link/QR Code (Optional):** A link for verification against a database.

**Diagram:** See the extensive Certification Page document for a full visualization.

**3.7 Library Page (Program-Specific)**

*   **Purpose:** Provides access to learning resources tailored to the selected program.
*   **Content:**
    *   **Program-Specific Section:**
        *   **Heading:**  [Program Name] Library.
        *   **Organization:**  Resources organized by courses within the program.  Use expandable sections for each course.
    *   **Global Resources Section:**
        *   **Heading:**  University Library or General Resources.
        *   **Organization:** Resources categorized by subject, topic, or type.
    *   **Written Lectures Section** (if applicable)
    * **Search Component:** allow the user to be able find book/material they arelooking for, in bothe the program context and globally.

**3.8 Live Sessions Page**

*   **Purpose:**  Displays upcoming and past live sessions for the selected program.
*   **"Current Session" Tab:** *Only appears if a live session is in progress*.  Provides a direct link to join the session and shows basic session details.
*   **"Past & Upcoming Sessions" Tab:**
    *   **Calendar View:**  An interactive calendar showing scheduled sessions.
    *   **Past Sessions List:** 
        * Expandable cards for each past session.
        * Expanded card contains a video player with the session recording.
    *   **Upcoming Sessions List:**
        * Cards displaying title, instructor, date, time, and duration.
        * "Join Session" button (appears at start time).
    * **Missed Sessions**

**Diagram:** See the extensive Live Sessions Page documents for a full visualization.

**3.9 User Profile Page**

* **Purpose:** Allow students to edit their name (used for certifications) and other details.

**3.10 Account Settings Page**
* **Purpose:** Provide account setting management.
* **Content:**
    - Account details (change password, email, etc.). 
    - Sign out
    - Privacy controls

