---
layout: post
toc: true
title: Tasks
icon: fas fa-circle-check
order: 2
---

## Summary Tasks

Summary tasks allow you to group your tasks. To create a summary task, you simply indent (by tapping **Indent selected tasks** button on the toolbar) the tasks under the designated summary task. By removing the indentation of all subtasks of a summary task (**Unindent selected tasks** button) you can change the summary task back to being a regular task.

As summary tasks group other tasks, they are not tasks on themselves, so their durations show the overall duration of the tasks within the group. The end date of a summary task is the latest end date among end dates of subtasks.

Similarly, a summary task shows the overall % complete of its subtasks, the total cost of its subtasks, the total work of its subtasks.

In the Gantt chart summary tasks are shown as black bars. In the list of tasks they can be **expanded** or **collapsed** to show or hide the list of their subtasks.

## Root Summary Task

In Ingantt, there's always a summary task for your entire project. This task is task number 0, above all of your tasks.

The root summary task might not be visible by default. To change this, check **Show root summary task** in **Options** dialog.

Just like any other summary task, the root summary task shows the overall data of its subtasks. As all tasks in your schedule are its subtasks, the root summary task shows the overall data of your entire project.

The name of the root summary task is the same as the name of the project.

## Duration

While planning your project you enter Durations as estimates, meaning that the duration is a reasonable guess of how much time a task will take for all resources involved.

Don't confuse **Duration** with **Work**. You can have, for example, 3 people working on your task, but if they complete it in 1 day, you set the Duration of the task to 1 day. If these 3 people are assigned to the task, Ingantt calculates Work property for you as 3 days.

Duration can be changed using **Duration** field in **Task Properties** dialog.

When you're not yet confident with your estimate for the Duration, you can mark the Duration as **Estimate** ("**?**") in **Task Properties** dialog, in which case the Duration is always displayed with a question mark "**?**". Checking or unchecking this flag does not affect scheduling.

If at least one subtask of a summary task has **Estimate** checked, the summary task's duration is also marked as **Estimate** and thus also shows "**?**".

Duration can be set in Hours, Days, Weeks or Months. By default, "1 Day" means 8 hours, "1 Week" means 5 days (40 hours) and "1 Month" means 20 days and these defaults can be changed on **Advanced** tab of **Project Properties** dialog.

When you change resource assignments, work or duration, one of these is recalculated according to task's [Type](#type-and-effort-driven).

## Work

Once a task has a work resource assigned (like a person who does the task), **Work** property of the task becomes different from 0\. It shows the time all resources would spend working on the task. For example, if there are 2 people working on a task of duration of 1 day, Work becomes equal to 2 days (16 hours according to default settings).

Work can be changed using **Work** field in **Task Properties** dialog.

Just like Duration, Work can be specified in Hours, Days, Weeks or Months using definitions of these on **Advanced** tab of **Project Properties** dialog. However, Work is always displayed in Hours.

When you change resource assignments, work or duration, one of these is recalculated according to task's [Type](#type-and-effort-driven).

## Deadline

Sometimes you need to keep in mind that a task should be completed by a particular day typically called a deadline.

Deadline of a task can be specified using **Deadline** field in **Task Properties** dialog.

Deadlines are for your own reference only, they do not affect scheduling.

Deadlines are shown in the Gantt chart as special icons.

> If your schedule shows that a task finishes later than its deadline specifies, Ingantt shows an icon in the list of tasks and counts such tasks in the navigation drawer.
{: .prompt-info }
> You can set a deadline for the entire project by setting the deadline to its root summary task. Just make sure the root summary task is set to visible in **Options** dialog.
{: .prompt-tip }

## Milestone

Any task can be marked as a milestone by checking **Milestone** checkbox in **Task Properties** dialog. This doesn't change its duration, doesn't affect scheduling, but the task is shown in the Gantt chart as an icon.

If you specify 0 as the **Duration** of a task, the task is marked as **Milestone** automatically once you save the change.

## Critical Tasks

Once your plan is put into action, reality happens. Some tasks finish earlier than planned, but some are not. And you might notice that some tasks are done a little longer, but this does not make the entire project longer. These tasks have some room to grow, some _slack_.

On the other hand, there are other tasks, and when they are done longer, the entire project's end date is shifted. They don't have room to grow at all, their slack is zero. Such tasks which cannot be delayed without delaying the entire project are called _critical tasks_. If you expect your project to finish in time it is important to pay special attention to critical tasks when tracking your project's progress.

Ingantt allows detecting critical tasks automatically. If in the **Options** dialog **Highlight critical tasks in the Gantt chart** is checked, such tasks are displayed in red.

## Fixed Cost

If there's a cost specifically associated with your particular task, you can set it in **Fixed Cost** property available in **Task Properties** dialog.

Task's total cost (shown in **Cost** column of the task list) is calculated as a total of Fixed Cost and costs of assigned resources based on their costs/rates.

For more information on costs, see [Planning costs](../planning-costs/).

## % Complete

Once your project is running, you need to track its progress. If you have % Complete set and up-to-date for each task, you can see the overall % Complete of the project in its root summary task.

Use **% Complete** field in **Task Properties** dialog to set % complete of a particular task.

> Updating this property updates visual representation of a task and summary tasks above it in the Gantt chart. It also updates **% Complete** column in the task list. But changing this property in Ingantt does not affect your schedule.
{: .prompt-info }

## Constraints

In combination with task dependencies (tasks linked to the task as predecessors), constraint of a task defines how the task is scheduled.

Constraints are set on **Advanced** tab of **Task Properties** dialog. The default constraint for a task is **As soon as possible** (in projects planned from Finish date the default constraint is **As late as possible**). This means that the task is set as close to the project's start date as possible with respect to dependencies with other tasks the task has.

There are 2 constraints which force the task to start or finish at the date specified regardless of dependencies. These constraints are called _inflexible constraints_ and are **Must start on** and **Must finish on**. It is recommended to set such constraints to your tasks only if you are absolutely confident that they are necessary for these tasks.

Other constraints (**Start/Finish no earlier/later than**) are called _flexible_, as they respect task dependencies and if such dependencies cause the task to start/finish at a different date then the task starts/finishes at the different date.

Constraint                 | Description
:------------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------
**As soon as possible**    | Task is scheduled as soon as the predecessors allow. So, if no predecessors are linked, the task starts at the beginning of the parent's summary task.
**As late as possible**    | Task is scheduled as late as the predecessors allow. So, if no predecessors are linked, the task finishes at the end of the parent's summary task.
**Start no earlier than**  | If the task starts later than the specified date due to predecessors, nothing changes. Otherwise, the task is scheduled to start on the specified date.
**Start no later than**    | If the task starts earlier than the specified date due to predecessors, nothing changes. Otherwise, the task is scheduled to start on the specified date.
**Finish no earlier than** | If the task finishes later than the specified date due to predecessors, nothing changes. Otherwise, the task is scheduled to finish on the specified date.
**Finish no later than**   | If the task finishes earlier than the specified date due to predecessors, nothing changes. Otherwise, the task is scheduled to finish on the specified date.
**Must start on**          | Task's start date is scheduled to be exactly as specified, regardless of predecessors.
**Must finish on**         | Task's finish date is scheduled to be exactly as specified, regardless of predecessors.

If a flexible or inflexible constraint is applied for a task, a special icon is shown for the task in the list of tasks.

> Use default constraints for most tasks, use flexible constraints for tasks where Start or Finish depends on a particular date.
{: .prompt-tip }

## Type and Effort Driven

Work resource assignments (or, rather units of assigned work resources), work and duration depend on each other. So once you change one of these, the rest should somehow change. Task's **Type** (with the help of **Effort Driven** flag) defines, which of the remaining 2 properties should stay unchanged, so that only one of them would be recalculated.

For example, you can set the **Type** to **Fixed units** (like it is by default), in which case when you change Duration Work is automatically recalculated.

Type               | Description
:----------------- | :---------------------------------------------------------
**Fixed units**    | When you change Duration: Work is recalculated.
                   | When you change Work: Duration is recalculated.
                   | When you change Units:
                   | - If **Effort Driven** is set: Duration is recalculated
                   | - If **Effort Driven** is not set: Work is recalculated
**Fixed duration** | When you change Duration: Work is recalculated.
                   | When you change Work: Units are recalculated.
                   | When you change Units:
                   | - If **Effort Driven** is set: Units are recalculated
                   | - If **Effort Driven** is not set: Work is recalculated
**Fixed work**     | When you change Duration: Units are recalculated.
                   | When you change Work: Duration is recalculated.
                   | When you change Units: Duration is recalculated

In other words, thanks to **Type** you can freeze one of the 3 properties, while **Effort Driven** defines whether Work should stay unchanged among the remaining two.

## Notes

You can add any texts to your task by filling in **Notes** field in **Task Properties** dialog. Use it for task description, contact information, ideas or any other text data.

If a task has **Notes** field filled in, a special icon is shown for the task in the list of tasks. In Windows and Web versions of Ingantt hovering the mouse over the icon shows the note.

## Resource Assignments and Units

Resources can be assigned to a task on **Resources** tab of **Task Properties** dialog.

To assign a resource, simply check the checkbox in the row with the resource. To unassign a resource, uncheck the checkbox.

Resource assignments of work or material resource types have **Units** as shown in the corresponding column. By clicking **Edit** button you can change the value of **Units** set by default when assigning.

By default, work resources are assigned with 100% units. This means that they will do the particular task fully dedicating their time available in their calendar. You can change the default value to a lower number.

By default, material resources are assigned with 1 unit. This means that 1 unit (box, gallon, ton etc. depending on how you define it for the material) of that material will be spent when implementing the task. You can change the default value and set any number of units.

## Predecessors and Dependencies

When you link tasks using **Link selected tasks** toolbar button, you create a dependency between the tasks. The dependency is called **Finish to Start**, and it is one of 4 dependencies available:

Type                 | Description
:------------------- | :-------------------------------------------------------------------
**Finish to Start**  | the second task starts at the same time as the first task finishes
**Finish to Finish** | the second task finishes at the same time as the first task finishes
**Start to Finish**  | the second task finishes at the same time as the first task starts
**Start to Start**   | the second task starts at the same time as the first task starts

To assign predecessors and edit dependencies, use **Predecessors** tab in **Task Properties** dialog.

## Lag and Lead time

Sometimes you might need to set some waiting time between 2 dependent tasks.

Let's say that your first task is "Paint the wall" and your second task is "Hang pictures on the wall", these tasks are linked (have **Finish to Start** dependency). It's not possible to hang pictures until the paint is dry, so you need to wait. To reflect this in your schedule, set the **Lag** (for example, 1 day) for the dependency between the two tasks.

Lags can also be used in a situation directly opposite to waiting, when the depending task should start a bit earlier. To set this, make the **Lag** negative (for example, -1 day). This is called _lead time_.

To set lag or lead time, use **Edit** button in **Predecessors** tab in **Task Properties** dialog to set such time between the task that is being edited and its predecessor in the list.

> Note that lags can be set in hours, days, weeks, months or as a fraction of the predecessor task's duration (for example, 50%).
{: .prompt-info }

## Circular dependencies

If you accidentally create two dependencies between two tasks, making each task a predecessor of the second one, Ingantt detects such situations and reverts the last action. There can be other, more complex situations when such circular dependencies occur, but in all cases they are immediately detected and the last action causing them is reverted.
