# IAM-Lab

# Lab: Introduction to AWS Identity and Access Management (IAM)

**Lab ID:** SPL-66  |  **Version:** 3.1.21  
**Duration:** 2 hours  |  **Platform:** AWS Skill Builder – Builder Labs  
**Date Completed:** Nov 2025  

---

## 🎯 Lab Overview
AWS Identity and Access Management (IAM) enables centralized control of user identities, permissions, and credentials within AWS.  
In this lab, you explore existing IAM users and groups, attach and review managed policies, and verify permissions through real sign-ins.

---

## 🧠 Topics Covered
- Managing IAM users, groups, and policies  
- Exploring managed vs inline policies  
- Understanding *Effect*, *Action*, and *Resource* in JSON policy syntax  
- Using IAM Sign-in URLs for federated user access testing  
- Testing least-privilege permissions in real scenarios  

---

## 🧩 Tasks

### **Task 1: Explore Users and Groups**
- Reviewed pre-created users (`user-1`, `user-2`, `user-3`) and groups (`EC2-Admin`, `EC2-Support`, `S3-Support`).
- Inspected **AmazonEC2ReadOnlyAccess** and **AmazonS3ReadOnlyAccess** managed policies.  
- Compared with **EC2-Admin-Policy**, an inline policy allowing `Describe`, `Start`, `Stop` EC2 instances.

### **Task 2: Add Users to Groups**
| User | Group | Permissions |
|------|--------|--------------|
| user-1 | S3-Support | Read-only access to Amazon S3 |
| user-2 | EC2-Support | Read-only access to Amazon EC2 |
| user-3 | EC2-Admin | Start/Stop and view EC2 instances |

Steps:  
1. Navigated to **User groups → Add users**.  
2. Added each user to their respective group.  
3. Verified each group lists one user.

### **Task 3: Sign In and Test Permissions**
- Used IAM sign-in URL (e.g., `https://123456789012.signin.aws.amazon.com/console`).  
- **user-1:** Viewed S3 buckets only (Access Denied on EC2).  
- **user-2:** Viewed EC2 instances but denied Start/Stop or S3 access.  
- **user-3:** Viewed and successfully stopped an EC2 instance.  

---

## 🧱 Business Scenario
Simulated a growing company with separate support and admin teams.  
Demonstrated how IAM enables **role-based access control (RBAC)** by assigning least-privilege permissions per job function.

---

## ✅ Knowledge Check
- What’s the difference between a *Managed* and *Inline* policy?  
- Which IAM policy element defines allowed actions?  
- Why is the principle of *least privilege* critical in cloud security?  

---

## 📘 Key Takeaways
- IAM enforces identity-based security using users, groups, roles, and policies.  
- Managed policies = reusable permission sets; Inline policies = one-off rules.  
- JSON policy structure uses **Effect**, **Action**, and **Resource** to define scope.  
- RBAC improves security and governance for multi-user AWS environments.  

---

## 🧩 Skills Demonstrated
AWS IAM · Policy Management · Access Control · JSON Policy Syntax · RBAC · Cloud Governance  

---

## 📸 Evidence
![IAM Dashboard Screenshot](../images/iam-dashboard.png)

---

© 2025 Amazon Web Services, Inc. All rights reserved.  
*Lab reproduced and summarized for educational portfolio purposes.*
