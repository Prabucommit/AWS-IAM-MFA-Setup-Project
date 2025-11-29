# 🔒 AWS-IAM-MFA-Setup-Project: Enforcing Cloud Security

## ☁️ Project Goal
In this project I will be showing you how to create a **IAM User**, create a **user group** to add a user into it, and assigning special permissions for a user as well as mandating **Multi-Factor Authentication (MFA)** for enhanced user security.

---

## 💡 What is an IAM User?
**AWS Identity and Access Management (IAM)** is a web service for securely controlling access to AWS services. With IAM, you can centrally manage **users**, **security credentials** (like access keys), and **permissions** that control which AWS resources users and applications can access.

![AWS IAM Introduction Diagram](ss1.webp)

---

## ⚙️ Prerequisites & Setup

1.A **AWS account** (New users will be eligible for the 1 year AWS Free Tier).
  
2.A working **PC/Laptop**. MacOS/Windows
   
3.Sign into your AWS account. Upon successfully logging into your AWS account, you will be greeted with the AWS Management Console Home. Type “IAM” in the search box and click on **“IAM”**.
   
![iam console](https://github.com/user-attachments/assets/d4e408c1-118f-43f3-9a67-55a052afce51)

---
## 🛠️ Implementation Steps

5.You will be greeted with the **“Add User”** page. The first thing you must do is to choose a username for your user. For the sake of this project, I use the name **“DemoProjectUser22”**. It is up to you as the root user to choose a name that appropriately helps you properly “MANAGE” and “IDENTIFY” your user(s).

After choosing a username that fits your liking, you will have the option of choosing how the user will have access to the console. If you select **“Access key — Programatic Access”**, this will require the user to enter a granted access key ID in order to use certain AWS services such as the **Command Line (CL), API (Application Programming Interface), or SDK (Software Development Kit)**.

The second option is to create a **console password** that will enable your user(s) to be able to enter and have access to the console. For the sake of this project, I used the second option.

The user will have the ability to **change their password upon their next sign-in**, and this is strictly for security reasons.

![add user](https://github.com/user-attachments/assets/fb355789-28c1-4567-abc3-c74edb02a862)
<img width="1395" height="272" alt="s2" src="https://github.com/user-attachments/assets/9a75fb7a-98e9-4d73-94cd-38a8ae41dd4f" />

---

6.Next up, we are going to create a **“User group”** to place our user(s) into. Click on **“Add user to group”**.
   
<img width="2698" height="1166" alt="create group" src="https://github.com/user-attachments/assets/1fa384fb-e079-4abb-838d-42c86f8280d3" />

---

7.Enter a **“Group name”**. As you can see below in the image, I chose **“AdminsOfTheWorld”** as the group name.

We are going to give our group **Administrator Access**. Administrator Access provides unlimited access with no restrictions to AWS services and resources. Select **“AdministratorAccess”** and click on **“Create group”**.

![group permission](https://github.com/user-attachments/assets/fafdbb91-00d6-458b-9d5b-16605cf906d5)

---

8.Verify here on the review page that everything is setup to your liking before the user and group is officially created. When you are satisfied with how everything is setup, click on **“Create user”**.

![review iam](https://github.com/user-attachments/assets/fc7c38cc-53c8-4a91-bf45-ae82c8bc995b)

---

9.Finally… Congratulations you have successfully created your user and group!

<img width="2250" height="647" alt="iam created succesfuly" src="https://github.com/user-attachments/assets/8647512f-327d-454b-b792-b0ef63a181bb" />

---
# Enforcing Multi-Factor Authentication (MFA)

10.Now that the user and group have been officially created, it is time to setup **Multi Factor Authentication (MFA)** for the user. MFA is another layer of security that further helps users ensure that their account is protected. MFA comes in a variety of different methods, including a **virtual MFA device** (Ex: Microsoft Authenticator), a **U2F security key**, and a **hardware-based MFA device**.

11.Under **Security credentials** where it says “Assigned MFA device”, click on **“Manage”**.
    
![summary of mfa](https://github.com/user-attachments/assets/497b7677-6ace-4b27-9975-bbaeaec280d5)

We will be using a **virtual MFA device** for this project. I used Microsoft Authenticator as the “Manage MFA device”.
  
![manage mfa](https://github.com/user-attachments/assets/ba506cca-c9b2-4d5c-8670-b175673e5b4a)

---

12.Due to security reasons I will not be showing the MFA access codes. Upon entering the MFA code you should get the same successful message. The user now has the peace of mind of knowing that their account is more secured with MFA setup.

![assigned mfa](https://github.com/user-attachments/assets/b2856584-5667-4978-8268-dbc46dcac462)

![mfa attached](https://github.com/user-attachments/assets/3ce4f069-a9cc-440e-a9ac-fa7af3ae2e3b)

## 🧹 Cleanup and Conclusion

**Congratulations!** You have successfully created a IAM user, User group, as well as set up MFA for your user. Do not forget to delete your user if you don’t want them having long-term access group access!

![delete user](https://github.com/user-attachments/assets/9f667227-8b78-45e9-ac11-03046b02bc36)

Thank you for viewing this project!
