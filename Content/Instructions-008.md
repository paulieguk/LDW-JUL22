## Introduction

Having built Labs that allow a user to access the AWS console but have no resources provision (other than a default VPC), in this lab you will attached templates to build objects as get access to those objects.

### Adding an S3 Template

As per the demonstration earlier you will add a template that conatins the same content to provision and S3 bucket.

- Edit the ++AWS Simple Storage Service S3 Lab++ Lab Profile
- On the **Cloud** page in the **Stack Deployments** section add the **Resource Template** ++aws s3 bucket no name++
- Save the Lab Profile

The Resource Template conatins the JSON below.  One thing to notice when you have been creating S3 buckets you have had to supply a nam, notive the JSON file does not contain the name field.  So what will happen about the s3 Bucket name?

```AWSTemplate-nocopy
{
  "AWSTemplateFormatVersion" : "2010-09-09",

  "Description" : "Sample template showing how to create a publicly accessible S3 bucket with a deletion policy of retain on delete.",

  "Resources" : {
    "S3Bucket" : {
      "Type" : "AWS::S3::Bucket",
      "Properties" : {
        "AccessControl" : "PublicRead"
      },
      "DeletionPolicy" : "Delete"
    }
  }
}
```

- Launch the Lab Profile
- Navigate to the S3 dashboard and notice the S3 Bucket name

>[!ALERT] The first partcipant to either shout out or enter into chat, the name format wins a prize!

- End the Lab

This time you will add a second resource template that specifies the name.

- Edit the ++AWS Simple Storage Service S3 Lab++ Lab Profile
- On the **Cloud** page in the **Stack Deployments** section add a second **Resource Template** ++AWS S3 Bucket with Lab Instance++
- Save the Lab Profile 

The Resource Template conatins the JSON below.  One thing to notice when you have been creating S3 buckets you have had to supply a name, notice the JSON file does not contain the name field.  So what will happen about the s3 Bucket name?

```AWSTemplate-nocopy
{
  "AWSTemplateFormatVersion" : "2010-09-09",

  "Description" : "Sample template showing how to create a publicly accessible S3 bucket with a deletion policy of retain on delete.",

  "Resources" : {
    "S3Bucket" : {
      "Type" : "AWS::S3::Bucket",
      "Properties" : {
        "AccessControl" : "PublicRead",
        "BucketName" : "labinstances3-&#x40lab.LabInstance.Id"
      },
      "DeletionPolicy" : "Delete"
    }
  }
}
```

- Launch the Lab Profile
- When launched notice two buckets now exist and notice the name of the second one
- Create a third S3 Bucket using all defaults with a name of s3-@lab.LabInstance.Id
- This bucket should create successfully
- Create a fourth S3 Bucket using all defaults with a name of testbucket-@lab.LabInstance.Id
- This bucket should **not** create successfully as the ACP is still in place enforcing a naming scheme.  But notice the template deployed resources whee not impacted by the ACP.

- [] This completes the activities for Lab 3 please let your instructor know that you have completed Lab 3

Press **End** to complete this set of labs.
