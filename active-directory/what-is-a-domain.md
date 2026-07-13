---
icon: chart-network
---

# What is a Domain ?

## 🏢 What is a Domain?

A **Domain** is a logical collection of users, computers, servers, groups, and other network resources that are managed together under a single administrative boundary.

In Active Directory, a domain allows administrators to centrally manage authentication, authorization, security policies, and access to shared resources.

Simply put, a domain enables users to sign in with one account and securely access resources across the organization's network.

***

### 🤔 Why do we need a Domain?

Imagine a company with:

* 👨‍💼 500 Employees
* 💻 800 Computers
* 🖥️ 100 Servers
* 🏢 Multiple Office Locations

Without a domain:

* Every computer would have its own local user accounts.
* Employees would need different usernames and passwords for different computers.
* Administrators would have to manually manage each system.
* Security policies would be difficult to enforce.

A domain solves these problems by centralizing identity and management.

***

### 🏗️ Example

Suppose a company called **Inj3kt0r Labs** has the following domain:

```
inj3ktor.local
```

Users:

```
alicebobcharlieadministrator
```

Computers:

```
CLIENT01CLIENT02CLIENT03SERVER01
```

All these objects belong to the **inj3ktor.local** domain and are managed by the Domain Controller.

***

### 🔑 Domain vs Local Account

#### Local Account

A local account exists only on one computer.

Example:

```
Laptop01
└── User: John
```

John can only log in to **Laptop01** using that account.

***

#### Domain Account

A domain account is stored in Active Directory.

Example:

```
Domain
└── inj3ktor.local   
   └── John
```

John can log in to any domain-joined computer using the same credentials, provided he has permission.

***

### 🌐 Domain Name

Every Active Directory domain has a unique DNS name.

Examples:

```
corp.locallab.localcompany.comad.inj3ktor.local
```

The domain name helps computers locate Domain Controllers and other services using DNS.

***

### 🖥️ What is stored inside a Domain?

A typical domain contains:

* 👤 Users
* 💻 Computers
* 👥 Security Groups
* 🏢 Organizational Units (OUs)
* 🖨 Printers
* 📂 Shared Folders
* 📜 Group Policies
* 🖥 Domain Controllers

All these objects are stored in the Active Directory database.

***

### 🔐 Authentication

When a user signs in:

1. The user enters their domain username and password.
2. The computer contacts a Domain Controller.
3. The Domain Controller verifies the credentials.
4. If authentication succeeds, the user receives access based on their permissions.

This allows users to access shared folders, printers, applications, and other domain resources without creating separate accounts on each system.

***

### 📌 Advantages of Using a Domain

* Centralized user management
* Single sign-on (SSO)
* Centralized security policies
* Easier administration
* Resource sharing
* Better scalability
* Improved security
* Simplified password management

***

### ⚠️ Domain vs Workgroup

| Domain                     | Workgroup                           |
| -------------------------- | ----------------------------------- |
| Centralized management     | Each computer is managed separately |
| Uses Domain Controllers    | No Domain Controller                |
| Single Sign-On             | Separate accounts on every computer |
| Suitable for organizations | Suitable for small home networks    |
| Supports Group Policy      | No centralized Group Policy         |

***

### 🧠 Key Takeaways

* A **Domain** is a centralized administrative boundary in Active Directory.
* It stores users, computers, groups, and other network objects.
* Users authenticate using a single domain account.
* Domain Controllers manage authentication and security.
* Domains simplify administration and improve security in enterprise environments.

***

### 📚 Next Topics

After understanding what a domain is, continue with:

* 🖥️ What is a Domain Controller?
* 👥 Active Directory Objects
* 📂 Organizational Units (OUs)
* 🔑 Authentication in Active Directory
* 🌐 DNS in Active Directory
* 🎫 Kerberos Authentication
* 📜 Group Policy (GPO)
