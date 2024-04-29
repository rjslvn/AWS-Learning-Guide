
**IAM Deep Dive**

* **Users:**  Individual accounts for people accessing AWS. Enforce strong passwords and multi-factor authentication (MFA).
* **Groups:** Organize users based on job function. Apply permissions at the group level for streamlined management.
* **Roles:**  Temporary credentials for services/applications. Avoid embedding access keys directly in code; instead, grant roles to EC2 instances or Lambda functions.
* **Policies:**  JSON documents defining permissions. Adhere to the principle of least privilege – grant only the minimum necessary access.

**Best Practices**

*  **Regularly Review IAM:** Audit permissions and remove unused or excessive access.
* **IAM Credentials Rotation:** Rotate access keys and enforce password changes.
* **Leverage AWS Tools:**  Use services like IAM Policy Simulator and IAM Access Analyzer  to validate and refine policies.

**Encryption**

* **Encryption at Rest:** Protecting stored data.
    * **SSE-S3:** Server-side encryption managed by S3.
    * **SSE-KMS:** Encryption using keys managed by AWS Key Management Service (KMS).
    * **Client-side Encryption:** Encrypt data before uploading to AWS.

* **Encryption in Transit:**  Protecting data in motion.
    * **HTTPS/TLS:** Use secure protocols for data transfer.
    * **VPN:**  Encrypted tunnels for private connectivity (e.g., between VPC and on-premises).

**Network Security** 

* **Security Groups:** Instance-level firewalls. Control inbound and outbound traffic with stateful filtering.
* **NACLs:** Subnet-level firewalls.  Stateless rules for traffic filtering. Use as an additional layer of defense.
* **VPC Endpoints:** Enable private connections to supported AWS services within your VPC, keeping traffic off the public internet. 

**Compliance**

* **AWS Responsibility Model:**  Understand that AWS secures the *of* the cloud, while you are responsible for security *in* the cloud.
* **Relevant Frameworks:** AWS supports compliance with various standards:
    * **PCI-DSS:** For handling payment card data.
    * **HIPAA:** For protected healthcare information.
    * **FedRAMP:** For US government workloads.
* **AWS Artifact:** Provides access to compliance reports and certifications.

**IMPORTANT NOTES**

* **Defense in Depth:**  Security is best achieved through a layered approach.
* **Continual Monitoring:**  Leverage tools like GuardDuty, Security Hub, and Config to identify potential security issues. 
