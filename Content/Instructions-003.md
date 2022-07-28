## Introduction

In this exercise you will add some more settings to enable the AWS Lab to be
actually more useful.

-   From the LOD Dashboard select the Lab Profile ++AWSCloudLab++ and edit that
    profile.

On the **Cloud page** make the following changes.

In the Stack Deployments section Click **+ Add Stack Deployment**

-   Save the Lab Profile, then launch the Lab.

>   [!NOTE] With the lab now loaded notice that you are automatically logged
>   into the AWS Console. Select **VPC** from the dashboard, notice the *retry*
>   messages everywhere. From the search box enter **EC2** and go to the EC2
>   dashboard, notice the *API Error*. This is all because AWS works on the
>   default security principle of Deny all so without applying a security
>   template access to everything has been blocked.

>End the Lab and make sure you close both Windows just leaving the original
    **LDW-Jul22-001: 001 LDW - AWS Cloud** lab running and continue.

>   [!KNOWLEDGE] LOD enables the ability to create user accounts in an AWS
>   Organisation. In most scenarios these are not required as the automatically
>   created account meets the requirements when creating AWS Lab. The primary
>   reason you might create user accounts is when you want to simulate different
>   users having access to different Stack Deployments.  
>   When a User Account has been added it can then be assigned to the Stack by
>   clicking the **+ Add Permission** link within the Stack section.

### Lets assign some access

You will start by assigning a development Access Control Policy as that will
allow all access. This policy is Skillable managed and not allowed in
production.

-   From the LOD Dashboard select the Lab Profile ++AWSCloudLab++ and edit that
    profile.

-   On the Cloud page click **+Add Policy** in the Access Control Policies section

-   Select the **LOD Managed - Allow All (DEVELOPEMENT ONLY - AWS)**

-   Save the Lab Profile, then launch the lab.

With the lab launched notice the following:

>  - [] Automatically logged on

>  - [] Search for EC2 and view the EC2 Dashboard - No errors

>  - [] Search for VPC and view the VPC dashboard again no errors and all values set at **0**

> End the lab

Now you will add the default VPC resources to see what that does.

-   From the LOD Dashboard select the Lab Profile ++AWSCloudLab++ and edit that
    profile.

-   On the Cloud page tick the **Deploy Default VPC**

-   Save the Lab Profile, then launch the lab.

Once the Lab has started and the console is displayed click VPC from the
dashboard or type ++VPC++ in the search to view the VPC dashboard. Notice the
VPC dashboard now shows a VPC, Subnets, security objects, etc. objects have been
created.

!IMAGE[VPC Objects](images/image2.jpg)

---

> Remember the VPC had the following default configuration: 

---

 !IMAGE[AWS Default VPC](images/image4.jpg)

-   Click **Subnets** on the left and noticed the three subnets that have been
    created including their IP Address ranges, as discussed earlier.

!IMAGE[Subnets in the VPC](images/image3.jpg)

Press **Next** to continue
