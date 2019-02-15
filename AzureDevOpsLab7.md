# Lab 7: Create a release dashboard

In this lab we will create an Azure Boards dashboard to show build and release status.

# Adding widgets to a dashboard

Navigate to the dashboards (Overview | Dashboards) and click on Add a widget:

<img src="images/Lab7_1.jpg" width="624"/>

Type in "build" and select the Build History widget, and then click Add:

<img src="images/Lab7_2.jpg" width="312"/>

In the newly added widget select the settings cog:

<img src="images/Lab7_3.jpg" width="624"/>

Set the build pipeline to the one used in this project and click Save:

<img src="images/Lab7_4.jpg" width="312"/>

Add another widget by typing in "release" and then select and add the Deployment Status widget:

<img src="images/Lab7_5.jpg" width="312"/>

Configure the Deployment Status widget to select the Build pipeline and then select all stages (dev and QA) for the release pipeline, then click Save (you may need to change the widget size to 3x2 if there isn't room in the default size):

<img src="images/Lab7_6.jpg" width="312"/>

Click Done Editing and the dashboard is ready:

<img src="images/Lab7_7.jpg" width="624"/>

<img src="images/Lab7_8.jpg" width="624"/>

If you select the settings for the dashboard (cog in top right hand corner) you can see options to rename the dashboard, auto-refresh the widgets and set security permissions, if desired:

<img src="images/Lab7_9.jpg" width="624"/>

You now have a dashboard showing the current status of build and release pipelines.

[<- Lab 6: Extend the release pipeline](https://github.com/gidavies/AzureDevOpsLab/blob/master/AzureDevOpsLab5.md)
