## Summary
In this exercise you will add some more settings to enable the AWS Lab to be actually more useful.

- From the LOD Dashboard select the Lab Profile ++AWSCloudLab++ and edit that profile.

On the **Cloud page** make the following changes.

In the Stack Deployments section Click **+ Add Stack Deployment**

- Save the Lab Profile, then launch the Lab.

>[!KNOWLEDGE] With the lab now loaded notice that you was automatically logged into the AWS Console.  Select **VPC** from the dashboard, notive the *retry* messages everywhere.  From the search box enter **EC2** and go to the EC2 dashboard, notice the *API Error*.  This is all because AWS works on the default security principle of Deny all so without applying a security template access to everything has been blocked.

- End the Lab and make sure you close both Windows just leaving the original **LDW-Jul22-001: 001 LDW - AWS Cloud** lab running and continue.


Ensure **User1-** is listed with the Role **Contributor**

>[!KNOWLEDGE] LOD provides three levels of user access:    
>**Reader** - Can read all objects in a Resource Group but cannot modify.    
>**Contributor** - Can Read, Create, Modify and Delete objects in a Resource Group.    
>**Owner** - Can manage the security and access to the Resource Group.    
>These groups are very similar to the standard groups, but you will see them created as LODS-rolename.

- Save the Lab Profile

>[!ALERT]You will see an error at the top of the page. This is because we are trying to use an account with write permissions and Lod requires that an Access Control Policy be defined and applied to the Lab Profile.  

- Set the Role for User1- to Reader
- Save the Lab Profile.
- Launch and enter the Lab, signing in with the credentials provided on the resource tab.

- From the Dashboard Click **Resource Groups**  This will generate an error just click on the arrow to the right and the Resource group should be displayed.  
- Click the **Resource Group** to enter it and on the left-hand menu select **Access Control (IAM)**
- Click view my access and notice the results returned.  Close the Windows/Blade that appeared with your access in.
- On the left Click **Overview** followed by **+ Create** on the menu.
- In the Search Box type ++Storage Account++
- Click **Create Storage Account** and fill in the form as follows:

!IMAGE[Create Storage Account](images/image02.jpg)

|||
|---------------|--------------------------|
| Storage Account Name:       | ++sa@lab.LabInstance.Id++    |

- Press **Review + Create**

>[!ALERT]Notice the error.  Click it to view the details and notice it is an access/permissions issue as you only have read access.

Cancel the wizard with the **X** top right.

 - End the Lab and make sure you close both Windows just leaving the original **LDW-Jun22-001: 001 LDW - Azure Cloud** lab running and continue.

- [] This completes the activities for Lab 1 please let your instructor know that you have completed Lab 1

Press **Next** to continue
