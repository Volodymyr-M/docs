---
layout: post
toc: true
title: Getting Started
icon: fas fa-bars-progress
order: 1
---

## Installation

Ingantt is multi-platform, so install the version that is right for you device.

- **Windows:** [Get it from Microsoft Store](ms-windows-store://pdp/?productid=9NHQ26QV09F6)
- **Android:** [Get it on Google Play](https://play.google.com/store/apps/details?id=com.ingantt_development.ingantt){:target="_blank"}
- **macOS:** [Download on the Mac App Store](https://apps.apple.com/us/app/ingantt/id6450835363){:target="_blank"}
- **iOS:** [Download on the App Store](https://apps.apple.com/us/app/ingantt-project-scheduling/id6466750274){:target="_blank"}
- **Web:** [Open this link](https://web.ingantt.com){:target="_blank"}

{% include contact.html %}

## Logging in (optional)

Once installed, you can start working with Ingantt right away by creating, opening and saving local files on your device. If you would like to have your files in the cloud, on non-Apple platforms you can **Sign in to Google**. This gives you the ability to save and open your schedules from your **Google Drive** storage.

> When signing in, Ingantt requires permission to only be able to edit the files that it creates. No other files are read or written, and the permission for them is not requested.
{: .prompt-info }

## Creating basic schedule

Let's say you have a small home renovation project of 2 tasks, one is done after another.

Once you click on **Create new** project button, you're brought to a split screen containing your future list of tasks on the left and your Gantt chart on the right. Add your tasks one after another by clicking on the big **+** button in the bottom right and specifying **Name** and predicted **Duration** of each of them in **Add Task** dialog.

![light mode only](/tabs/images/add_task.png){: .light  .shadow .rounded-10 w='694' h='599' }
![dark mode only](/tabs/images/add_task_d.png){: .dark .shadow .rounded-10 w='694' h='599' }

Select both of your tasks in the list on the left and then click **Link selected tasks** toolbar button. This makes the tasks connected and the Gantt chart is updated.

- To select multiple tasks on Android and iOS, hold your finger a little longer while tapping each task either in the list or in the Gantt chart.
- On other platforms click on tasks in the list or in the Gantt chart while holding _Ctrl_ or _Shift_.

![light mode only](/tabs/images/link.png){: .light  .shadow .rounded-10 w='694' h='197' }
![dark mode only](/tabs/images/link_d.png){: .dark .shadow .rounded-10 w='694' h='197' }

Now that the tasks are linked if you decide to update the duration of the first task (by double-clicking it in the list or the Gantt chart and editing **Duration** field in **Task Properties** dialog), you can see how this change affects the schedule shifting the second task.

![light mode only](/tabs/images/gantt.png){: .light  .shadow .rounded-10 w='682' h='197' }
![dark mode only](/tabs/images/gantt_d.png){: .dark .shadow .rounded-10 w='682' h='197' }

## Setting project's Name and Start Date

Your project might start on a different day than the default used by Ingantt.

Click on **Show menu** toolbar icon, and then on **Project Properties**.

Set the new project start date in **Project Start Date** field. And change the **Name** of the project while you're there.

![light mode only](/tabs/images/project_name.png){: .light .shadow .rounded-10 w='550' h='365' }
![dark mode only](/tabs/images/project_name_d.png){: .dark .shadow .rounded-10 w='550' h='365' }

> With all the simplicity of the basic schedule, by looking at the Gantt chart you can already tell when the project is expected to end.
{: .prompt-tip }

## Adding and assigning resources

Let's say that 2 different people will do each of the tasks in your project.

Click on the navigation menu button and switch to **Resources** view.

![light mode only](/tabs/images/nav.png){: .light .shadow .rounded-10 w='294' h='483' }
![dark mode only](/tabs/images/nav_d.png){: .dark .shadow .rounded-10 w='294' h='483' }

Click on the big **+** button and add a work resource to your project using **Add Resource** dialog by giving the resource some **Name**. Then repeat the steps to add another work resource.

![light mode only](/tabs/images/add_resource.png){: .light .shadow .rounded-10 w='364' h='287' }
![dark mode only](/tabs/images/add_resource_d.png){: .dark .shadow .rounded-10 w='364' h='287' }

![light mode only](/tabs/images/resources.png){: .light .shadow .rounded-10 w='682' h='197' }
![dark mode only](/tabs/images/resources_d.png){: .dark .shadow .rounded-10 w='682' h='197' }

Using the navigation menu switch back to **Tasks** view, double-click your first task in the list or in the Gantt chart to open **Task Properties** dialog.

Switch to **Resources** tab, check your first resource to assign this person to the task and save your changes.

![light mode only](/tabs/images/assignments.png){: .light .shadow .rounded-10 w='550' h='241' }
![dark mode only](/tabs/images/assignments_d.png){: .dark .shadow .rounded-10 w='550' h='241' }

Repeat the same steps for your second task and the second resource.

![light mode only](/tabs/images/resources_gantt.png){: .light  .shadow .rounded-10 w='682' h='197' }
![dark mode only](/tabs/images/resources_gantt_d.png){: .dark .shadow .rounded-10 w='682' h='197' }

## Setting vacations

People can have different events during the course of your project, affecting its timeline.

Let's say that the resource doing the first task in your project needs to have 1 day off during it.

To configure this, use the navigation menu to go to **Resources** view.

Double-click on the resource so see **Resource Properties**. Go to **Calendar** tab and click **Add exception** button. Choose one of the days during the course of your project, leave the list of working times empty and save.

![light mode only](/tabs/images/day_off.png){: .light .shadow .rounded-10 w='551' h='302' }
![dark mode only](/tabs/images/day_off_d.png){: .dark .shadow .rounded-10 w='551' h='302' }

Using the navigation menu go back to **Tasks** and see how your schedule has changed and the task following the resource's task has also shifted due to its dependency on it.

![light mode only](/tabs/images/vacation.png){: .light .shadow .rounded-10 w='682' h='197' }
![dark mode only](/tabs/images/vacation_d.png){: .dark .shadow .rounded-10 w='682' h='197' }

> Similarly, you can configure not only vacations, but also other changes to a person's schedule. For example, by adding working time to the Exception you can tell Ingantt that on that particular day the resource works only during specific hours.
{: .prompt-info }

## Setting holidays

Let's say that there's a holiday during the course of your project, a day during which no work is done.

While vacations are configured through each resource's calendar, days affecting everyone are configured in the project's calendar. The default project's calendar is called **Standard**, and it already contains information that no work is done on weekends.

To configure holidays, use navigation menu to go to **Calendars** view. Double-click on **Standard** so see **Calendar Properties**. Click **Add exception** button. Choose one of the days during the course of your project, leave the list of working times empty and save.

![light mode only](/tabs/images/holiday.png){: .light .shadow .rounded-10 w='550' h='302' }
![dark mode only](/tabs/images/holiday_d.png){: .dark .shadow .rounded-10 w='550' h='302' }

Using the navigation menu go back to **Tasks** view and see how your project has changed and the tasks are shifted. In the Gantt chart your holiday is shown similarly to weekends.

![light mode only](/tabs/images/final.png){: .light .shadow .rounded-10 w='682' h='197' }
![dark mode only](/tabs/images/final_d.png){: .dark .shadow .rounded-10 w='582' h='197' }

> Using the same approach you can configure not only holidays, but also other changes to everyone's schedule. For example, by adding working time to the Exception you can tell Ingantt that on that particular day everyone works only during specific hours. You can also take a look at tabs representing each weekday in **Calendar Properties**. If your whole team, for example, leaves earlier on Fridays or works on Saturdays, you can configure this on the corresponding tabs.
{: .prompt-info }

## Saving your schedule

Any time you can save your schedule by clicking on **Save** button in the main toolbar.

Depending on your choice, your schedule can either be saved as a local file on your device or in Google Drive.

If your project is saved at least once and **Enable autosave** is checked in **Options** dialog, Ingantt saves every change you make to the file automatically to the destination of your initial choice: local or Google Drive.

> Web version does not autosave to local files due to specifics of the platform.

Your project is always saved in a format that is fully compatible with Microsoft Project.
