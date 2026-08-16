---
title: "DealerAdmin: Enterprise Insurance Infrastructure"
date: 2026-03-31

status: "in production"
readTime: "6 min read"

tags:
  - Django
  - DRF
  - Celery
  - Redis
  - Signals
  - LLM Integration
  - AWS

domains: "Insurance, Claims, Payments"
database: "Production backend system"
integrity: "Audit + business rules"

---

## Project Overview

A comprehensive vehicle insurance administrative platform. Over the past year, I have been responsible for maintaining mission-critical features while **spearheading the ongoing migration** of the backend architecture to the latest stable versions of Python and Django.

## Key Engineering Contributions

### // fraud-detection.py

- **Signal-Based Fraud Detection** — Engineered an automated fraud detection layer using **Django Signals** to validate claim photo metadata and system-defined rules immediately upon record creation.

- **Automated Cancellation Review** — Optimized an existing AI-driven verification pipeline by implementing `post_save` signals. This ensures that uploaded cancellation documents are automatically processed by an LLM to verify policy termination criteria.

- **Advanced Prompt Engineering** — Refined LLM prompts and expanded metadata inputs to improve the accuracy and detail of automated policy reviews.

### // background_jobs.py

- **Scalable Reporting** — Leveraged **Celery** to handle asynchronous generation of complex Excel and PDF reports with dynamic filtering, helping maintain a responsive experience for large datasets.

- **Automated System Hygiene** — Implemented **Celery Beat** schedules to automate the deletion of API logs older than 90 days.

### // security_and_audit.py

- **Customizable MFA** — Architected a flexible Two-Factor Authentication system for logins, password resets, and high-value payments, featuring granular user-level controls.

- **Model-Level Audit Logging** — Built a custom logging system to track and record changes within specific database models, supporting insurance audit trails.

- **AWS Messaging** — Integrated AWS Two-Way Messaging for automated system notifications and user verification workflows.

### // notification_engine.py

- **Targeted Announcements** — Developed a role-based notification engine to deliver custom homepage announcements based on user permissions and organizational levels.

## Technical Stack

- **Languages & Frameworks** — Python, Django, Django REST Framework

- **Asynchronous Processing** — Celery, Redis, Celery Beat

- **Cloud & Infrastructure** — AWS SNS, Ubuntu Linux, Gunicorn

- **Quality Assurance** — Django TestCase and SonarQube