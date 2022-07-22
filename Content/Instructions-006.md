## Introduction

As you saw in the previous exercise the unrestricted policy allowed any potential resource could be created which could mean extreme costs could be incurred as well as increase the chance of the Azure subscription being abused by a threat actor.  In this exercise we will assume the requirement is to only allow the creation of an AWS Lab Profile that allows only Simple Storage Service (S3) resources to be created.

### Updating the Access Control Policy

- From within LOD ensure the AWSCloudLab, Lab Profile is being displayed.
- Edit the Lab Profile and use the **SaveAs** function to save the new Lab Profile with a name of ++AWS Simple Storage Service S3 Lab++
- Make this new Lab Profile a favourite so it is easy to find
- Edit this new Lab Profile
- On the **Cloud** page remove the old Access Control Policy and add the policy ++LDW - JUL22 S3 Only++

```AWS-ACP-nocopy
{
    "Version": "2012-10-17",
    "Statement": [
        {
	   "Effect": "Allow",
            "Action": "s3:*",
            "Resource": "*"
        }
    ]
}
```

- Save the Lab Profile

### Testing the new Policy

#### Confirming S3 Buckets can be created

- Launch the Lab Profile **AWS Simple Storage Service S3 Lab**
- Using the search function navigate to the S3 dashboard
- Create a new S3 Bucket using all defaults with a name of s3-@lab.LabInstance.Id
- This should create successfully
- Create a second S3 Bucket using all the defaults with the name of test-@lab.LabInstance.Id
- This S3 bucket shoukd create successfully.

### Attempt to create a non S3 resource

- In the Search box type ++ec2++ and navigate to the ec2 dashboard.

>[!ALERT] Notice all the API Error messages on the dashboard

- On the left had side select **AMI Catalog**
- In the middle panel select the top AMI named **Amazon Linux 2 AMI (HVM) - Kernel 5.10, SSD Volume Type**

!IMAGE[AMI Selection](images/image6.jpg)

- At the top of the page press the **Launch Instance with AMI** button
- On the next page for the **Name** field enter ++@lab.Variable(initials)-ec2-01++
- Press the **Launch Instance** button on the left
- On the next screen choose the **Procced without key pair**
- Then press the **Procced without key pair** button
- You will be noticing lots of errors due to a lack of permissions
- Attempt to press the **launch Instance** button again and notice the additional errors

- End the Lab and make sure you close both Windows just leaving the original **LDW-Jun22-001: 001 LDW - AWS Cloud** lab running and continue.

Press **Next** to continue

