# AWS CLI Basics - Solution

**Name: Hafiz Abdul Quddus**

**GitHub Username: HafizAQ ([github.com/HafizAQ](https://github.com/HafizAQ))**

---

# Part 1 – Verify AWS CLI Installation

## Command Output

### aws --version

```text
aws-cli/2.35.11 Python/3.14.5 Linux/5.15.167.4-microsoft-standard-WSL2 exe/x86_64.ubuntu.24
```

### aws configure list

```text
NAME       : VALUE                    : TYPE             : LOCATION
profile    : <not set>                : None             : None
access_key : ****************6I6U     : shared-credentials-file : 
secret_key : ****************Pfe1     : shared-credentials-file : 
region     : us-east-1                : config-file      : ~/.aws/config
```

### aws sts get-caller-identity

```text
{
    "UserId": "AIDAS62N5DSUQ4PDSWNWE",
    "Account": "203637464233",
    "Arn": "arn:aws:iam::203637464233:user/hquddus"
}
```

### Screenshots

![AWS Version](screenshots/task1-aws-version.png)

![AWS Configure List](screenshots/task1-configure-list.png)

![Caller Identity](screenshots/task1-caller-identity.png)

---

# Part 2 – AWS Account Information

Answer the following:

**AWS Account ID:** 203637464233(UserId: AIDAS62N5DSUQ4PDSWNWE)

**IAM User ARN:** arn:aws:iam::203637464233:user/hquddus

**Default Region:** us-east-1

**Configured Output Format:** json

### Screenshot

![Account Information](screenshots/task2-account-information.png)

---

# Part 3 – AWS Regions & Availability Zones

## Regions

**How many AWS Regions are available?** 

17

**Which Region is configured as your default?**

us-east-1

### Screenshot

![AWS Regions](screenshots/task3-regions.png)

---

## Availability Zones

**How many Availability Zones exist in your current Region?** 

6

**Why should production workloads use multiple Availability Zones?**

Production workloads should use multiple Availability Zones to improve availability, reliability, and fault tolerance. If one Availability Zone fails, the application can continue running from another Availability Zone without downtime.

### Screenshot

![Availability Zones](screenshots/task3-availability-zones.png)

---

# Part 4 – Investigating IAM

**How many IAM users exist?** 

1

**Why is using IAM users safer than using the root account?**

Using IAM users is safer because the root account has complete access to all AWS services and account settings. If root credentials are stolen, the entire AWS account can be compromised.

### Screenshots

![IAM Users](screenshots/task4-list-users.png)

![IAM Account Summary](screenshots/task4-account-summary.png)

---

# Part 5 – Investigating EC2

**Are there any EC2 instances running?**

No ("Reservations": [])

**Are any EC2 Key Pairs configured?**

No ("KeyPairs": [])

**What information does AWS return for the `t3.micro` instance type?**


---

|                    DescribeInstanceTypes                    |
+-------------------------------------------------------------+
||                       InstanceTypes                       ||
|+----------------------------------------+------------------+|
||  AutoRecoverySupported                 |  True            ||
||  BareMetal                             |  False           ||
||  BurstablePerformanceSupported         |  True            ||
||  CurrentGeneration                     |  True            ||
||  DedicatedHostsSupported               |  True            ||
||  FreeTierEligible                      |  True            ||
||  HibernationSupported                  |  True            ||
||  Hypervisor                            |  nitro           ||
||  InstanceStorageSupported              |  False           ||
||  InstanceType                          |  t3.micro        ||
||  NitroEnclavesSupport                  |  unsupported     ||
||  NitroTpmSupport                       |  supported       ||
||  PhcSupport                            |  unsupported     ||
||  RebootMigrationSupport                |  supported       ||
||  SupportedInRegion                     |  True            ||
|+----------------------------------------+------------------+|
|||                         EbsInfo                         |||
||+-------------------------------------+-------------------+||
|||  AttachmentLimitType                |  shared           |||
|||  EbsOptimizedSupport                |  default          |||
|||  EncryptionSupport                  |  supported        |||
|||  MaximumEbsAttachments              |  27               |||
|||  NvmeSupport                        |  required         |||
||+-------------------------------------+-------------------+||
||||                   EbsOptimizedInfo                    ||||
|||+---------------------------------------+---------------+|||
||||  BaselineBandwidthInMbps              |  87           ||||
||||  BaselineIops                         |  500          ||||
||||  BaselineThroughputInMBps             |  10.875       ||||
||||  MaximumBandwidthInMbps               |  2085         ||||
||||  MaximumIops                          |  11800        ||||
||||  MaximumThroughputInMBps              |  260.625      ||||
|||+---------------------------------------+---------------+|||
|||                       MemoryInfo                        |||
||+-----------------------------------+---------------------+||
|||  SizeInMiB                        |  1024               |||
||+-----------------------------------+---------------------+||
|||                       NetworkInfo                       |||
||+-----------------------------------+---------------------+||
|||  DefaultNetworkCardIndex          |  0                  |||
|||  EfaSupported                     |  False              |||
|||  EnaSrdSupported                  |  False              |||
|||  EnaSupport                       |  required           |||
|||  EncryptionInTransitSupported     |  False              |||
|||  FlexibleEnaQueuesSupport         |  unsupported        |||
|||  Ipv4AddressesPerInterface        |  2                  |||
|||  Ipv6AddressesPerInterface        |  2                  |||
|||  Ipv6Supported                    |  True               |||
|||  MaximumNetworkCards              |  1                  |||
|||  MaximumNetworkInterfaces         |  2                  |||
|||  NetworkPerformance               |  Up to 5 Gigabit    |||
|||  SecondaryNetworkSupported        |  False              |||
||+-----------------------------------+---------------------+||
||||            ConnectionTrackingConfiguration            ||||
|||+-----------------------------------------+-------------+|||
||||  DefaultTcpEstablishedTimeout           |  432000     ||||
||||  DefaultUdpStreamTimeout                |  180        ||||
||||  DefaultUdpTimeout                      |  30         ||||
|||+-----------------------------------------+-------------+|||
||||                     NetworkCards                      ||||
|||+-----------------------------------+-------------------+|||
||||  BaselineBandwidthInGbps          |  0.064            ||||
||||  DefaultEnaQueueCountPerInterface |  2                ||||
||||  MaximumNetworkInterfaces         |  2                ||||
||||  NetworkCardIndex                 |  0                ||||
||||  NetworkPerformance               |  Up to 5 Gigabit  ||||
||||  PeakBandwidthInGbps              |  5.0              ||||
|||+-----------------------------------+-------------------+|||
|||                      NitroTpmInfo                       |||
||+---------------------------------------------------------+||
||||                   SupportedVersions                   ||||
|||+-------------------------------------------------------+|||
||||  2.0                                                  ||||
|||+-------------------------------------------------------+|||
|||                   PlacementGroupInfo                    |||
||+---------------------------------------------------------+||
||||                  SupportedStrategies                  ||||
|||+-------------------------------------------------------+|||
||||  partition                                            ||||
||||  spread                                               ||||
|||+-------------------------------------------------------+|||
|||                      ProcessorInfo                      |||
||+-------------------------------------------+-------------+||
|||  Manufacturer                             |  Intel      |||
|||  SustainedClockSpeedInGhz                 |  2.5        |||
||+-------------------------------------------+-------------+||
||||                SupportedArchitectures                 ||||
|||+-------------------------------------------------------+|||
||||  x86_64                                               ||||
|||+-------------------------------------------------------+|||
|||                   SupportedBootModes                    |||
||+---------------------------------------------------------+||
|||  legacy-bios                                            |||
|||  uefi                                                   |||
||+---------------------------------------------------------+||
|||                SupportedRootDeviceTypes                 |||
||+---------------------------------------------------------+||
|||  ebs                                                    |||
||+---------------------------------------------------------+||
|||                  SupportedUsageClasses                  |||
||+---------------------------------------------------------+||
|||  on-demand                                              |||
|||  spot                                                   |||
||+---------------------------------------------------------+||
|||              SupportedVirtualizationTypes               |||
||+---------------------------------------------------------+||
|||  hvm                                                    |||
||+---------------------------------------------------------+||
|||                        VCpuInfo                         |||
||+-----------------------------------------------+---------+||
|||  DefaultCores                                 |  1      |||
|||  DefaultThreadsPerCore                        |  2      |||
|||  DefaultVCpus                                 |  2      |||
||+-----------------------------------------------+---------+||
||||                      ValidCores                       ||||
|||+-------------------------------------------------------+|||
||||  1                                                    ||||
|||+-------------------------------------------------------+|||
||||                  ValidThreadsPerCore                  ||||
|||+-------------------------------------------------------+|||
||||  1                                                    ||||
||||  2                                                    ||||
|||+-------------------------------------------------------+|||

### Screenshots

![Describe Instances](screenshots/task5-describe-instances.png)

![Key Pairs](screenshots/task5-key-pairs.png)

![Instance Types](screenshots/task5-instance-types.png)

---

# Reflection

### 1. Which AWS CLI command did you find most useful?

The most useful command was

    aws configure list

It helps in troubleshooting connection and permission issues.

---

### 2. Which command output was the easiest to understand?

The easiest command output to understand was:

    aws ec2 describe-availability-zones --output table

because the table format clearly shows the Availability Zones available in the current AWS Region.

---

### 3. How does using the AWS CLI compare to navigating the AWS Management Console?

AWS Console is better for learning and visualization, while AWS CLI is better for automation and quick cloud management.

---

# Bonus Challenge: NA

**Service Chosen:**

**What does the service do?**

**What problem does it solve?**

**Where do you think it might be used?**
