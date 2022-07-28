### Testing the new Policy

#### Confirming S3 Buckets can be created

- Launch the Lab Profile **AWS Simple Storage Service S3 Lab**
- Using the search function navigate to the S3 dashboard
- Create a new S3 Bucket using all defaults with a name of ++s3-006-@lab.LabInstance.Id++
- This should create successfully
- Create a second S3 Bucket using all the defaults with the name of ++test-006-@lab.LabInstance.Id++
- This S3 bucket should create successfully.

### Attempt to create a non S3 resource

- In the Search box type ++EC2++ and navigate to the EC2 dashboard.

>[!ALERT] Notice all the API Error messages on the dashboard

- On the left had side select **AMI Catalog**
- In the middle panel select the top AMI named **Amazon Linux 2 AMI (HVM) - Kernel 5.10, SSD Volume Type**

!IMAGE[AMI Selection](images/image6.jpg)

- At the top of the page press the **Launch Instance with AMI** button
- On the next page for the **Name** field enter ++@lab.Variable(initials)-EC2-01++

>[!ALERT] You will see an error at the bottom of the page.

- Press the **Launch Instance** button on the left
- On the next screen choose the **Procced without key pair**
- Then press the **Procced without key pair** button
- You will be noticing lots of errors due to a lack of permissions and otions not being completed because of those lack of permissions 

> End the Lab and make sure you close both Windows just leaving the original **LDW-Jun22-001: 001 LDW - AWS Cloud** lab running and continue.

Press **Next** to continue

