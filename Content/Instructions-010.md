### Introduction

We user a AWS Resource Template in Lab 3 that had a lab variable placed into the
template. This approach is fine if you always want the same generated value
being used in the template for every lab. But what if the requirement was to use
different string prefixes for example in different labs. Multiple templates
could be created, and the **JOIN** function could be used. This would require
every Resource Template and Lab Profile to go through security review which
cloud impact development. An alternative option would be to configure the field
as a parameter. In this scenario the Lab Profile can then have the parameter
customised on a per Lab Profile. This way multiple templates do not need to be
managed and reviewed if edited.

-   Edit the ++AWS Simple Storage Service S3 Lab++ Lab Profile

-   On the **Cloud** page in the **Stack Deployments** section add a third
    **Resource Template** ++AWS S3 Bucket with Parameter++
    
-   On the parameter page enter s3-&#64;lab.LabInstance.Id, click OK.

-   Save the Lab Profile

The Resource Template contains the JSON below. Notice this file has a Parameter at the top.  The parameter is called *BucketNameParam* and is referenced in the resources section on the *BucketName* lineone has a BucketName.

```AWSTemplate-nocopy
{
  "AWSTemplateFormatVersion" : "2010-09-09",

  "Description" : "Sample template showing how to create a publicly accessible S3 bucket with a deletion policy of retain on delete.",

  "Parameters" : {
  "BucketNameParam" : {
    "Type" : "String",
    "Description" : "Name for the S3 Bucket.  It must start with a lowercase letter."
  }
},

  "Resources" : {
    "S3Bucket" : {
      "Type" : "AWS::S3::Bucket",
      "Properties" : {
        "AccessControl" : "PublicRead",
        "BucketName" : { "Ref" : "BucketNameParam" }
      },
      "DeletionPolicy" : "Delete"
    }
  }
}
```

-   Launch the Lab Profile

-   When launched notice three buckets now exist and notice the name of the
    third one. The second and third S3 buckets are based on the Lab Instance Id
    therefore, the suffix number should be the same.

>End the Lab

Press **Next to continue**
