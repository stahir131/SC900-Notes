There are four learning paths to prepare for the SC-900<br />

**Part 1: Describe the concepts of security, compliance, and identity**<br />
**Part 2: Describe the capabilities of Microsoft Entra<br />**
**Part 3: Describe the capabilities of Microsoft security solutions<br />**
**Part 4: Describe the capabilities of Microsoft compliance solutions<br />**


**Part 1: Describe the concepts of security, compliance, and identity**<br />
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
 Compliance refers to the country/region, state or federal laws or even multi-national regulations that an organization must follow. This may include Data residency, data sovereignty and data privacy


















 
   
