---
icon: server
---

# What is Active Directory

## 🟥 What is Active Directory?

Active Directory (AD) is Microsoft's centralized directory service that helps organizations manage users, computers, servers, printers, groups, and other network resources from a single location.

Instead of creating user accounts on every individual computer, administrators can manage everything through a **Domain Controller (DC)**.

Active Directory is used by organizations of all sizes, from small businesses to large enterprises, making it one of the most important technologies to understand in Windows environments.

***

### 🎯 Why is Active Directory used?

Imagine a company with:

* 👨‍💼 500 Employees
* 💻 700 Computers
* 🖥️ 50 Servers
* 🏢 Multiple Office Locations

Without Active Directory:

* Every computer would have its own user accounts.
* Passwords would need to be managed separately.
* Administrators would have to configure each machine manually.
* Managing permissions would become difficult.

Active Directory solves these problems by providing centralized authentication and management.

***

### 🏗️ Core Components of Active Directory

#### 🏢 Domain

A **Domain** is a collection of users, computers, and other resources that share the same Active Directory database and security policies.

**Example:**

```
corp.local
```

***

#### 🖥️ Domain Controller (DC)

A **Domain Controller** is a Windows Server that stores the Active Directory database and authenticates users.

Its responsibilities include:

* User Authentication
* Password Management
* Group Policy
* DNS Integration
* Replication
* Security Management

***

#### 👤 Users

Every employee in an organization usually has a domain user account.

Example:

```
john.doealiceadministrator
```

These accounts allow users to log in from any domain-joined computer.

***

#### 💻 Computers

Every Windows machine joined to the domain becomes a computer object inside Active Directory.

Example:

```
CLIENT01CLIENT02SRV01
```

***

#### 👥 Groups

Groups make permission management easier.

Common examples include:

* Domain Admins
* Enterprise Admins
* Administrators
* Remote Desktop Users
* Backup Operators

Instead of assigning permissions to each user individually, permissions are assigned to groups.

***

#### 📂 Organizational Units (OU)

Organizational Units (OUs) help organize objects within a domain.

Example:

```
corp.local
│
├── IT
├── HR
├── Finance
└── Developers
```

Administrators can apply different policies to different OUs.

***

#### 🌳 Forest

A **Forest** is the highest-level structure in Active Directory.

It can contain one or more domains.

Example:

```
Forest
│
├── corp.local
├── europe.corp.local
└── us.corp.local
```

***

### 🔐 Authentication in Active Directory

When a user logs into a domain computer:

1. The user enters their username and password.
2. The computer contacts a Domain Controller.
3. The Domain Controller verifies the credentials.
4. If successful, the user is granted access to the network resources.

Active Directory primarily uses **Kerberos** for authentication and **NTLM** for compatibility with older systems.

***

### 🌐 Services Used by Active Directory

Active Directory works together with several important technologies:

* LDAP (Lightweight Directory Access Protocol)
* Kerberos
* DNS (Domain Name System)
* Group Policy
* SMB
* RPC

Understanding these protocols is essential for both administrators and security professionals.

***

### 🔴 Why is Active Directory important in Cybersecurity?

More than 90% of enterprise Windows environments use Active Directory to manage identities and access.

Because it controls authentication and authorization across an organization, it is a common target during penetration tests and real-world attacks.

Security professionals should understand:

* How Active Directory works
* How it is administered
* Common attack paths
* Defensive best practices

A solid understanding of Active Directory is fundamental for Windows administration, blue teaming, and red teaming.

***

### 📚 What's Next?

In the next articles, we'll explore:

* What is a Domain?
* What is a Domain Controller?
* Active Directory Objects
* LDAP Basics
* Kerberos Authentication
* Group Policy (GPO)
* Active Directory Lab Setup
* Active Directory Penetration Testing (with Practical)
