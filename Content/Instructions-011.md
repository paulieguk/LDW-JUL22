### Introduction

This lab will look at the Geo-Location features when launcing a Lab from LOD.  When multiple Datacenters are listed LOD will provision the AWS Stack in the closet possible location to the user.  When resources are provisioned into that stamp they will autolocate into the same region.  In most instances implementing geo-location is as simple as adding confirming the resource is a available in the regions you wish to use and then adding the locations to the LOD Cloud Page.

This time you will add a second location or change the locations in the template.

Are you located outside the USA?  @lab.DropDownList(location)[null,yes,no]

:::ROW(location=yes)

- Edit the ++AWS Simple Storage Service S3 Lab++ Lab Profile
- On the Cloud page in the Stack Deployments section add a second Datacenter closer to your location
- Save the Lab Profile
- Launch the Lab Profile

When the Lab launches review the location information in the AWS Portal title bar and the location information in the LOD Lab Client on the resources page.  They should be no US locations.  for example: 

!IMAGE[AWS Region](images/image6.jpg

:::

:::USA(location=no)

- Edit the ++AWS Simple Storage Service S3 Lab++ Lab Profile
- On the Cloud page in the Stack Deployments remove the **US East (Ohio)** Datacenter and add either Europe London or Asia Singapoore locations
- Save the Lab Profile
- Launch the Lab Profile

When the Lab launches review the location information in the AWS Portal title bar and the location information in the LOD Lab Client on the resources page.  They should be the location you selected.  for example: 

!IMAGE[AWS Region](images/image7.jpg

- End the Lab
- Edit the ++AWS Simple Storage Service S3 Lab++ Lab Profile
- On the Cloud page in the Stack Deployments add the **US East (Ohio)** Datacenter back in.
- Save the Lab Profile
- Launch the Lab Profile

When the Lab launches you should be automatically connected to the US East location again.

!IMAGE[AWS Region](images/image8.jpg

:::

- End the Lab
