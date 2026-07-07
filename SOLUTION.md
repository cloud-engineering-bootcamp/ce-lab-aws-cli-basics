# AWS CLI Basics - Solution

Name: Faramarz Karamizadeh

GitHub Username: f-karamizadeh

---

# Task 1 - Verify AWS CLI

## aws --version

aws-cli/2.34.60 Python/3.14.5 Windows/11 exe/ARM64

```

### Screenshot

![Task 1](screenshots/task1-aws-version.png)

---

# Task 2 - AWS Configuration

## aws configure list

NAME       : VALUE                    : TYPE             : LOCATION
profile    : <not set>                : None             : None
access_key : ****************YT44     : shared-credentials-file :
secret_key : ****************kVnO     : shared-credentials-file :
region     : eu-north-1               : config-file      : ~/.aws/config

### Screenshot

![Task 2](screenshots/task2-configure-list.png)

---

# Task 3 - Caller Identity

## aws sts get-caller-identity
{                                                                                                                                                                        
    "UserId": "AIDAS7CA3GYETARUZV4JC",
    "Account": "204146947593",
    "Arn": "arn:aws:iam::204146947593:user/fara"
}

### Screenshot

![Task 3](screenshots/task3-caller-identity.png)

---

# Task 4 - AWS Regions

Number of Regions: 17

Default Region: eu-north-1

Closest Region: eu-central-1

### Screenshot

![Task 4](screenshots/task4-regions.png)

---

# Task 5 - Availability Zones

Number of AZs: 3

Why are multiple AZs important?
Multiple Availability Zones (AZs) are crucial because they prevent a single physical disaster or power outage from taking your entire business offline. High Availability & Fault Tolerance , Redundancy Without High Latency are  exactly why they matter.
### Screenshot

![Task 5](screenshots/task5-availability-zones.png)

---

# Task 6 - S3 Investigation

Buckets: 1

Reason if none exist:

### Screenshot

![Task 6](screenshots/task6-s3-buckets.png)

---

# Task 7 - IAM Investigation

IAM Users: 1 user

Why avoid using the root account?
It has absolute, unrestrictable power over your entire AWS account.If your root account credentials are leaked, stolen, or compromised, a malicious actor can instantly gain full control.

### Screenshot

![Task 7](screenshots/task7-iam-users.png)

---

# Task 8 - EC2 Investigation

Running Instances: 1

Key Pairs: Yes

Instance Types: t3.micro

### Screenshot

![Task 8](screenshots/task8-ec2-info.png)

---

# Task 9 - Output Formats

Preferred format: table

Reason: readability

### Screenshot

![Task 9](screenshots/task9-output-formats.png)

---

# Reflection
1. Which AWS CLI command did you find most useful?
I think the most useful command was `aws ec2 describe-availability-zones`. Instead of clicking through multiple sub-menus in the AWS Management Console to find topological details, this single command instantly maps out the available infrastructure zones within a region. It is incredibly efficient for a quick health check of the underlying cloud landscape.

2. Which command output was the easiest to understand?
The output of `aws iam get-user` (or `aws sts get-caller-identity`) was the easiest to parse. Because it returns a clean, highly structured JSON block containing just a few clear key-value pairs—such as the explicit `UserId`, `Account` ID, and the exact user `Arn`—it leaves zero room for ambiguity regarding which identity is currently authenticated in the terminal.

3. How does using the AWS CLI compare to navigating the AWS Management Console?
**AWS Management Console** is excellent for visual exploration, initial learning, and viewing high-level dashboards. However, it can be slow, requires extensive clicking, and makes repetitive tasks inefficient.
**AWS CLI** is built for speed, precision, and automation. Once you know the specific queries, executing a command takes seconds. More importantly, CLI operations can be easily scripted and integrated into DevOps automation pipelines, making it the preferred choice for managing scalable cloud infrastructure.

# Bonus

### Screenshot

![Bonus](screenshots/bonus-vpc.png)
