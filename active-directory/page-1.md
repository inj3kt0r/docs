# Page 1

## 📦 Active Directory Objects

Active Directory stores information about every resource in a domain as an **object**.

An object can represent a user, computer, printer, group, shared folder, or even an entire domain. Each object has a unique identity and a set of attributes that describe it.

Think of Active Directory as a large database where every resource in the network is stored as an object.

***

### 🤔 What is an Object?

An **Active Directory Object** is any resource that Active Directory manages.

Every object has:

* A unique name
* A unique Security Identifier (SID)
* A set of attributes
* Permissions
* A specific object type

For example, a user account is an object, and so is a computer or printer.

***

### 📚 Common Active Directory Objects

#### 👤 User Object

A User Object represents a person who can log into the domain.

Example:

```
John Doe
Username: john.doe
Department: IT
Email: john.doe@corp.local
```

Common attributes include:

* Username
* Full Name
* Password
* Email Address
* Department
* Phone Number
* SID

***

#### 💻 Computer Object

Every domain-joined computer is stored as a Computer Object.

Example:

```
CLIENT01
CLIENT02
SERVER01
```

Computer objects allow administrators to:

* Apply Group Policies
* Manage permissions
* Authenticate computers
* Track devices

***

#### 👥 Group Object

Groups are used to manage permissions efficiently.

Instead of assigning permissions to every user individually, administrators assign permissions to groups.

Examples:

```
Domain Admins
Enterprise Admins
IT Team
HR Team
Remote Desktop Users
```

***

#### 🏢 Organizational Unit (OU)

An Organizational Unit (OU) is a container used to organize Active Directory objects.

Example:

```
corp.local
│
├── IT
├── HR
├── Finance
└── Servers
```

OUs help administrators:

* Organize resources
* Delegate administration
* Apply Group Policies

***

#### 🖨 Printer Object

Network printers can also be stored in Active Directory.

Example:

```
Printer-01
Printer-02
```

Users can easily discover shared printers through Active Directory.

***

#### 📂 Shared Folder Object

Shared folders can be published in Active Directory.

Example:

```
\\SERVER01\HR
\\SERVER01\Finance
```

This makes shared resources easier to locate across the network.

***

#### 🌐 Domain Object

The domain itself is an object.

Example:

```
corp.local
```

It acts as the central administrative boundary that contains all other objects.

***

#### 🖥 Domain Controller Object

Each Domain Controller is also stored as an object.

Example:

```
DC01
DC02
```

These objects replicate information with one another to keep the directory synchronized.

***

### 📝 Object Attributes

Every object contains attributes that describe it.

For a User Object:

| Attribute  | Example             |
| ---------- | ------------------- |
| Name       | John Doe            |
| Username   | john.doe            |
| Email      | john.doe@corp.local |
| Department | IT                  |
| SID        | S-1-5-21-...        |

For a Computer Object:

| Attribute        | Example             |
| ---------------- | ------------------- |
| Name             | CLIENT01            |
| Operating System | Windows 11          |
| DNS Hostname     | client01.corp.local |
| SID              | S-1-5-21-...        |

***

### 🔐 Security Identifier (SID)

Every security-related object in Active Directory has a unique **Security Identifier (SID).**

The SID is used internally by Windows to identify objects.

Example:

```
S-1-5-21-3623811015-3361044348-30300820-1013
```

Even if a user changes their username, their SID remains the same.

***

### 🔎 Distinguished Name (DN)

Every object also has a **Distinguished Name (DN)** that uniquely identifies its location within Active Directory.

Example:

```
CN=John Doe,OU=IT,DC=corp,DC=local
```

Breaking it down:

* **CN** → Common Name
* **OU** → Organizational Unit
* **DC** → Domain Component

***

### 🌳 Active Directory Hierarchy

A simplified Active Directory structure looks like this:

{% code expandable="true" %}
```
corp.local
│├── OU=IT
│     ├── John Doe
│     ├── Alice
│     └── CLIENT01
│├── OU=HR
│     ├── Bob
│     └── CLIENT02
│
└── Domain Controllers
      ├── DC01      
      └── DC02
```
{% endcode %}

This hierarchy helps administrators organize and manage resources efficiently.

***

### 🎯 Why are Active Directory Objects Important?

Active Directory Objects make it possible to:

* Centrally manage users and computers
* Apply Group Policies
* Assign permissions
* Authenticate users
* Locate network resources
* Simplify administration
* Improve security

Without objects, Active Directory would not be able to organize or manage network resources.

***

### 🧠 Key Takeaways

* Everything stored in Active Directory is an **Object**.
* Every object has attributes, permissions, and a unique identity.
* Common object types include Users, Computers, Groups, OUs, Printers, Shared Folders, and Domain Controllers.
* Objects are organized hierarchically within the domain.
* Understanding Active Directory Objects is essential before learning LDAP, Kerberos, Group Policy, and Active Directory security.
