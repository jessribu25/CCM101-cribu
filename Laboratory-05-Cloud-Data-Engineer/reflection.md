# Reflection

### 1. Why is object storage better suited for storing millions of photos compared to a traditional block storage hard drive?

Block storage works like a regular hard drive connected to a virtual machine, making it useful for applications that need fast and structured data access. However, it is not ideal for handling millions of unstructured files. Object storage is designed to store large amounts of data in scalable buckets, with each file stored as an object with its own ID and metadata. Because of this, it is more suitable for applications that mainly need to store and retrieve large numbers of photos.

### 2. How did using Docker make it easier to deploy the MinIO storage server?

Docker made the deployment much simpler because I did not have to manually install MinIO and configure all of its requirements. With a single Docker command, I could create and run the MinIO server. The environment variables were used to set the login credentials, while the port options allowed me to access the service. This made the setup faster and easier to repeat.

### 3. What is a "bucket" in the context of cloud storage?

A bucket is a main storage container used in object storage to hold files or objects. It is similar to a folder in the sense that it keeps related files together, but it does not work exactly like a traditional file system. The objects inside the bucket are identified using unique names or IDs instead of relying on a normal folder structure.

### 4. How do you think large enterprise companies ensure their object storage data is not lost if the physical server crashes?

Large companies can protect their data by creating multiple copies and storing them across different drives, servers, or even locations. This process, known as data replication, helps prevent a single hardware failure from causing permanent data loss. They can also use separate backups to protect against accidental deletion, corruption, or other problems that could affect the original data.

### 5. How is your confidence in navigating the Linux command line growing?

After completing five labs, I feel more comfortable using the Linux terminal than I did at the beginning. Commands such as `ls` and `cd`, which were unfamiliar to me during the first lab, now feel much easier to use. Being able to deploy and manage a working server using Docker commands has also made me less nervous about using the command line. I now see the terminal as a useful tool for completing cloud and server-related tasks.

**Reference:**
University of Eastern Pangasinan – College of Information Technology. (2026). **CCM101 – Cloud Computing, Midterm Module, Chapter 5.**
