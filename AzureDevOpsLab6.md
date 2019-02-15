# Lab 6: Extend the release pipeline

The release pipeline can be extended to encompass additional stages and approvals.

# Step 1: Add a QA stage

Navigate to the pipeline (Pipelines | Releases) and select Edit:

<img src="images/Lab6_1.jpg" width="624"/>

Move the mouse over the dev stage and select Clone:

<img src="images/Lab6_2.jpg" width="624"/>

Click on the Copy of Dev title, rename the stage to QA and close the window:

<img src="images/Lab6_3.jpg" width="624"/>

Click on the 1 job, 4 tasks link in the newly created QA stage:

<img src="images/Lab6_4.jpg" width="624"/>

Edit the provisioning task to and make three changes to create an entirely separate QA web application from the Dev web application:

* Change the resource group name to a new one e.g. with QA in the name.
* Change the name of the web app.
* Change the name of the app service plan.

<img src="images/Lab6_5.jpg" width="624"/>

Edit the deployment task to reference the same name as set in the provisioning step above:

<img src="images/Lab6_6.jpg" width="624"/>

Save the changes to the QA tasks:

<img src="images/Lab6_7.jpg" width="624"/>

# Step 2: Add a pre-deployment approval to the QA stage

Select the pipeline view:

<img src="images/Lab6_8.jpg" width="624"/>

Click on the pre-deployment conditions area of the QA environment:

<img src="images/Lab6_9.jpg" width="624"/>

Make the following changes:

- Toggle the Enable pre-deployment approvals switch so that approvals are required.
- Add at least one user or group. There will be a project group that you are already a member of with the same name as the project, add this, and also your own identity.
- Set the approval order to Any one user.
- Ensure that "The user requesting a release or deployment should not approve it" check box is clear. This is a good setting in practice but for the lab it would prevent you from approving your own releases.
- Close the settings by clicking on the cross.

<img src="images/Lab6_10.jpg" width="624"/>

Save the changes and create a release manually to test the changes:

<img src="images/Lab6_11.jpg" width="624"/>

Keep the defaults (although note the options to limit the stages deployed to and to select the artifact versions) and clicj Create:

<img src="images/Lab6_12.jpg" width="624"/>

Click on the release link to watch the release:

<img src="images/Lab6_13.jpg" width="624"/>

Wait until the dev stage is complete and then notice that an approval is pending for the QA stage. The approvers will receive an email notification and can also be notified via other tools such as Teams or Slack. Click on the pending approval link in the QA stage:

<img src="images/Lab6_14.jpg" width="624"/>

Note that any one of the two approvers (a group and a person) can complete the approval. The options are to reject the release, approve it for immediate deployment or defer and pick a date and time for deployment. Optionally add a comment (e.g. "Approved for QA"  and click Approve to allow the creation of the QA environment:

<img src="images/Lab6_15.jpg" width="624"/>

The QA environment should then be succesfully created:

<img src="images/Lab6_16.jpg" width="624"/>

If you check in the Azure Portal you should now see the newly created Resource Group for the QA service plan and web application:

<img src="images/Lab6_17.jpg" width="624"/>

[<- Lab 5: Deploy changes via a Pull Request](https://github.com/gidavies/AzureDevOpsLab/blob/master/AzureDevOpsLab5.md) | [Lab 7: Create a release dashboard ->](https://github.com/gidavies/AzureDevOpsLab/blob/master/AzureDevOpsLab7.md)
