## Product Requirements Document: Student Hub (Dashboard)

**1. Introduction**

**1.1. Overview**

The Student Hub provides immediate access to key information, resources, and actions related to their enrolled program(s) and courses.

**1.2. Goals**

*   **Centralized Information:**  Provide a single point of access for crucial student information.
*   **Personalization:**  Tailor content and actions based on the student's enrollment, progress, and program context.
*   **Action-Oriented:**  Highlight important tasks, deadlines, and notifications.
*   **Engagement:**  Promote student engagement and motivation through informative and interactive elements.
*   **Efficiency:**  Streamline access to frequently used resources and features.


**2.  Functional Requirements**

**2.1. Core Components**

*   **2.1.1.  Welcome Message:**
    *   Personalized greeting (e.g., "Welcome back, [Student Name]").
    *   Optional: Rotating motivational quotes or messages from university supervisors.

*   **2.1.2.  Calendar:**
    *   **Interactive:**  Monthly, weekly, or agenda views.
    *   **Event Display:** 
        *   Upcoming quizzes.
        *   Assignments.
        *   Live session dates/times.
        *   Program events.
        *   Deadlines.
    *   **Color-Coding:**  Differentiate event types.
    *   **Event Details:**  Tooltips or click actions to view event details.

*   **2.1.4.  Recent Activity:**
    *   **Feed/List:**  Chronological display of recent student actions:
        *   Completed assignments.
        *   Quiz submissions.
        *   Forum posts (if applicable).
        *   Accessed course materials.
        *   New announcements
    *   **Links:**  Direct links to the relevant activity/content.

*   **2.1.5.  Announcements:**
    *   **Display:**  List of recent program/course announcements.
    *   **Source:**  From program administrators and instructors.
    *   **Filtering (Optional):**  By course or importance.
    *   **Mark as Read/Unread:** Capability.

* **2.1.6 Action Banners(Action Items):**
    * **Purpose:**  Highlight *required actions* for the student.
    * **Triggered By:**
        *  Need to choose a specialization from a set.
        *  Need to select a course from an exclusive course set.
        * Pending program application approval.
        * Other enrollment of program pending state based actions.
    * **Visual Design:**  Rectangular, prominent banner at the top of the Student Hub (or within the relevant section).
    * **Content:**
        *  Clear message explaining the required action.
        *  Call-to-action button linking directly to the relevant page/action.

**2.2. Additional Features**

* **Cross Program Content Display:**
  * **Purpose**: Provide a dedicated display module to showcase 'Abstract courses.'
  * **Functionality**: This module should include a visual carousel or grid that cycles through available abstract courses.
  * **Content**: Each course card should contain:
    * **Course Image:** A relevant image representing the course.
    * **Title:** The name of the abstract course.
    * **Short Description:** A concise overview of the course content.
    * **"Learn More" Button:** A button that redirects users to the course details page.
    * **Filtering:** Students can filter courses by category or topic of interest.
    * **Sorting:** Options to sort courses (e.g., by popularity, date, rating)
*   **Exam/Quiz Persistence:**  If a student exits a quiz/exam before submitting, save their progress and allow them to resume from where they left off (within the time limit). Includes:
     * **Save Progress:** The system should automatically save the student's answers and progress at regular intervals during the exam/quiz.
  - **Notification:** Upon re-entering the website, the student should be notified that they have an incomplete exam/quiz attempt.
  - **Resume Option:** Provide an option for the student to resume their previous attempt.
  - **Time Limit:** The system should track the remaining time for the exam/quiz, ensuring that the time limit is still enforced.

**3.  User Scenarios**

*   **6.1. Checking Upcoming Deadlines:** A student logs into the Student Hub to quickly see if any assignments are due soon.
*   **6.2. Accessing Course Materials:**  A student navigates to the relevant course materials from the hub.
*   **6.3.  Viewing Announcements:**  A student checks the announcements section for updates from their instructors.
*   **6.4. Resuming a Quiz:** A student accidentally closed their browser during a quiz. They log back in, receive a notification about the incomplete attempt, and resume the quiz from where they left off.
*  **6.5 Choosing a Specilization:** A student need to choose specialization from available options and he gets notification Action Banner.
:** Efficient loading and rendering of content for the 'Abstract courses' section.
