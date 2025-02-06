## Product Requirements Document: Quiz Page

**1. Introduction**

**1.1. Purpose**

The Quiz Page is a core component enabling instructors to assess student understanding and students to demonstrate their knowledge.  It supports various quiz types, access controls, and detailed result reporting.

**1.2. Goals**

*   **Versatile Assessment:**  Support different quiz types (module, course, program application, abstract).
*   **Clear Presentation:**  Deliver quiz questions in a user-friendly and accessible format.
*   **Secure and Reliable:**  Enforce quiz rules, time limits, and prevent unauthorized access.


**2.  Functional Requirements**

**2.1. Quiz Types**

The system MUST support the following quiz types:

*   **Module Quiz:** Associated with a specific module within a course.
*   **Course Quiz:**  Covers the content of an entire course.
*   **Program Application Quiz:**  A prerequisite quiz for program enrollment (if applicable).
*   **Abstract Quiz:**  A stand-alone quiz, not tied to a specific course or program.

**2.2. Quiz Access and Display**

*   **2.2.1.  Landing Page (Pre-Quiz):**
    *   The system MUST display a landing page before the quiz starts.
    *   The landing page MUST display:
        *   Quiz title.
        *   Instructions (duration, number of attempts allowed, navigation rules).
        *   Quiz Status:
            *   **Available:**  A "Start Quiz" button MUST be displayed.
            *   **Upcoming:**  The future availability date and time MUST be displayed.
            *   **Past:**  The completion status (e.g., "Completed," "Attempted," "Missed") MUST be displayed.
    *  The system MUST prevent users from accessing the Quiz if it is not "Available".

*   **2.2.2.  Start Confirmation:**
    *   Before starting the quiz, the system MUST display a confirmation dialog.
    *   The confirmation dialog MUST:
        *   Reiterate the time limit (if applicable).
        *   Provide a warning about the duration.
        *   Include "Start" and "Cancel" buttons.

*   **2.2.3. Quiz Interface (During Quiz):**
    *   **Pinned Countdown Timer:**
        *   If the quiz has a time limit, a countdown timer MUST be displayed and pinned to the top of the page.
        *   The timer MUST remain visible while the student scrolls.
    *   **Question Display:**
        *   Questions MUST be displayed clearly with appropriate input mechanisms for each question type (see Section 2.4).
        *    The display SHOULD adapt to each question type.
        *   One question per page design SHOULD be implemented.
    *   **Answer Saving:**
        *   The system MUST automatically save student answers at regular intervals (e.g., every 10 seconds or after each question submission).
        *   The system SHOULD implement logic for Quiz persistence, in case of accidental tab closing.
    *   **Navigation:**
        *   "Previous" and "Next" buttons MUST be provided (unless restricted by quiz settings).
        *   A question navigator panel SHOULD be provided to allow students to jump to specific questions (unless restricted by quiz settings).
    *   **Submit Button:** A "Submit Quiz" button MUST be displayed.

*   **2.2.4. Quiz Submission:**
    *   The system MUST display a confirmation dialog before final submission, warning the student that they cannot make further changes.

*   **2.2.5. Results Page (Post-Quiz):**
    *   **Immediate Results:**  If the quiz is auto-graded, the system MUST display the student's score immediately after submission.
    *   **Delayed Results:**  If the quiz requires manual grading, the system MUST inform the student of the expected date for results.
    *   **Retake Options:** The system MUST display retake options (if allowed by the quiz settings), including the number of remaining attempts.

*   **2.2.6.  Review Interface:**
    *   (If enabled by quiz settings) The system MUST allow students to review the quiz:
        *   Questions.
        *   Their answers.
        *   Correct answers.
        *   Feedback (if provided by the instructor).
    *  The system could have a dedicated date for Quiz results.

**2.3 Quiz Persistence**
    *   If the Quiz is interrupted, refresh or closing. The system MUST save the current state of the Quiz.
    *   The system MUST provide "Resume" Quiz option.

**2.4. Question Types**

The system MUST support, *at minimum*, the following question types:

*   Multiple Choice (single correct answer)
*   Multiple Choice (multiple correct answers)
*   True/False
*   Fill-in-the-Blank
*   Short Answer
* Matching


**3.  Glossary**

*   **Abstract Quiz:**  A quiz not associated with a specific course or program.
*   **Module Quiz:** A quiz associated with a module within a course.
*   **Course Quiz:**  A quiz covering the content over an entire course.
*   **Program Application Quiz** : A Quiz needed as a requirement for enrolling in a specific Program.
*   **WCAG:** Web Content Accessibility Guidelines.
*   **UI** : User Interface.
*   **PRD** : Product Requirements Document.