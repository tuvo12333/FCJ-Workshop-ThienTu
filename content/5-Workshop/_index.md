---
title: "Workshop"
date: 2024-01-01
weight: 5
chapter: false
pre: " <b> 5. </b> "
---

# AWS Student Management Portal

#### Overview

**AWS Student Management Portal** is a student management system built on a **Serverless architecture on AWS**. 
The system serves three user groups: **Admin, Teacher, and Student**, with clear separation of privileges for account management, academic management, and personal profile lookups.

In this workshop, you will learn how to build, configure, and deploy a complete serverless application on AWS using modern cloud services.

#### Content

1. [Overview & Architecture](5.1-Overview-architecture/)
2. [Prerequisites](5.2-Prerequisite/)
3. [Infrastructure & Database](5.3-Infrastructure-database/)
4. [Backend & API Gateway](5.4-Backend-apigateway/)
5. [Frontend & Hosting](5.5-Frontend-deployment/)
6. [Testing & Clean up](5.6-Testing-cleanup/)

### Live Product URL & Demo Accounts
**Live Web Product URL (CloudFront CDN)**: https://d3th0yl82lu593.cloudfront.net/

# Test Account & Roles

| Role | Login Email | Password | Allowed Functions |
| --- | --- | --- | --- |
| Admin | admin@example.com | Abc12345! | View all functions (including teacher management, logs, accounts). |
| Teacher / Staff | staff@example.com | Abc12345! | View Student, Grades, Study Materials, Profile, Notifications menus. (Hidden Admin and Teacher config). |
| Student | student@example.com | Abc12345! | Only view Overview, Profile, Grades, Study Materials and Notifications menus. (Hidden all other management). |