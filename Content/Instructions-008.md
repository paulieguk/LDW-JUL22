## Introduction

Having built Labs that allow a user to access the AWS console but have no
resources provision (other than a default VPC), in this lab you will attach
templates to build objects as get access to those objects.

### Adding an S3 Template

As per the demonstration earlier you will add a template that contains the same
content to provision and S3 bucket.

-   Edit the ++AWS Simple Storage Service S3 Lab++ Lab Profile

-   On the **Cloud** page in the **Stack Deployments** section add the
    **Resource Template** ++aws s3 bucket no name++

-   Save the Lab Profile

The Resource Template contains the JSON below. One thing to notice when you have
been creating S3 buckets you have had to supply a name, notice the JSON file
does not contain the name field. So, what will happen about the s3 Bucket name?

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~ AWSTemplate-nocopy
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
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

-   Launch the Lab Profile

-   Navigate to the S3 dashboard and notice the S3 Bucket name

>   [!ALERT] The first participant to either shout out or enter into chat, the
>   name format wins a prize!

-   End the Lab

-   Press **Next** to continue
