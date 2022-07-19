
## Summary
You will build an AWS Lab Profile with the absolute minimal settings

- From the Skillable Dashboard Create a new lab profile then from the Template Gallery use the **+ Create Custom Environment** option.  When creating the new Lab Profile use the following information:

**Basic Page**

|||
|---------------|--------------------------|
| Number:       | ++@lab.Variable(initials)++  |
| Name:         | ++AWSCloudLab++ |
| Series:       | LDW-JUL22                |
| Organisation: | LDW-JUL22                |
| Virtualization Platform: | None |

**Cloud Page**

|||
|---------------|--------------------------|
| Cloud Platform:       | AWS                     |
| Enable Automatic Login | Selected |
| Subscription Pool:    | Career RockIT |
| Datacenter Availability | US East (Ohio) |
| User Accounts | Remove the User1 account (click the **X** on the right |

>[!Knowledge] This represents the minimum data that can be entered into an AWS Cloud Lab Profile.  If you attended the Azure Cloud Slice what setting did Azure Require but AWS does not?

- Save the Lab Profile.
- From the top of the Lab Profile click the **Favourite** star

 - Launch the Lab.  A few things to note:
    - No Credentials allocated
    - Not automatically logged in
- This Lab is pretty much useless

>[!KNOWLEDGE] An AWS Cloud Slice Lab will allocate an account from the Subscription Pool.  But for this to happen a Stack has to be deployed (even if empty). 
!IMAGE[AWS Subscription Pool](images/image01.jpg)
 
 - End the Lab and make sure you close both Windows just leaving the original **LDW-Jul22-001: 001 LDW - AWS Cloud** lab running and continue.

Press **Next** to continue
