# Homepage

## 1. Introduction

## 2. Goals

*   **Attract prospective students:** Present a compelling and informative overview of the online university.
*   **Communicate Value Proposition:** Clearly explain the benefits of the university's offerings (e.g., cohort-based learning, expert instructors, flexible online platform).
*   **Highlight Programs & Courses:** Showcase key programs and abstract (open) courses to encourage exploration.
*   **Drive User Action:** Guide users towards desired actions (e.g., signing up, exploring programs, enrolling in courses).
*   **Build Trust:** Establish credibility and convey the quality of the educational experience.

## 3. Target Audience

The homepage caters to multiple user types:

*   **Public Users:** Visitors who are not logged in and have no existing account.
*   **Registered Users:** Users who have created an account but are not yet enrolled in a program.
*   **Enrolled Students (Global Context):** Logged-in students who have *not* selected a specific program context. (Enrolled students *within* a program context will primarily use their dashboard, not the global homepage).

## 4. Release Criteria

*   The homepage is fully responsive and displays correctly on various screen sizes (desktop, tablet, mobile).
*   All content is dynamically loaded and up to date.
*   The homepage is visually appealing and aligns with the university's branding.

## 5. Design and Functionality

### 5.1. Global Elements (present regardless of user state)

*   **Header:**
    *   **Logo:** University logo, linked to the homepage. (Start Alignment)
    *   **Navigation Bar (Navbar):**
        *   **Links:**
            *   Home (links to homepage)
            *   Programs (links to Program Listing page)
            *   Open Courses (links to Abstract Courses Listing page)
            *   Library (links to global library section)
            *   About Us (links to About page)
            *   Contact Us (links to Contact page)
        *   **Search Icon:** Opens a search bar for site-wide content search (Implementation TBD - Phase 2).
        *   **Language Switcher:** Dropdown to select website language.
        *  **Theme Switcher:** Toggle between light and dark themes.
    *   **Authentication:**
        *   **Public Users:** "Login" and "Sign Up" buttons.
        *   **Registered/Enrolled Users:** Profile picture (or generic user icon) that opens a dropdown user menu.
            *   **User Menu:**
                *   My Profile
                *   My Dashboard (only visible to enrolled students)
                *   Switch Program (only visible to students enrolled in multiple programs—icon similar to Facebook's profile switch icon)
                *   Settings
                *   Logout

*   **Footer:**
    *   **Copyright Notice:** "© [Year] [Safwa University]. All Rights Reserved."
    *   **Quick Links:** "About Us," "Contact Us," "Privacy Policy," "Terms of Service."
    *   **Social Media Icons:** Links to the university's social media profiles.

### 5.2. Homepage Content (for Public and Registered Users)

*   **5.2.1. Hero Section:**
*  **Purpose:** Dynamic, engaging content to capture user attention and encourage exploration.
    *   **Background:** High-quality image or video showcasing the online learning experience, student success stories, or a relevant abstract visual.
    *   **Headline:** Concise, impactful message communicating the university's core value proposition.
    *   **Subheading:** Brief explanation expanding on the headline and introducing the cohort model.
        *   Example: "Experience a structured, collaborative, and supportive learning journey with our cohort-based online programs."
    *   **Call-to-Action Buttons:**
        *   Primary Button: "Explore Programs" (links to Programs Listing page)
        *   Secondary Button: "Sign Up" (links to account creation page)

*   **5.2.2. Featured Programs Section:**
    *   **Heading:** "Explore Our Top Programs" (or similar)
    *   **Layout:** Grid layout (3–4 program cards per row)
    *   **Program Card Design:**
        *   **Thumbnail Image:** Visually engaging image representing the program.
        *   **Program Name:** Clear and concise program title.
        *   **Short Description:** Highlights key features and benefits.
        *   **"Learn More" Button:** Links to the program details page.

*   **5.2.4. Abstract Course Showcase:**
    *   **Heading:** "Discover Open Courses" (or similar)
    *   **Subheading (Optional):** "Start learning today with our free, accessible courses."
    *   **Layout:** Carousel or smaller grid (2–3 course cards per row)
    *   **Course Card Design:**
        *   **Thumbnail Image:** Visually appealing image representing the course.
        *   **Course Title:** Clear and concise course title.
        *   **Short Description:** Brief overview of the course content.
        *   **Instructor Name (Optional):**
        *   **"Enroll Now" Button:** Links to the course enrollment page.

* **5.2.5.  Message from the Supervisor (Optional):**
    * **Heading:** "A Message from Our Supervisor" (or similar)
    * **Content:** A brief, welcoming message from a university leader (e.g., President, Dean, Supervisor) highlighting the institution's mission, values, and commitment to providing a quality online education.
    * **Visual:** Include a professional photo of the supervisor.

*   **5.2.6. Social Proof Section:**
    *   **Purpose:** Build trust and demonstrate the value of the university.
    *   **Content Options (Choose one or a combination):**
        *   **Testimonial Slider:** Display rotating quotes from satisfied students or graduates, including their name and (optionally) photo.
        *   **Statistics:** Showcase key metrics (e.g., "Over 10,000 students enrolled," "95% program completion rate").

*   **5.2.7. Call to Action Section:**
    *   **Newsletter Signup:**
        *   **Heading:** "Stay Informed" (or similar)
        *   **Text:** "Subscribe to our newsletter for updates on new programs, courses, and university news."
        *   **Input Field:** Email address input field.
        *   **Button:**  "Subscribe"

### 5.3. Homepage Content (for Enrolled Students - *Global Context*)

*   **Same as 5.2:** The homepage content will *remain the same* for enrolled students who are *not* in a specific program context.  This ensures consistent messaging and promotion of other programs and resources.  Enrolled students will primarily use their dashboard after selecting a program.

## 6.  UI Design Considerations

*   **Visual Appeal:** The homepage should be visually appealing and engaging, using high-quality images, graphics, and a modern design aesthetic.
*   **Branding:** The design should consistently align with the university's branding (logo, colors, fonts).
*   **Mobile Responsiveness:** The homepage MUST be fully responsive, adapting seamlessly to different screen sizes (desktops, tablets, and smartphones).
*   **Accessibility:** The design MUST adhere to WCAG 2.1 AA guidelines to ensure accessibility for users with disabilities, including:
    *   Sufficient color contrast between text and background.
    *   Alternative text for all images.
    *   Proper heading structure for screen reader compatibility.
*   **Page Load Speed:** Optimize the homepage for fast loading times to provide a positive user experience.  Minimize image sizes, leverage browser caching, and use efficient code.

## 7.  Technical Requirements

*   **Dynamic Content:** The homepage should dynamically load content based on the user's login and enrollment status.

## 9.  Success Metrics (Additional, Phase 2)

*   **Website Traffic:** Track the number of visitors to the homepage.
*   **Bounce Rate:** Monitor the percentage of visitors who leave the homepage without interacting further.
*   **Click-Through Rate (CTR):** Measure the CTR on key elements like program cards, course cards, and call-to-action buttons.
*   **Sign-Up Rate:** Track the number of users who create an account through the homepage.
*   **Program Exploration Rate:** Monitor how many users navigate from the homepage to the Program Listing or individual program pages.