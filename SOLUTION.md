# AWS CLI Basics - Solution

Name: Julio Aldana

GitHub Username: Jcaldana97

---

# Task 1 - Verify AWS CLI

## aws --version

```aws-cli/2.35.11 Python/3.14.5 Windows/11 exe/AMD64

```

### Screenshot

![Task 1](screenshots/task1-aws-version.png)

---

# Task 2 - AWS Configuration

## aws configure list

```NAME       : VALUE                    : TYPE             : LOCATION
profile    : <not set>                : None             : None
access_key : ****************DG3T     : shared-credentials-file : 
secret_key : ****************tzwJ     : shared-credentials-file : 
region     : us-east-1                : config-file      : ~/.aws/config

```

### Screenshot

![Task 2](screenshots/task2-configure-list.png)

---

# Task 3 - Caller Identity

## aws sts get-caller-identity

```{                                                                                 
    "UserId": "AIDA4COT7F5XWDL6SF5LE",
    "Account": "829910101871",
    "Arn": "arn:aws:iam::829910101871:user/julioaldana"
}

```

### Screenshot

![Task 3](screenshots/task3-caller-identity.png)

---

# Task 4 - AWS Regions

Number of Regions: 17

Default Region: us-east-1

Closest Region: eu-central-1 (Germany)

### Screenshot

![Task 4](screenshots/task4-regions.png)

---

# Task 5 - Availability Zones

Number of AZs: 6

Why are multiple AZs important? To have more resources available in case one server is overloaded.

### Screenshot

![Task 5](screenshots/task5-availability-zones.png)

---

# Task 6 - S3 Investigation

Buckets: 0

Reason if none exist: No S3 bucket has been created.

### Screenshot

![Task 6](screenshots/task6-s3-buckets.png)

---

# Task 7 - IAM Investigation

IAM Users: 1

Why avoid using the root account? Because with IAM users you can control the permisions the user has, reducing the security risks. 

### Screenshot

![Task 7](screenshots/task7-iam-users.png)

---

# Task 8 - EC2 Investigation

Running Instances: 0

Key Pairs: 0

Instance Types: EbsInfo, EbsOptimizedInfo, MemoryInfo, NetworkInfo, ConnectionTrackingConfiguration, NetworkCards, NitroTpmInfo, SupportedVersions, PlacementGroupInfo, SupportedStrategies, ProcessorInfo

### Screenshot

![Task 8](screenshots/task8-ec2-info.png)

---

# Task 9 - Output Formats

Preferred format: Table

Reason: Most readable format for humans

### Screenshot

![Task 9](screenshots/task9-output-formats.png)

---

# Reflection

1. Which AWS CLI command did you find most useful?
Ans: By now the command **aws ec2 describe-instances** is for me the most useful since it tells you which instances are running without needing to go to AWS console.

2. Which command output was the easiest to understand?
Ans: **aws --version** is really simple and tells you if you have installed aws cli correctly

3. How does using the AWS CLI compare to navigating the AWS Management Console?
Ans: It is more powerful and comfortable to use CLI commands, since you can choose which command windows to use and you are closer to your application files. 

---

# Bonus

### Screenshot

![Bonus](screenshots/bonus-vpc.png)
