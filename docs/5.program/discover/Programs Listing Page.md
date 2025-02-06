**Product Requirements Document: Programs Listing Page**

**1. Introduction**

**1.1. Purpose**

 This page will be a public-facing page accessible to all website visitors (both logged-in and non-logged-in users). The primary purpose is to present a catalog of available academic programs and encourage exploration.

**1.3. Target Audience**

*   **Prospective Students:** Individuals exploring potential online education programs.
*   **Parents/Guardians:** Assisting potential students in their program search.
*   **General Public:** Visitors curious about the university's academic offerings.
*   **Registered, Non-Enrolled Users:** Users who have a platform account, but haven't enrolled in a program yet.
* **Enrolled Students:** To be able to see the different programs that may have prerequisites.

**2. Goals**
*   **Engagement:** Provide an appealing and visually engaging presentation to encourage exploration.
*   **Information:** Offer sufficient information about each program to inform user decision-making.
*   **Action-Oriented:** Guide users towards taking the next step (viewing program details, applying).

**3. Functional Requirements**

**3.1. Page Structure and Layout**

* The Programs Listing Page shall display a catalog of available academic programs.
* The page shall employ a grid or list layout to present program information.
  * **Prioritization:** A grid layout is recommended for visual appeal and showcasing multiple programs.
  * **Fallback:** A list layout should be available as a fallback if the grid layout is not suitable for the content or number of programs.
* The page should have clear visual hierarchy.
* The page loading time should be optimized for all devices.

**3.2. Program Card Design**

* Each program shall be represented by a "program card."
* Program cards shall display the following information:
    * **Program Title:**  The full, official name of the program.
    * **Thumbnail Image:** A visually appealing and representative image for the program.
    * **Short Description:**  A concise overview of the program, highlighting key features and benefits (approximately 50-100 words).
    * **Category:** The program's category (if categorization is implemented).
    * **Sign-up Status:** Indicate whether the program is open for enrollment (e.g., "Open for Enrollment," "Enrollment Closed," "Coming Soon").
    * **"Learn More" Button:** A clear call-to-action button that links to the program's dedicated details page.
* Program cards shall have interactive hover effects (e.g., slight enlargement, shadow, button color change) to indicate interactivity.

**3.3. Program Categorization (Optional, but Recommended)**

* If program categories are implemented, the page shall provide a mechanism for users to browse programs by category.
* Category browsing options may include:
    * **Top-Level Categories:** Display prominent links or buttons for major program categories at the top of the page.
    * **Expandable/Collapsible Categories:**  Use an expandable/collapsible menu or list to display subcategories within main categories.
    * **Category-Specific Pages:**  Create separate pages for each category, listing programs within that category.
* If not implemented, it must be implemented in phases.

**3.4. Filtering (Optional, but Recommended)**

* If filtering is implemented, the page shall provide filter options to narrow down the displayed programs.
* Potential filter options include:
    * **Program Level:** (e.g., Bachelor's, Master's, Certificate)
    * **Subject Area/Category:** (e.g., Engineering, Business, Humanities)
    * **Start Date:** (e.g., Upcoming Start Dates, Open Enrollment)
    * **Language of Instruction:** (If programs are offered in multiple languages)
* If not implemented, it must be implemented in phases.

**3.5.  Search Functionality:**

* The page shall include a search bar that allows users to search for programs by keywords (title, description, etc.)

**3.6.  Handling of Restricted Programs**

* All programs (including restricted ones) shall be displayed on the Programs Listing Page.
* Restricted programs shall be visually distinguished from unrestricted programs.  Visual indicators may include:
    * A "Restricted" or "Prerequisites Required" label.
    * A grayed-out appearance for the program card.
    * A disabled "Learn More" button.
    * A tooltip on hover explaining the restriction.
* When a user hovers over or clicks on a restricted program card, a clear message shall be displayed explaining the prerequisites or reason for the restriction.

**3.7. Uncategorized Programs**

* If programs are not categorized, all programs shall be displayed in:
    * Alphabetical Order
    * Popularity
    * Program level
    * New to Old

**3.8. User Interaction**

* Clicking the "Learn More" button on a program card shall navigate the user to the program's dedicated details page.
* Clicking on a category (if implemented) shall filter the displayed programs to show only those within that category (or navigate to a category-specific page).
* The search bar shall dynamically update the program listings as the user types.