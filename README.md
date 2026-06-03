# AWS-IAM-S3-Least-Privilege-Access-Project-
AWS Least Privilege IAM Project
This project demonstrates how I implemented a least‑privilege access model in AWS using IAM users, groups, and custom JSON policies. The goal was to restrict identities to only the permissions required for their tasks and verify the configuration through access testing.

Overview
I created a small IAM environment in AWS to show how least‑privilege access works in practice. The project includes:
IAM user and group creation
Custom policy design
Permissions boundary usage
Testing allowed and denied actions
Screenshots documenting each step
All screenshots are stored in the screenshots folder.

1. IAM User Creation
Created a user named dev-user with console access.
Screenshot: Screenshot 2026-06-02 134802.png

2. Group Assignment
Assigned the user to DeveloperGroup, which contains a custom S3 read‑only policy.
Screenshot: Screenshot 2026-06-02 134926.png

3. Custom S3 Read‑Only Policy
Created a policy that allows the user to list all buckets, view the location of buckets, and read objects only from jack-secure-bucket.
Screenshot: Screenshot 2026-06-02 135010.png

4. S3 Bucket Setup
Created a secure S3 bucket named jack-secure-bucket for testing.
Screenshot: Screenshot 2026-06-02 135336.png

5. MFA Enforcement
Enabled MFA for the IAM user to follow AWS security best practices.
Screenshot: Screenshot 2026-06-02 135535.png

Results
The least‑privilege model worked as expected. Users were able to perform only the actions defined in their policies, and attempts to access unauthorized services or operations were denied.
Key Takeaways
Least‑privilege access reduces risk and limits the impact of compromised credentials
Permissions boundaries add an extra layer of control
Testing is essential to confirm policy behavior
IAM requires clear structure and documentation
