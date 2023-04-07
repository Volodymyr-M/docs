---
# the default layout is 'page'
layout: post
toc: true
title: Getting Started
icon: fas fa-bars-progress
order: 1
---

Ingantt is a project management multi-platform app allowing to create project plans, schedules, timelines, roadmaps.

### What you can do with Ingantt
- plan and estimate your project by splitting the project into a number of tasks and setting dependencies between them
- review you plan using Gantt chart
- manage project resources (work, material or cost) and assign them to tasks
- manage project calendars (set working times, add holidays etc)
- manage resource calendars (working times, vacations etc)
- plan and estimate costs
- control your project's progress by setting % complete values
- review critical tasks
- be notified if a resource is overallocated
- auto-level overallocated resources
- mark tasks as milestones
- set task deadlines and be notified if the task is scheduled to finish later
					
### Compatibility

Ingantt is a user-friendly alternative to Microsoft Project, if you're familiar with Microsoft Project, you can quickly get started with Ingantt.
Ingantt can open files saved by Microsoft Project in XML format. Files saved by	Ingantt also use the same XML format, so they can be opened by Microsoft Project or software compatible with it.

### Cloud support

Ingantt can can create, open and save local files on your device. If you choose, you can sign in to your Google account to be able to open and save files on your Google Drive.

### Platform support

Ingantt is available on Windows, Android and the Web.

## Installation
Ingantt is multi-platform, so install the version that is right for you device.
						
- **Web:** Just open this <a href="https://ingantt.com/web/">link</a>
- **Windows:** <!--Get it at <a href="#">Microsoft Store</a> -->	Coming soon
- **Android:**				<!-- Get it at <a href="#">Google Store</a>-->Coming soon

> Ingantt is currently in **Open Beta** status. This means that you can	get the app for free, yet some bugs are possible. We would like to hear your feedback! Please contact us <script language="javascript" type="text/javascript">var a = "support"; document.write("<a href='mailto:" + a + "@ingantt.com'>" + a + "@ingantt.com</a>");</script>
{: .prompt-info }
						
						

## Logging in (optional)
Once installed, you can start working with Ingantt right away by creating, opening and saving local files on your device. 
If you would like to have your files in the cloud, you can **Sign in to	Google**. This gives you the ability to save and open your schedules from your **Google Drive** storage.

> When signin in, Ingantt requires permission to only be able to edit the files that it creates. No other files are read or written, and the permission for them is not	requested.
{: .prompt-info }
						
## Creating basic schedule
Let's say you have a small home renovation project of 2 tasks, one is done after another.

Once you click on **Create new** project button, you're brought to a split	screen containing your future list of tasks on the left and your Gantt chart on the right.
Add your tasks one after another by clicking on the big **+** button in the bottom right and specifying **Name** and predicted **Duration** of each of them in **Add Task** dialog.
Select both of your tasks in the list on the left and then click **Link selected tasks** toolbar button. This makes the tasks connected and the Gantt chart is updated.

- To select multiple tasks on Android hold your finger a little longer while tapping each task either in the list or in the Gantt chart.
- On other systems click on tasks in the list or in the Gantt chart while holding _Ctrl_ or _Shift_.
							
Now that the tasks are linked if you decide to update the duration of the first task (by double clicking it in the list or the Gantt chart and editing **Duration**	field in **Task Properties** dialog), you can see how this change affects the schedule shifting the second task.
						
				


## Setting project's Name and Start Date
Your project might start on a different day than the default used by Ingantt.

Click on **Show menu** toolbar icon, and then on **Project Properties**. Set the new project start date in **Project Start Date** field. And change the **Name** of the project while you're there.

> With all the simplicity of the basic schedule, by looking at the Gantt chart you can already tell when the project is expected to end.
{: .prompt-tip }

## Adding and assigning resources
Let's say that 2 different people will do each of the tasks in your project.

Click on the navigation menu button and switch to **Resources** view. Click on the big **+** button and add a work resource to your project using **Add	Resource** dialog by giving the resource some **Name**. Then repeat	the steps to add another work resource.

Using the navigation menu switch back to **Tasks** view, double click your first task in the list or in the Gantt chart to open **Task Properties** dialog.
						
Switch to	**Resources** tab, check your first resource to assign this person to the task	and save your changes.
						
Repeat the same steps for your second task and the second resource.

## Setting vacations
People can have different events during the course of your project, affecting its timeline.

Let's say that the resource doing the first task in your project needs to have 1 day off during it.

To configure this, use the navigation menu to go to **Resources** view.

Double click on the resource so see **Resource Properties**. Go to **Calendar** tab and click **Add exception** button. Choose one of	the days during the course of your project, leave the list of working times empty and save.
					
Using the navigation menu go back to **Tasks** and see how your schedule has changed and the task following the resource's task has also shifted due to its dependency on	it.

> Similarly you can configure not only vacations, but also other changes to a person's schedule. For example, by adding working time to the Exception you can tell Ingantt that on that particular day the resource works only during specified	hours.
{: .prompt-info }

						
## Setting holidays

Let's say that there's a holiday during the course of your project, a day during which no	work is done.

While vacations are configured through each resource's calendar, days affecting everyone are configured in project's calendar. The default project's calendar is called	**Standard** and it already contains information that no work is done on	weekends.
						
To configure holidays, use navigation menu to go to **Calendars** view. Double click on **Standard** so see **Calendar Properties**. Click **Add exception** button. Choose one of the days during the course of your project, leave the list of working times empty and save.

Using the navigation menu go back to **Tasks** view and see how your project has changed and the tasks are shifted. In the Gantt chart your holiday is shown similarly to	weekends.

> Using the same approach you can configure not only holidays, but also other changes to everyone's	schedule. For example, by adding working time to the Exception you can tell	Ingantt that on that particular day everyone works only during specified hours. You can also take a look at tabs representing each weekday in **Calendar Properties**. If your whole team, for example, leaves earlier on Fridays	or works on Saturdays, you can configure this on the corresponding tabs.
{: .prompt-info }

					
## Saving your schedule
Any time you can save your schedule by clicking on **Save** button in the main toolbar.

Depending on your choice, your schedule can either be saved as a local file on your device or	in Google Drive.

If your project is saved at least once and **Enable autosave** is checked	in **Options** dialog, Ingantt saves every change you make to the file automatically to the destination of your initial choice: local or Google Drive.

> Web version does not autosave to local files due to specifics of the platform.

Your project is always saved in a format that is fully compatible with Microsoft Project.
