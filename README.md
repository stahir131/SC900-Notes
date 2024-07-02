There are four learning paths to prepare for the SC-900<br />

**Part 1: Describe the concepts of security, compliance, and identity**<br />
**Part 2: Describe the capabilities of Microsoft Entra <br />**
**Part 3: Describe the capabilities of Microsoft security solutions<br />**
**Part 4: Describe the capabilities of Microsoft compliance solutions<br />**


**Part 1: Describe the concepts of security, compliance, and identity**<br />
**Module 1**: Security and compliance concepts<br />
Covered in this chapter are;<br />
1. Shared responsibilty and defence in-depth<br />
2. Zero-Trust model<br />
3. Encryption and hashing<br />
4. Basic compliance concepts

**1. Shared responsibilty and defence in-depth<br />**
  i. On-premises datacenters: Customer is responsible for everything from       physical security to encrypting sensitive data. <br />
  
 ii. Infrastructure as a Service (IaaS): Cloud provider is responsible for physical components like computers, network and physical security of the datacenter. Cloud cutomer is responsible for software components such as OS, network controls, applications and protecting data.

 iii. Platform as a Service (PaaS): PaaS provides environment for building,testing and deploying software apps.Cloud provider manages hardware and OS while customer is responsible for apps and data.

iv. Software as a Service (SaaS): example is M365, Skype via a subscription. Cloud provider manages everything except data, devices, accounts and identities

In all cloud model, customer is always responsible for:

  Information and data
  Devices (mobile and PCs)
  Accounts and identities

**Defense in depth**<br />: It uses a layered approach to security rather than relying on ansingle perimeter. It uses a series of mechanism/layer to slow advance of an attack so when one layer is breached, a subsequent layer will prevent an attacker getting unauthorized access to data.<br />
The layers might be; Physical, Identity and access, Perimeter, Network, Compute, Application and Data.

![4-defense-depth](https://github.com/stahir131/SC900-Notes/assets/64047385/e13e723a-ce02-434c-812e-91f3229071d1)

**Confidentiality, Integrity, Availability (CIA)**

![4-confidentiality-integrity-availability](https://github.com/stahir131/SC900-Notes/assets/64047385/b8d3fca4-c69f-45cc-ba0e-4065fbbaf821)

Confidentiality: Refers to the need to keep sensitive data, keys, passwords and other secrets confidential.<br />
Integrity: Refers to keeping data or messages correct. When you send email messages, you want to be sure recipient got the same messages you sent. <br />
Availability: Refers to making data available to those who need it , when they need it.

**Zero Trust model**<br />: The principle that nothing is secure even resources behind the firewalls. 
Only password is not sufficient<br />
Users must be granted access to only apps and data that they need.<br />
**Three guiding principles of Zero Trust**
1. Verify explicitly: Always authenticate and authorize based available data points like user identity, location, device, service.<br />
2. Least privileged access: Limit user access with just-in-time and just-enough access(JIT/JEA). In JIT, access is limited to predetermined periods of time, on an as-needed basis.<br />
3. Assume breach: Segment access by network, user, devices and application. Use encryption to protect data.

**Six foundational pillars**
1. Identities
2. Devices
3. Applications
4. Data
5. Infrastructure
6. Networks

**Encryption and Hashing**<br />
Encryption is the process of making data unreadable and unusable to unauthorized viewers. Must be decrypted by using a secret key to make it readable.<br />
There are two top-level types of encryption:
**Symmetric**: It uses same key to encrypt and decrypt data.<br />
**Asmmetric**: It uses a public and private key pair. Either key can encrypt data, but the key used to encrypt can't be used to decrypt encrypted data. You need a paired key to decrypt the data. Examaple, if a public key is used to encrypt you need the corresponding private key to decrypt it.<br />
Asymmetric encryption is used for accessing websites using HTTPS protocol amnd electronic data signing solutions.
![image](https://github.com/stahir131/SC900-Notes/assets/64047385/26dd5278-3d36-409e-95d2-6674667b4159)

**Encryption for data at rest**: Data stored in a server, database or storage account can be encrypted.<br />
**Encryption for data in transit**: HTTPS is an example of data encryption in transit. Data moving from one location to another.<br />
**Encryption for data in use**: Example of this involves securing data in nonpersistent storage such as RAM or CPU caches.

**Hashing**: It uses an algorithm to convert text to a unique fixed-length value called a hash. Each time the same text is hashed using the same algorithm, the same hash is produced.<br />
Hashing is different from encryption in that it doesn't use keys and the hashed value is not decrypted back to the original. <br />
Hashing is often used to store passwords. Hackers can use brute-force dictionary attack. To mitigate the risk, passwords are often Salted - adding a fixed-length random value to the input of hash functions.

**Basic compliance concepts**: Governance, Risk and Compliance(GRC)<br />
Governance: is the system of rules, practices, and processes an organization uses to direct and control its activities.<br />
Risk management is the process of identifying, assessing, and responding to threats or events that can impact company or customer objectives.<br />
 Compliance refers to the country/region, state or federal laws or even multi-national regulations that an organization must follow. This may include Data residency, data sovereignty and data privacy.

**Data residency**: Refers to physical locations where data can be stored, how and when it can be transferred, processes or accessed internationally.<br />
**Data sovereignty**: Data is subject the laws and regulations of the country in which its physically collected, held or processed.<br />
**Data privacy**: Providing notice and being transparent about the collection, processing, use, and sharing of personal data.

**Module 2**: Identity concepts<br />
Identity is the way in which people and things are identified on your corporate network, and in the cloud.<br />

**Authentication**: Authentication is the process of proving that a person is who they say they are.<br />

**Authorization**: Once authenticated, this determines the level of access or permissions a user has to data and resources.<br />

**Identity as Primary security perimeter**: There are four fundamental pillars in an identity infrastucture<br />

1. Administration: This is about the creation and management/governance of identities for users, devices, and services.<br />
2. Authentication<br />
3. Authorization<br />
4. Auditing: Tracking who does what, when, where and how. Involves repoting, alerting and governance of identities<br />

**Role of identity provider(IdP)**:<br />
An identity provider creates, maintains, and manages identity information while offering authentication, authorization, and auditing services.
Modern authentication is an umbrella term for authentication and authorization methods between a client, such as your laptop or phone, and a server, like a website or application.<br />
In modern authentication, the client communicates with the IdP using username&password. When the identity is verified, the IdP issues a _security token_ that the client sends to the server.<br />
The server validates the security token through its _trust relationship_ witht the identity provider. <br />
Examples of idP are Microsoft Entra ID, Google, Amazon, LinkedIn, GitHub.<br />

**Single sign-on**: idP and modern authentication are capable of single sign-on. With SSO, the user logs in once and that credential is used to access multiple applications or resources. When you set up SSO between multiple identity providers, it's called federation.<br />
**Concept of directory services and Active Directory**<br />
Active Directory Domain Services(AD DS) stores information about the members of the domain, including devices, users, verifies their credentilas and define their access rights.<br />
AD DS only supports on-prem infrastructure components, it does not support mobile devices, SaaS apps or line of business apps that require modern authentication methods.<br />
**Concept of federation**<br />
Federation enables the access of services across organizational or domain boundaries by establishing trust relationships between the respective domain’s identity provider.













**Part 2: Describe the capabilities of Microsoft Entra<br />**
**Module 1**: Function and identity types of Microsoft Entra ID<br />
Identity can be assigned to users, physical devices and software-based such as applications.<br />
Types of Identities<br />
**User identity**: These are employees and external users such as customers, vendors and partners. In Entra ID, user identities are characterized by how they authenticate and user type property. <br />
Internal authentication: Useers has account on host organozation's Entra ID and authenticate to Entra ID. <br />
External authentication: Users authenticate using an external Entra account of another Org, a social network identity or external identity provider.<br />
User type property describes whether user is a guest or a member of the organization Entra tenant.<br />

**Workload identities**: You assign to a software workload to enable it autheticate to and access other services and resources. Workload identities  are applications, service principals and managed identities.<br />

Applications and service principals: This is an identity for an application. For apps to delegate its identity and access functions to Entra ID, it must register to enable its integration with Entra ID. Then a service principal is created in each Entra ID tenant where the app is used. <br />
Manage identities: type of service principal that are managed automatically in micorosoft Entra ID and relief the stress off of app developers to manage credentials.
![image](https://github.com/stahir131/SC900-Notes/assets/64047385/0f15debf-a5e7-4c16-8f4f-5abdd477d753)

There are two types of managed identities: System-assigned and user-assigned<br />
System-assigned is when managed identity is enabled directly on the resources and its tied to the lifecycle of the resource. When the resource is deleted the identity gets deleted as well.<br />
User-assigned: This is when managed identity is created as a standalone Azure resource and then can be assigned to one or more instances of an Azure service. 
- can be assigned to multiple VMs
- its managed separately from the resources that use it.
- deleting resources that use it does not delete the identity
- Useful with multiple VMs with same set of permissions.

**Devive identity**: This can be set up in different ways<br />
1. Microsoft Entra registered devices: For BYOD users to access your organization's resources. The devices register to Entra ID without requiring organizational account to sign in to the device.<br />
2. Microsoft Entra joined: Organization owned devices joined to Entra ID using org account and then used to sign in to the device.<br />
3. Microsoft Entra hybrid joined devices: To control devices that are AD and Entra ID joined.

**Hybrid identity**: A combination of both on-premises and cloud environments.<br />
Hybrid identity is done through provisioning and synchronization.<br />
1. Inter-directory provisioning is provisioning an identity between two different directory services systems.<br />
2. Synchronization: Done to make sure identity information for on-prem users and groups is matching the cloud. These both are done using Entra cloud sync<br />

**External identities**:<br />
1. B2B collaboration: Typically represented as guest users to sign in to your Microsoft applications or other enterprise apps by using their preferred identity.B2B does not require credentials to sign but rather they authenticate with their home organization or identity provider.The guests are created in your directory.There are various ways to add external users<br />
  a. Invite users to B2B collaboration using their Microsoft enta accounts, microsft accounts, or social identities that you enable.<br />
  b. Use self-service sign up user flows to let external users sign up for applications themselves. You can customize to allow sign-up with a work, school or social identity. User info can be collected during sign-up process.<br />
  c. Use Microsoft Entra entitlement management, an identity governance feature that lets you manage identity and access for external users at scale by automating access request workflows, access assignments, reviews, and expiration.<br />
3. B2B direct connect: A new way to collaborate with other Microsoft Entra organizations using the Miccrosoft Teams shared channels. Here you create 2-way trust relationships with other Enrtra organizations to allow users to seamlessly sign in to your shared resources and vice-versa. The users here are not added as guests but are visible from within Teams shared channel and managed in Teams admin center.
4. Microsoft Entra External ID for customers (preview)
5. Microsoft Entra multi-tenant organization


**Module 2**:Authentication capabilities of Microsoft Entra ID<br />
**Phone**: Microsoft Entra ID supports two options for phone-based authentication.<br />
SMS-based authentication: SMS can be used as a primary form of authentication where users don't require username and passowrd. They enter their registered number to receive a code to sign in.<br />
SMS can also be used as a secondary form of authentication during self-service password or Entra ID MFA.

Voice call verification: User receives a phone call to authenticate.

**OATH**: Open Authentication is an open standard that specifies how time-based, one-time password (TOTP) codes are generated.

Software OATH tokens are typically applications. Microsoft Entra ID generates the secret key, or seed, that's input into the app and used to generate each OTP.

OATH TOTP hardware tokens are devices that look like a key fob that displays a code and refreshes every 30/60 seconds

Passwordless authentication: The use of biometrics with Windows Hello for Business or a FIDO2 security key.

Windows Hello for Business:As a passwordless authentication method, Windows Hello for Business serves as a primary or secondary form of authentication

FIDO2: Fast Identity Online is an open standard for passwordless authentication. It uses an external security key or a platform key built into a device. 
They are unphishable<br />
They incoporate web autheutication(WebAuthn)<br />
Typically USB devices or bluetooth or NFC based devices
 
Microsoft Authenticator app: Can be user as a primary or secondary form of authentication

Certificate-based authentication: This is only supported as a primary form of authentication. It uses X.509 certificates

Security defaults and multifactor authentication<br />











   
