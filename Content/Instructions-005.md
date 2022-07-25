## Introduction

During this exercise you will confirm the current policy does not restrict the ability to create any supported AWS resource 

### Testing the Policy

#### Confirming S3 Buckets can be created

- Launch the Lab Profile **AWSCloudLab**
- Using the search function navigate to the S3 dashboard
- Create a new S3 Bucket using all defaults with a name of ++s3-@lab.LabInstance.Id++
- This bucket should create successfully
- Create a second S3 Bucket using all the defaults with the name of ++test-@lab.LabInstance.Id++
- This S3 bucket should create successfully.

### Attempt to create a non S3 resource

- In the Search box type ++ec2++ and navigate to the **ec2 dashboard**.
- On the left had side select **AMI Catalog**
- In the middle panel select the top AMI named **Amazon Linux 2 AMI (HVM) - Kernel 5.10, SSD Volume Type**

!IMAGE[AMI Selection](images/image6.jpg)

- At the top of the page press the **Launch Instance with AMI** button
- On the next page for the **Name** field enter ++@lab.Variable(initials)-ec2-01++
- Press the **Launch Instance** button on the left
- On the next screen choose the **Procced without key pair**
- Then press the **Procced without key pair** button
- Attempt to press the **Launch Instance** button again the ec2 Instance should launch.  This can be confirmed on the ec2 Instances dashboard.  

Wait for the **Instance State** to be displayed as running and having passed both the **Status Checks**.  This might take a few minutes.

- End the Lab and make sure you close both Windows just leaving the original **LDW-Jul22-001: 001 LDW - AWS Cloud** lab running and continue.

Press **Next** to continue

