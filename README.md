# Surcodex
# Project Requirement: College Coding Practice & Examination Management Platform

## Project Overview

Build a full-stack web application for colleges that enables coding practice, online examinations, performance tracking, ranking systems, and academic management. The platform will support four user roles:

1. Student
2. Teacher
3. Sub Admin (College/HOD Level)
4. Super Admin (Platform Owner)

The system should be scalable, secure, responsive, and suitable for multiple colleges.

---

# 1. Authentication & Registration System

## Landing Page

The homepage should contain:

* Login Button
* Register Button

All other platform features remain locked until login.

When users click Login or Register, they must first choose:

* Student
* Teacher

---

# 2. Student Registration & Verification

### Registration Fields

* Full Name
* Student ID / Roll Number
* Department
* Year of Study
* College Email
* Password
* Confirm Password

### Password Rules

* Minimum 8 characters
* Maximum 20 characters
* At least:

  * 1 uppercase letter
  * 1 lowercase letter
  * 1 special character

### Verification Process

1. Email OTP Verification
2. Student ID Verification

The system must automatically verify the student ID against the college database.

Registration is approved only if:

* OTP verification succeeds
* Student ID exists in the database

### Account Validity

Student account validity depends on academic year:

* 1st Year Student → valid for 4 years
* 2nd Year Student → valid for 3 years
* 3rd Year Student → valid for 2 years
* 4th Year Student → valid until graduation

Only one account can be created per student ID.

---

# 3. Teacher Registration & Verification

### Registration Fields

* Full Name
* Department
* Subject
* College Email
* Password
* Confirm Password

### Verification Process

1. Email OTP Verification
2. Registration Request Generated

After registration:

* Teacher remains in Pending Status
* Request appears in Sub Admin Dashboard

Sub Admin can:

* Approve
* Reject

Only approved teachers can access the platform.

---

# 4. Login & Password Recovery

### Student Login

* Email
* Password

### Teacher Login

* Email
* Password

### Forgot Password

Process:

1. Verify email using OTP
2. Create new password
3. Previous password becomes invalid

---

# 5. Student Dashboard

## Profile Section

* Profile Picture Upload
* Full Name (Non-editable)
* Student ID
* Department
* Academic Year
* Email
* Account Information

### Profile Actions

* View History
* Change Password
* Delete Account

---

## Coding Practice Module

Students can:

* Solve Coding Problems
* Practice Topic-Wise

Examples:

* Arrays
* Linked Lists
* Trees
* Graphs
* Dynamic Programming
* Sorting
* Recursion

Problem Difficulty:

* Easy
* Medium
* Hard

---

## Live Exam & Contest Module

Students can:

* Join Live Exams
* Participate in Coding Contests
* Attempt MCQ Quizzes

Teacher announcements and upcoming exams should appear in dashboard notifications.

---

## Ranking & Reward System

Students earn points for:

* Solving problems
* Participating in contests
* Performing well in exams

### Leaderboard

Weekly Leaderboard:

* Shows Top Students
* Displays ranking and points

Monthly Reset:

* Rankings reset every month
* New competition cycle begins

---

## Student Statistics

### Coding Stats

* Total Problems Solved
* Current Rank
* Total Points
* Current Streak
* Contest Participation Count
* Highest Contest Rank

### Skill Profile

* Strong Topics
* Preferred Programming Language
* Easy/Medium/Hard Breakdown

### Achievement System

Badges such as:

* First Accepted Solution
* 7-Day Streak
* Top 10 Contest Finisher
* DP Master
* Problem Solver

### Activity History

* Submission History
* Contest History
* Join Date

---

# 6. Teacher Dashboard

## Overview

* Total Assigned Students
* Total Problems Created
* Active Contests
* Pending Reviews
* Recent Activities

---

## Problem Management

Teachers can:

* Create Coding Problems
* Edit Problems
* Delete Problems
* Add Test Cases
* Add Tags
* Set Difficulty
* Publish / Unpublish Problems

---

## Quiz Management

Teachers can:

* Create MCQ Quizzes
* Add Sections
* Add Question Banks
* Set Marks
* Set Time Limits

---

## Exam Management

Teachers can create:

### Section-Based Exams

Example:

Section A:

* MCQ Questions

Section B:

* Coding Problems

Section C:

* Subjective Questions (optional future feature)

Features:

* Timer Control
* Start Time
* End Time
* Auto Submission

---

## Student Monitoring

Teachers can:

* Track Student Progress
* View Exam Participation
* View Submission Records
* Send Warnings
* Send Messages

---

## Analytics

* Class Performance
* Weak Topics
* Most Attempted Problems
* Submission Success Rate
* Active vs Inactive Students

---

## Contest Management

Teachers can:

* Create Contests
* Add Problems
* Schedule Start/End Time
* View Rankings
* Announce Winners

---

# 7. Sub Admin Dashboard (College Level)

Typically assigned to:

* HOD
* Department Coordinator
* College Administrator

---

## Teacher Management

* View Pending Teacher Requests
* Verify Teacher Information
* Approve Teacher
* Reject Teacher
* Suspend Teacher
* Remove Teacher

Track:

* Exams Created
* Problems Added
* Activity Statistics

---

## Student Management

View:

* All Students
* Department-wise Students
* Year-wise Students

Features:

* Search
* Filter
* Bulk Import via CSV

---

## College Analytics

* Overall College Performance
* Top Performing Students
* Most Active Teachers
* Department Comparison
* Contest Participation Rate

---

## Notifications

Send announcements to:

* All Teachers
* All Students
* Specific Departments

---

## College Settings

* College Name
* Logo
* Departments
* Academic Year Settings
* Allowed Email Domain

Example:

Only users with:

@college.edu

can register.

---

# 8. Super Admin Dashboard (Platform Owner)

## Platform Monitoring

View:

* Total Students
* Total Teachers
* Total Problems
* Total Exams
* Total Contests
* Server Status
* Last 24 Hour Registrations

---

## Sub Admin Management

* Create Sub Admin
* Assign College
* Reset Password
* Remove Sub Admin
* View Last Login

---

## Security Control

* Login Attempts
* Failed Login Alerts
* Audit Logs
* Ban/Unban Users
* Suspicious Activity Monitoring

---

## Platform Settings

* Platform Name
* College Name
* Logo
* Allowed Email Domains
* Registration Enable/Disable
* Maintenance Mode
* Credits Section

---

## Super Admin Profile

* Profile Picture
* Change Password
* Last Login
* Secret Admin URL
* Platform Owner Badge

---

# Technical Requirements

Frontend:

* Next.js / React
* Tailwind CSS
* Responsive Design

Backend:

* Node.js + Express.js
* REST API

Database:

* PostgreSQL 

Authentication:

* JWT
* OTP Email Verification

Cloud:

* Firebase (optional)
* AWS / Vercel

Other Features:

* Role-Based Access Control (RBAC)
* Real-Time Notifications
* Secure Password Hashing
* Leaderboard System
* Automated Monthly Rank Reset
* Exam Timer System
* Coding Judge Integration (Judge0 API or custom compiler service)

Goal:
Create a complete college-level coding practice, examination, ranking, and academic monitoring platform that supports multiple colleges and thousands of students while maintaining secure authentication, performance tracking, and role-based administration.
