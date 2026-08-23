# Cloud Infrastructure Components

## Compute Resources

**Purpose:** Compute resources provide the processing capability required to run programs, applications, and the operating system. They can be provided through virtual machines, containers, or serverless computing.

**Why it matters in cloud computing:** Compute power is necessary for applications and services to function. Cloud providers allow users to adjust their computing resources depending on their needs, such as increasing CPU, RAM, or the number of virtual machines.

**Relation to KillerCoda:** KillerCoda provides a virtual machine that acts as a compute resource. It gives users a ready-to-use Linux environment without needing a physical computer or server.

## Storage Resources

**Purpose:** Storage resources are used to save the operating system, applications, files, and other information. Cloud storage can be categorized into object, block, and file storage.

**Why it matters in cloud computing:** Cloud storage offers a reliable and flexible way to keep data. It can expand when more space is needed and can protect information by storing it across different systems.

**Relation to KillerCoda:** The storage displayed through `df -h` represents the disk space available to the KillerCoda virtual machine. This is similar to the storage volume connected to a virtual machine in AWS, Azure, or Google Cloud.

## Networking Resources

**Purpose:** Networking resources allow different systems and services to communicate with each other and connect with users. Examples include virtual networks, routers, firewalls, and load balancers.

**Why it matters in cloud computing:** Networking makes it possible for cloud resources to communicate and allows users to access applications and services. It also helps protect systems by controlling network access.

**Relation to KillerCoda:** The KillerCoda environment has a hostname and IP address, which can be checked using `hostname` and `hostname -I`. These identify the virtual machine within its network and allow it to communicate through the cloud infrastructure.

## Operating System

**Purpose:** The operating system controls system resources, manages applications, and provides the interface used to interact with the computer.

**Why it matters in cloud computing:** Linux is commonly used for cloud servers because it is lightweight, stable, flexible, and widely supported. It provides the platform where administrators can configure and manage cloud services.

**Relation to KillerCoda:** The KillerCoda environment runs **Ubuntu 24.04.4 LTS**, which was verified using `cat /etc/os-release`. Ubuntu is also commonly used on cloud virtual machines provided by platforms such as AWS, Azure, and Google Cloud.
