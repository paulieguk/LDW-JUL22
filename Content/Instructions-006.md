## Introduction

As you saw in the previous exercise the unrestricted policy allowed any potential resource could be created which could mean extreme costs could be incurred as well as increase the chance of the AWS subscription being abused by a threat actor, crypto miner or other individual.  In this exercise we will assume the requirement is to only allow the creation of an AWS Lab Profile that allows only Simple Storage Service (S3) resources to be created.

### Updating the Access Control Policy

- From within LOD ensure the AWSCloudLab, Lab Profile is being displayed.
- Edit the Lab Profile and use the **SaveAs** function to save the new Lab Profile with a name of ++AWS Simple Storage Service S3 Lab++
- Make this new Lab Profile a favourite so it is easy to find
- Edit this new Lab Profile
- On the **Cloud** page remove the old Access Control Policy and add the policy ++LDW - JUL22 S3 Only++

```AWSACP-nocopy
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

Press **Next** to continue

