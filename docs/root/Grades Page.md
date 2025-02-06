# Product Requirements Document: Grades Page

**1. Introduction**

**1.1. Purpose**
The Grades page is a crucial component for students, providing a comprehensive and transparent view of their academic performance across different levels (program, academic year, semester, and course).


**2. Goals**

*   **Transparency:** Provide students with a clear and understandable view of their grades and how they are calculated.
*   **Accessibility:** Make grade information easily accessible and navigable.
*   **Comprehensiveness:** Display grades at multiple levels (program, year, semester, course).
*   **Visual Appeal:**  Present grade information in a visually appealing and modern way.
*   **Actionable Insights:** (Optional) Provide insights into student performance and areas for improvement.

**3. Overall Description**

**3.1. Features**

*   **Hierarchical Grade Display:** Grades are organized in a nested structure: Program > Academic Year > Semester > Course.
*   **Expandable/Collapsible Sections:** Users can expand or collapse sections (academic years, semesters) to view more or less detail.
*   **Overall Program Grade:** Displays the student's cumulative grade for the entire program.
*   **Academic Year Grade:** Shows the overall grade for each academic year.
*   **Semester Grade:**  Displays the overall grade for each semester.
*   **Course Grades:**  Shows the final grade for each individual course.
*   **Grade Visualization:**  Uses progress bars or other visual elements to represent grades.
*   **Grade Distribution (Optional):** Displays a histogram or bar chart showing the grade distribution for a course.
*   **Pass/Fail Indicator:** Clearly indicates whether the student has passed or failed a course/semester.
*   **Student Performance Insights (Optional):**  Leverages AI to provide personalized feedback on grade trends.
*   **Additional Statistics (Optional):**  Includes data like completion rate, time spent on learning, assessment difficulty.


**4. User Interface Requirements**

*   **Navigation:**  The page should be accessible from the main navigation menu within the program context (e.g., a "Grades" link in the program-specific navbar).


**5. System Features**

**5.1. Hierarchical Grade Display**

*   **Description:**  The Grades page displays grades in a hierarchical structure, mirroring the program structure.
*   **Details:**
    *   The highest level is the overall program grade.
    *   Below that, grades are organized by academic year.
    *   Within each academic year, grades are further broken down by semester.
    *   Finally, within each semester, grades are displayed for individual courses taken during that semester.
*   **UI:**  Use expandable/collapsible sections to represent the hierarchy.  The user can expand an academic year to see semesters, and expand a semester to see courses.
* **Example:**
```
Grade Book:
	Program Grade: B+   [Progress Bar]
	+ Academic Year 2023-2024
		- Year Grade: A-  [Progress Bar]
		+ Semester 1
			-Semester Grade : A-
			-Course 1: Introduction to Programming:  A [Progress Bar]
			-Course 2:  Calculus I: B+ [Progress Bar]
		+ Semester 2
			-Semester Grade : B
			-Course 3: Data Structures:  B [Progress Bar]
			-Course 4:  Linear Algebra: C+ [Progress Bar]
	+ Academic Year 2024-2025

* **6.2. Expandable/Collapsible Sections**

*   **Description:**  Academic years and semesters are displayed as expandable and collapsible sections.
*   **Details:**
    *   Initially, academic years are displayed in a collapsed state, showing only the year (e.g., "Academic Year 2023-2024").
    *   When a user clicks to expand an academic year, the semesters within that year are revealed.
    *   When a user expands a semester, the courses and their respective grades are displayed.
*   **UI:** Use standard UI elements such as "+" and "-" icons or chevrons to indicate expand/collapse functionality. Implement smooth animations for expanding and collapsing sections.

**6.3. Grade Visualization**

*   **Description:** Grades are represented visually using progress bars.
*   **Details:**
    *   Each numeric grade is displayed alongside a progress bar that visually indicates the grade relative to the maximum possible grade.
    *   Color-coding is used to provide additional visual cues:
        *   Green: Represents high grades (e.g., A, A-)
        *   Yellow: Represents average grades (e.g., B+, B, B-, C+)
        *   Red: Represents low or failing grades (e.g., C, D, F)
*   **UI:**
* Use visually distinct progress bars. Examples for B+ grade

```
[=====-----] 78% B+ (Yellow)
[==========] 100% B+ (Green)

```

**6.4. Grade Distribution (Admins only)**

*   **Description:**  Provides a visual representation of the grade distribution for a course.
*   **Details:**
    *   A histogram or bar chart is displayed, showing the frequency of each grade (e.g., how many students received an A, how many received a B, etc.).
    *   The student's own grade is highlighted on the distribution chart.
    *   The percentile ranking of the student's grade is displayed (e.g., "Top 30%").
*   **UI:**
* Example for a C+ grade in a course.

```
Grade Distribution:
  A: [====      ] 20%
  B: [========  ] 40%
  C: [=====     ] 25%  <-- Your Grade (Highlighted)
  D: [==        ] 10%
  F: [          ] 5%

Your Percentile: Top 75%
```

**6.5. Pass/Fail Indicator**

*   **Description:** Provides a clear indication of whether the student passed or failed the course.
*   **Details:** Use a checkmark (✓) for passing and an X (✗) or other suitable icon for failing grades. Color-coding is applied.
*   **UI:**
* Examples

```
Course 1:  A [Progress Bar] (✓ Green)
Course 2:  F [Progress Bar] (✗ Red)
```

**6.6. Student Performance Insights (Optional)**

*   **Description:**  Uses AI to analyze grade trends and provide personalized feedback.
*   **Details:**
    *   Analyze grade trends over time (e.g., declining performance in a particular subject).
    *   Identify areas where the student is excelling and areas where they may need improvement.
    *   Generate personalized recommendations (e.g., "Consider reviewing the materials for Module 3," "Your performance in quizzes is consistently high").
*   **UI:** Display the AI-generated insights in a clear and concise format, possibly in a separate panel or using tooltips.

**6.7 Abstract Course Grades**
* Description: A distinct section is added for comprehensive display and management of grades earned from abstract courses.

* Details:
    * Clear division, ensuring that students can quickly distinguish between grades from academic program courses and those from abstract courses.
    * Visually set apart from mandatory academic courses, possibly with a specific labeled heading, such as "
       "Abstract Courses Grades.”".
     *  The section might include a progress bar, providing a visual indication of a student’s performance and progression in the course.
    * A clear visual indicator (such as a checkmark or a colored highlight) is displayed for completed courses. Example for a UI.

```
Grade Book:
   Program Grade: B+   [Progress Bar]
   + Academic Year 2023-2024
	...
   Abstract Courses:
   - Course 1:  A [Progress Bar] (✓ Green)
   - Course 2:  F [Progress Bar] (✗ Red)
```
**6.8. Additional Statistics (Admin, Phase 2)**

*   **Description:**  Displays additional statistics related to student performance.
*   **Details:**
    *   Completion rate: Percentage of courses completed.
    *   Time spent on learning:  Total time spent accessing course materials.
    *   Assessment difficulty indicators: Aggregate data on how other students are performing on assessments.
*   **UI:** Use concise labels and clear visual representations (e.g., charts, icons).


**7. Future Enhancements (Out of Scope for this Release)**

*   Downloadable Grade Reports:  Allow students to download a PDF report of their grades.
*   Integration with Learning Analytics Dashboards:  Provide instructors with insights into student performance trends.