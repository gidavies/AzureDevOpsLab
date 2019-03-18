# Lab 4: Agile planning with Azure Boards

In this lab we will use Azure Boards to plan and track work in the project.

# Step 1: Add some items to the Product Backlog

Navigate to the product backlog by selecting Boards | Backlogs:

<img src="images/Lab4_1a.jpg" width="624"/>

You will see that the backlog is empty and that no work has been assigned to any Iterations/Sprints. Add an item to the backlog by selecting + New Work Item:

<img src="images/Lab4_2a.jpg" width="624"/>

Give the work item (a user story by default if using the Agile template) a title e.g. "Update the about page in the web application" and click the Add to bottom button:

<img src="images/Lab4_3a.jpg" width="624"/>

Repeat and add at least one more work item. Then drag and drop the items up and down the backlog to raise or lower their relative priority:

<img src="images/Lab4_4a.jpg" width="624"/>

Many teams prefer to visualise their product backlogs, and progress, in a board rather than a list view. Select View as board:

<img src="images/Lab4_5a.jpg" width="624"/>

And you will now see the same work items in a board view:

<img src="images/Lab4_6a.jpg" width="624"/>

Try adding more work items in the board, and reordering the work items in the New column:

<img src="images/Lab4_7a.jpg" width="624"/>

You can add more columns, rename existing columns, add swimlanes, choose which fields to show, apply colour stylings and more in the settings. Explore the settings as you wish and play around with the board:

<img src="images/Lab4_8.jpg" width="624"/>

As an example we've added a swimlane called Expedite (to show work that needs to be given priority) and added a style that changes the card colour if the priority field is equal to 1:

<img src="images/Lab4_8b.jpg" width="624"/>

# Step 2: Add a new item and create a branch to work on it

In the Board create a new item called "Update home page heading":

<img src="images/Lab4_9a.jpg" width="624"/>

Move (drag and drop) it to the first column (Active if using the default Agile process) to indicate that you are going to start work on it:

<img src="images/Lab4_10a.jpg" width="624"/>

Click on the card's three dots and select New branch:

<img src="images/Lab4_11.jpg" width="624"/>

Give the branch a name (no spaces) and notice that the branch is linked to the work item (or you could link to others if you want) and will be branching from the master branch. Click Create branch:

<img src="images/Lab4_12.jpg" width="624"/>

You will be redirected to the Azure Repos file area and you will see that the new branch you have just created is now available alongside the master branch.

<img src="images/Lab4_13.jpg" width="624"/>

You have now added work to a board, and are ready to make code changes in an independent branch without directly impacting the master branch. In the next lab we will change the branch and merge in back into the master branch via a Pull Request.

[<- Lab 3: Exploring the created Azure DevOps release pipeline](https://github.com/gidavies/AzureDevOpsLab/blob/master/AzureDevOpsLab3.md) | [Lab 5: Deploy via a Pull Request ->](https://github.com/gidavies/AzureDevOpsLab/blob/master/AzureDevOpsLab5.md)
