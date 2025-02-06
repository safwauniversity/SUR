# Online University Management System (OUMS)
Product Requirements Document

## 1. Introduction

### Overview
- Comprehensive web-based platform for a fully online university
- Enhanced functionality beyond traditional LMS
- Manages complete university operations including programs, courses, and administration

### Purpose
- Provide comprehensive platform for online university management
- Deliver seamless learning experience
- Streamline administrative operations
- Support flexible, cohort-based learning
- Enable program visualizations

### Key Features
- **Cohort-Based System:** Students enroll in specific cohorts per program
- **Single Enrollment:** One cohort per program at a time
- **Dynamic Course Creation:** New courses can be added anytime
- **Automatic Cohort Generation:** Created on schedule (e.g., annually)
- **Grade and Certificate Persistence:** Carry over to subsequent cohorts
- **Abstract Courses:** Stand-alone courses available to all users

### Target Audience
- Students: Seeking online education
- Instructors: Content delivery and assessment
- Administrators: System operations management
- Program Controllers: Program management
- Organizations: Content creation and program management

## 2. System Architecture

### Core Components
1. **Learning Management System (LMS)**
   - Enhanced functionality beyond typical LMS
   - Comprehensive course and program management
   - Student progress tracking
   - Interactive content delivery

2. **Program Management System**
   - Multiple faculties/institutes
   - Program categorization
   - Independent program operations
   - Profile-like context switching
   - Program controller functionality

### Content Organization
- **Faculties:** Different departments/subject areas
- **Programs:** Specific courses of study within faculties
- **Main Branch:** Primary curriculum structure template
- **Cohort Branches:** Individual cohort-specific branches
- **Abstract Courses:** Stand-alone courses outside programs

### Database Structure
#### Entities & Relationships
- Faculty → Multiple Main Branches
- Main Branch → Multiple Academic Years
- Academic Year → Multiple Semesters
- Semester → Multiple Courses
- Course → Multiple Lectures/Quizzes
- Student → Multiple Enrollments

## 3. Access Levels & Features

### Public Access
- Homepage
- About Us
- Contact Us
- Programs Listing
- Abstract Courses Listing
- Library (Global Access)
- Login/Signup

### Enrolled Student Access
- Dashboard (Student Hub)
- Course Pages
- Lecture Pages
- Quiz/Assessment Pages
- Grades System
- Certification
- Library (Full Access)
- Live Sessions
- Community Features
- Profile Management

## 4. Detailed Page Structure

### Homepage
- Hero Section
- Featured Programs
- Abstract Course Showcase
- Message from Supervisor
- Social Proof Section
- Newsletter Signup
- Footer

### Dashboard (Student Hub)
- Overview Tab (Welcome, Deadlines, Announcements)
- My Courses Tab
- Calendar Tab
- Messages Tab
- Resources Tab
- Progress Visualization
- Action Notifications

### Course Page
- Overview/Syllabus
- Content Modules
- Sessions
- Instructors
- Grades
- Files
- Discussions

### Learning Components
- Video/Audio Player
- Transcript
- Download Options
- Assessments
- Feedback System
- Comments
- Error Reporting

## 5. Technical Implementation

### Technology Stack
- Backend: Spring Boot with Kotlin
- Frontend: React with TypeScript
- Database: PostgreSQL
- API: GraphQL
- Web interface for all interactions

### Technical Requirements
- Dynamic Content Loading
- Context-Aware Navigation
- Access Control System
- Responsive Design
- Scalability
- Security Implementation
- Performance Optimization
- Data Backup and Recovery
- System Monitoring

### Security & Compliance
- Role-Based Access Control
- Data Protection & Encryption
- Authentication System
- Educational Standards Compliance
- Accessibility Guidelines
- Content Standards

## 6. User Experience & Design

### Visual Design
- Clean, modern interface
- Consistent branding
- Limited color palette
- Clear visual hierarchy
- Responsive layouts

### Navigation & Usability
- Intuitive Navigation
- Clear Context Indicators
- Consistent Layout
- Mobile-Friendly Interface
- Efficient Workflows
- Accessibility Compliance

## 7. Application States & Access Methods

### Program Status States
- Pending
- Approved
- Active
- Failed
- Invited

### Access Methods
- Auto-approval
- Self-application
- Admin approval
- Quiz/exam requirement
- Invite-only access
