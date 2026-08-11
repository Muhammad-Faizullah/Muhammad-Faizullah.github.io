---
title: "DealerAdmin: Enterprise Insurance Infrastructure"
date: 2026-03-31
draft: false
tags: ["Python", "Django", "Django REST Framework", "Celery", "AWS"]
---

### Project Overview
A comprehensive Vehicle Insurance Administrative platform. Over the past year, I have been responsible for maintaining mission-critical features while **spearheading the ongoing migration** of the entire backend architecture to the latest stable versions of Python and Django.

### Key Engineering Contributions

#### 1. Event-Driven AI & Logic Verification
- **Signal-Based Fraud Detection:** Engineered an automated fraud detection layer using **Django Signals** to validate claim photo metadata and system-defined rules immediately upon record creation.
- **Automated Cancellation Review:** Optimized an existing AI-driven verification pipeline by implementing `post_save` signals. This ensures that every uploaded cancellation document is automatically processed by an LLM to verify policy termination criteria.
- **Advanced Prompt Engineering:** Refined LLM prompts and expanded metadata inputs to improve the accuracy and detail of automated policy reviews.

#### 2. Background Processing & Data Engineering
- **Scalable Reporting (Celery):** Leveraged **Celery** to handle asynchronous generation of complex Excel and PDF reports with dynamic filtering, ensuring a high-performance user experience for large datasets.
- **Automated System Hygiene:** Implemented **Celery Beat** schedules to automate the deletion of API logs older than 90 days, maintaining database performance and regulatory compliance.

#### 3. Security & Audit Frameworks
- **Customizable MFA:** Architected a flexible Two-Factor Authentication (2FA) system for logins, password resets, and high-value payments, featuring granular user-level controls.
- **Model-Level Audit Logging:** Built a custom logging system to track and record every change within specific database models, essential for insurance audit trails.
- **AWS Messaging:** Integrated **AWS Two-Way Messaging** for automated system notifications and user verification workflows.

#### 4. UI/UX Backend Logic
- **Targeted Announcements:** Developed a role-based notification engine to deliver custom homepage announcements based on specific user permissions and organizational levels.

### Technical Stack
- **Languages/Frameworks:** Python, Django, Django REST Framework
- **Asynchronous Tools:** Celery, Redis, Celery Beat
- **Cloud & Infrastructure:** AWS SNS (Two-Way Messaging), Ubuntu Linux, Gunicorn
- **Quality Assurance:** Unit Testing (Django TestCase), SonarQube