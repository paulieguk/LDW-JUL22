## Introduction

The previous lab blocked the ability to create all resources except S3 buckets.
To demonstrate a further restriction function in this lab a new ACP will be
applied but this time the ACP will also enforce a naming convention on the s3
bucket being created.

### Updating the Access Control Policy

-   From within LOD ensure the **AWS Simple Storage Service S3 Lab**, Lab
    Profile is being displayed.

-   Edit the Lab Profile.

-   On the Cloud page remove the old Access Control Policy and add the policy
    ++LDW-JUL22 S3 Name Prefix S3++. This policy enforces a rule that when an S3
    bucket is created the name has to start with the prefix s3

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~ AWSACP-nocopy
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Action": "s3:*",
      "Effect": "Allow",
      "Resource": "*"
    },
    {
      "Action": [
        "s3:CreateBucket"
      ],
      "Effect": "Deny",
      "NotResource": "arn:aws:s3:::s3*"
      }
  ]
}
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

-   Save the Lab Profile

### Testing the new Policy

---

#### Confirming S3 Buckets can be created

-   Launch the Lab Profile **AWS Simple Storage Service S3 Lab**

-   Using the search function navigate to the S3 dashboard

-   Create a new S3 Bucket using all defaults with a name of ++s3-007-@lab.LabInstance.Id++

-   This should create successfully

-   Create a second S3 Bucket using all the defaults with the name of ++test-007-@lab.LabInstance.Id++

-   This S3 bucket should fail to be created

> End the Lab and make sure you close both Windows just leaving the original
    LDW-Jun22-001: 001 LDW - AWS Cloud lab running and continue.

-   [] This completes the activities for Lab 2 please let your instructor know
    that you have completed Lab 2

Press Next to continue
