# AWS CLI Basics - Solution

**Name:** Julio Aldana

**GitHub Username:** Jcaldana97

---

# Part 1 – Verify AWS CLI Installation

## Command Output

### aws --version

```aws-cli/2.35.11 Python/3.14.5 Windows/11 exe/AMD64

```

### aws configure list

``` NAME       : VALUE                    : TYPE             : LOCATION
profile    : <not set>                : None             : None
access_key : ****************DG3T     : shared-credentials-file : 
secret_key : ****************tzwJ     : shared-credentials-file : 
region     : us-east-1                : config-file      : ~/.aws/config

```

### aws sts get-caller-identity

```{                                                                                 
    "UserId": "AIDA4COT7F5XWDL6SF5LE",
    "Account": "829910101871",
    "Arn": "arn:aws:iam::829910101871:user/julioaldana"
}

```

### Screenshots

![AWS Version](screenshots/task1-aws-version.png)

![AWS Configure List](screenshots/task1-configure-list.png)

![Caller Identity](screenshots/task1-caller-identity.png)

---

# Part 2 – AWS Account Information

Answer the following:

**AWS Account ID:** AIDA4COT7F5XWDL6SF5LE

**IAM User ARN:** arn:aws:iam::829910101871:user/julioaldana

**Default Region:** us-east-1

**Configured Output Format:** json

### Screenshot

![Account Information](screenshots/task2-account-information.png)

---

# Part 3 – AWS Regions & Availability Zones

## Regions

**How many AWS Regions are available?** 17

**Which Region is configured as your default?** us-east-1

### Screenshot

![AWS Regions](screenshots/task3-regions.png)

---

## Availability Zones

**How many Availability Zones exist in your current Region?** 6

**Why should production workloads use multiple Availability Zones?** To have more resources available in case one server is overloaded.

### Screenshot

![Availability Zones](screenshots/task3-availability-zones.png)

---

# Part 4 – Investigating IAM

**How many IAM users exist?** 1

**Why is using IAM users safer than using the root account?** Because with IAM users you can control the permisions the user has, reducing the security risks.

### Screenshots

![IAM Users](screenshots/task4-list-users.png)

![IAM Account Summary](screenshots/task4-account-summary.png)

---

# Part 5 – Investigating EC2

**Are there any EC2 instances running?** 0

**Are any EC2 Key Pairs configured?** 0

**What information does AWS return for the `t3.micro` instance type?** EbsInfo, EbsOptimizedInfo, MemoryInfo, NetworkInfo, ConnectionTrackingConfiguration, NetworkCards, NitroTpmInfo, SupportedVersions, PlacementGroupInfo, SupportedStrategies, ProcessorInfo

### Screenshots

![Describe Instances](screenshots/task5-describe-instances.png)

![Key Pairs](screenshots/task5-key-pairs.png)

![Instance Types](screenshots/task5-instance-types.png)

---

# Reflection

### 1. Which AWS CLI command did you find most useful?
By now the command **aws ec2 describe-instances** is for me the most useful since it tells you which instances are running without needing to go to AWS console.
---

### 2. Which command output was the easiest to understand?
**aws --version** is really simple and tells you if you have installed aws cli correctly
---

### 3. How does using the AWS CLI compare to navigating the AWS Management Console?
It is more powerful and comfortable to use CLI commands, since you can choose which command windows to use and you are closer to your application files.
---

# Bonus Challenge

**Service Chosen:**

**What does the service do?**

**What problem does it solve?**

**Where do you think it might be used?**
