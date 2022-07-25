This time you will add a second resource template that specifies the name.

-   Edit the ++AWS Simple Storage Service S3 Lab++ Lab Profile

-   On the **Cloud** page in the **Stack Deployments** section add a second
    **Resource Template** ++AWS S3 Bucket with Lab Instance++

-   Save the Lab Profile

The Resource Template contains the JSON below. Notice this one has a BucketName
which is using the **li-s3-** followed by the @lab.LabInstance.Id parameter

!IMAGE[AWS Template](images/image10.jpg

-   Launch the Lab Profile

-   When launched notice two buckets now exist and notice the name of the second
    one

-   Create a third S3 Bucket using all defaults with a name of
    \++s3-@lab.LabInstance.Id++

-   This bucket should create successfully

-   Create a fourth S3 Bucket using all defaults with a name of
    \++testbucket-@lab.LabInstance.Id++

-   This bucket should **not** create successfully as the ACP is still in place
    enforcing a naming scheme. But notice the template deployed resources where
    not impacted by the ACP.

-   [] This completes the activities for Lab 3 please let your instructor know
    that you have completed Lab 3

Press **End** to complete this set of labs.
