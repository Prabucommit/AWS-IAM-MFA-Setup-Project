# AWS-IAM-MFA-Setup-Project
Creating a IAM User, Creating a User Group, Assigning a Permission to a User and Setting Up MFA.
# ☁️ Project 1: Securing AWS with IAM, User Groups, and Multi-Factor Authentication (MFA)

## 🎯 Project Goal
Demonstrate foundational security practices in AWS by configuring Identity and Access Management (IAM) to:
1.  Create a dedicated **IAM User** with an initial password reset required.
2.  Organize the user within a custom **IAM User Group** with specific permissions.
3.  Enforce **Multi-Factor Authentication (MFA)** for enhanced account security.

## 🔧 AWS Services Used
* **IAM (Identity and Access Management):** Users, Groups, Policies.

---

## 💡 Cloud Support Engineer Relevance
This project directly addresses a critical and common task for a Cloud Support Engineer: **access management and security configuration**. Understanding IAM is key to troubleshooting "Access Denied" errors, enforcing the **Principle of Least Privilege**, and responding to security audit requests.

---

## ⚙️ Implementation Steps & Key Learnings

### 1. Setting Up the Policy (Principle of Least Privilege)
* **Action:** Created a custom IAM policy named `S3-ReadOnly-Policy` to grant read-only access to S3.
* **Learning:** I learned how to define and scope permissions using the Policy JSON structure to ensure the user can only perform necessary actions.
*  

### 2. Creating the User and Group
* **Action:** Created a new User `john-doe-admin` and a Group `Cloud-Admins-Group`.
* **Action:** Attached the custom `S3-ReadOnly-Policy` to the `Cloud-Admins-Group`.
* **Action:** Added the `john-doe-admin` user to the group.
* **Proof:** See the attached **`IAM-Policy.json`** file for the policy structure.

### 3. Enforcing and Testing MFA
* **Action:** Logged in as the new user and navigated through the process of setting up a virtual MFA device (e.g., using Google Authenticator).
* **Challenge:** The user initially had issues activating the MFA due to permission boundaries.
* **Solution:** *[Explain your specific troubleshooting steps here, e.g., "I confirmed the group's policy had the correct `iam:CreateVirtualMFADevice` action."]*
* **Result:** Successfully enforced MFA, requiring a 6-digit code upon future logins, significantly hardening security.
* 

---

## 📄 Repository Contents
* `screenshots/`: Screenshots of the IAM Policy, User Group members, and MFA confirmation.
* `IAM-Policy.json`: The JSON code for the custom IAM policy used in the project.
* `README.md`: This documentation.

---
