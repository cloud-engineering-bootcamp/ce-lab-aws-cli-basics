# Lab M1.02-2 - AWS CLI Basics

**Repository:** https://github.com/cloud-engineering-bootcamp/ce-lab-aws-cli-basics

**Activity Type:** Individual

**Estimated Time:** 45–60 minutes

**Submission:** GitHub Repository

---

# Learning Objectives

By completing this lab, you will:

- Verify your AWS CLI installation
- Configure and validate AWS CLI credentials
- Retrieve AWS account information
- Explore AWS Regions and Availability Zones
- Investigate IAM resources using the AWS CLI
- Explore EC2 resources using the AWS CLI
- Read and understand AWS CLI output

---

# Prerequisites

- AWS Account
- IAM User
- AWS CLI Installed
- AWS CLI Configured
- Git Installed

---

# Introduction

Welcome to your first AWS CLI lab!

While the AWS Management Console is useful for exploring services, cloud engineers frequently use the AWS Command Line Interface (CLI) to automate tasks, inspect cloud resources, and troubleshoot environments.

In this lab, you'll use only the AWS CLI to investigate your AWS account and gather information about your cloud environment.

Throughout the lab, capture screenshots of your terminal output and save them inside the **screenshots** folder using the exact filenames provided.

---

# Repository Structure

```text
ce-lab-aws-cli-basics/
│
├── README.md
├── SOLUTION.md
└── screenshots/
```

---

# Part 1 – Verify AWS CLI Installation

Run the following commands:

```bash
aws --version

aws configure list

aws sts get-caller-identity
```

Record the outputs in **SOLUTION.md**.

Save your screenshots as:

```text
task1-aws-version.png
task1-configure-list.png
task1-caller-identity.png
```

---

# Part 2 – AWS Account Information

Retrieve information about your AWS account.

Run:

```bash
aws sts get-caller-identity

aws configure get region

aws configure get output
```

Answer the following questions in **SOLUTION.md**:

- What is your AWS Account ID?
- What is your IAM User ARN?
- What is your configured default Region?
- What output format is configured?

Save your screenshot as:

```text
task2-account-information.png
```

---

# Part 3 – AWS Regions & Availability Zones

Run:

```bash
aws ec2 describe-regions --output table

aws ec2 describe-availability-zones --output table
```

Answer:

- How many AWS Regions are available?
- Which Region is configured as your default?
- How many Availability Zones exist in your current Region?
- Why should production workloads use multiple Availability Zones?

Save your screenshots as:

```text
task3-regions.png

task3-availability-zones.png
```

---

# Part 4 – Investigating IAM

Run:

```bash
aws iam list-users

aws iam get-account-summary
```

Answer:

- How many IAM users exist?
- Why is using IAM users safer than using the root account?

Save your screenshots as:

```text
task4-list-users.png

task4-account-summary.png
```

---

# Part 5 – Investigating EC2

Run:

```bash
aws ec2 describe-instances

aws ec2 describe-key-pairs

aws ec2 describe-instance-types \
    --instance-types t3.micro \
    --output table
```

Answer:

- Are there any EC2 instances running?
- Are any EC2 Key Pairs configured?
- What information does AWS return for the **t3.micro** instance type?

Save your screenshots as:

```text
task5-describe-instances.png

task5-key-pairs.png

task5-instance-types.png
```

---

# Reflection

Answer the following questions in **SOLUTION.md**:

1. Which AWS CLI command did you find most useful?

2. Which command output was the easiest to understand?

3. How does using the AWS CLI compare to navigating the AWS Management Console?

---

# Deliverables

By the end of this lab, your repository should have the following structure:

```text
ce-lab-aws-cli-basics/
│
├── README.md
├── SOLUTION.md
└── screenshots/
    ├── task1-aws-version.png
    ├── task1-configure-list.png
    ├── task1-caller-identity.png
    ├── task2-account-information.png
    ├── task3-regions.png
    ├── task3-availability-zones.png
    ├── task4-list-users.png
    ├── task4-account-summary.png
    ├── task5-describe-instances.png
    ├── task5-key-pairs.png
    └── task5-instance-types.png
```

Before submitting, make sure you have:

- Completed every section in **SOLUTION.md**
- Saved every screenshot inside the **screenshots** folder using the exact filenames above
- Committed all your changes to Git
- Pushed your repository to GitHub
- Created a Pull Request
- Submitted the Pull Request URL to the student portal

> **Important:** The screenshot links inside `SOLUTION.md` already reference these filenames. If you rename a screenshot or place it in another folder, it will not display correctly on GitHub.

---

# Success Criteria

Your lab is complete when:

- [x ] AWS CLI is installed and working
- [x ] AWS account information retrieved successfully
- [x ] AWS Regions explored
- [x ] Availability Zones investigated
- [x ] IAM information retrieved
- [x ] EC2 information retrieved
- [x ] Reflection questions answered
- [x ] All screenshots saved with the correct filenames
- [x ] Repository pushed to GitHub
- [x ] Pull Request submitted

---

# Bonus Challenge

Use the AWS CLI help command to learn about another AWS service.

Examples:

```bash
aws s3 help

aws lambda help

aws dynamodb help
```

Choose one service and answer:

- What does the service do?
- What problem does it solve?
- Where do you think it might be used?

---

# Troubleshooting

## "Unable to locate credentials"

Run:

```bash
aws configure
```

Verify your:

- Access Key ID
- Secret Access Key
- Default Region
- Output Format

---

## "Access Denied"

Ensure your IAM user has permission to access the requested AWS service.

---

## "AWS CLI not found"

Verify your installation:

```bash
aws --version
```

If necessary, restart your terminal after installing AWS CLI.

---

# Grading Rubric (100 Points)

| Criteria | Points |
|----------|-------:|
| AWS CLI Installation & Configuration | 15 |
| AWS Account Investigation | 20 |
| Regions & Availability Zones | 20 |
| IAM Investigation | 20 |
| EC2 Investigation | 15 |
| Reflection | 10 |

---

# Additional Resources

- AWS CLI User Guide
- AWS CLI Command Reference
- AWS Documentation
- AWS Free Tier

---
