---
layout: post
toc: true
title: Tasks
icon: fas fa-circle-check
order: 2
---

## Summary Tasks

Summary tasks help you organize your tasks by grouping them together. To create a summary task, simply select and indent the tasks you want to include under it by clicking the **Increase Indent** button on the toolbar. If you want to change a summary task back to a regular task, remove the indentation of all its subtasks by selecting them and clicking the **Decrease Indent** button.

Since summary tasks group other tasks, they are not exactly tasks themselves. Instead, their duration represents the overall duration of all the tasks within the group: the end date of a summary task is the latest end date among its subtasks.

A summary task also displays the overall percentage of completion, total cost, and total work of its subtasks.

In the Gantt chart, summary tasks are shown as black bars. In the task list, you can **expand** or **collapse** summary tasks to show or hide their subtasks.

![light mode only](/tabs/images/tasks/summary.png){: .light  .shadow .rounded-10 w='611' h='117' }
![dark mode only](/tabs/images/tasks/summary_d.png){: .dark .shadow .rounded-10 w='611' h='117' }

## Root Summary Task

In Ingantt, there's always a summary task for your entire project. This task is task number 0, above all of your tasks.

The root summary task might not be visible by default. To change this, check **Show root summary task** in the **Options** dialog.

Just like any other summary task, the root summary task shows the overall data of its subtasks. Since all tasks in your schedule are its subtasks, the root summary task shows the overall data of your entire project.

The name of the root summary task is the same as the name of the project.

## Duration

While planning your project, you enter Durations as estimates, meaning the duration is a reasonable guess of how much time a task will take for all resources involved.

Don't confuse **Duration** with **Work**. For example, if three people are working on your task, but they complete it in one hour, you set the **Duration** of the task to one hour. If these three people are assigned to the task, Ingantt calculates the **Work** property for you as three hours.

Duration can be changed using the **Duration** field in the **Task Properties** dialog.

When you're not yet confident with your estimate for the Duration, you can mark the Duration as an **Estimate** ("**?**") in the **Task Properties** dialog, which causes the Duration to always display a question mark ("**?**"). Checking or unchecking this flag does not affect scheduling.

If at least one subtask of a summary task has **Estimate** checked, the summary task's duration is also marked as **Estimate** and thus also shows "**?**".

Duration can be set in Hours, Days, Weeks, or Months. By default, "1 Day" means 8 hours, "1 Week" means 5 days (40 hours), and "1 Month" means 20 days. These defaults can be [changed]({% link _tabs/project.md %}#hours-per-day-days-per-week-days-per-month) on the **Advanced** tab of the **Project Properties** dialog.

When you change resource assignments, work, or duration, one of these is recalculated according to the task's [Type](#type-and-effort-driven).

## Work

Once a task has a work resource assigned (such as a person performing the task), the **Work** property of the task becomes greater than 0. It shows the time all resources will spend working on the task. For example, if a task with a **Duration** of 5 hours has 2 assigned resources working on it, the task's **Work** is equal to 10 hours.

Work can be changed using the **Work** field in the **Task Properties** dialog.

Just like Duration, Work can be specified in Hours, Days, Weeks, or Months using definitions on the **Advanced** tab of the **Project Properties** dialog. However, Work is always displayed in Hours.

When you change resource assignments, work, or duration, one of these is recalculated according to the task's [Type](#type-and-effort-driven).

## Deadline

Sometimes you need to ensure a task is completed by a specific day, typically called a deadline.

The deadline of a task can be specified using the **Deadline** field in the **Task Properties** dialog.

Deadlines are for your reference only and do not affect scheduling.

Deadlines are shown in the Gantt chart as special icons.

> If your schedule shows that a task finishes later than its specified deadline, Ingantt shows an icon in the list of tasks and counts such tasks in the navigation drawer.
{: .prompt-info }
> You can set a deadline for the entire project by setting the deadline for the root summary task. Just make sure the root summary task is set to visible in the **Options** dialog.
{: .prompt-tip }

![light mode only](/tabs/images/tasks/deadline.png){: .light  .shadow .rounded-10 w='604' h='77' }
![dark mode only](/tabs/images/tasks/deadline_d.png){: .dark .shadow .rounded-10 w='604' h='77' }

## Milestone

Any task can be marked as a milestone by checking the **Milestone** checkbox in the **Task Properties** dialog. This doesn't change its duration or affect scheduling, but the task is shown in the Gantt chart as an icon.

![light mode only](/tabs/images/tasks/milestone.png){: .light  .shadow .rounded-10 w='577' h='81' }
![dark mode only](/tabs/images/tasks/milestone_d.png){: .dark .shadow .rounded-10 w='577' h='81' }

If you specify 0 as the **Duration** of a task, the task is automatically marked as a **Milestone** once you save the change.

## Critical Tasks

Once your plan is put into action, reality happens. Some tasks finish earlier than planned, while others do not. You might notice that some tasks take a bit longer, but this doesn't extend the entire project timeline. These tasks have some room to grow, known as _slack_.

Conversely, there are tasks that, when delayed, shift the entire project's end date. These tasks have no room to grow, meaning their slack is zero. Such tasks, which cannot be delayed without impacting the entire project, are called _critical tasks_. To ensure your project finishes on time, it is crucial to pay special attention to critical tasks when tracking your project's progress.

Ingantt automatically detects critical tasks. If the **Highlight critical tasks in the Gantt chart** option is checked in the **Options** dialog, these tasks are displayed in red.

![light mode only](/tabs/images/tasks/critical.png){: .light  .shadow .rounded-10 w='595' h='160' }
![dark mode only](/tabs/images/tasks/critical_d.png){: .dark .shadow .rounded-10 w='595' h='160' }

## Fixed Cost

If there's a cost specifically associated with your task, you can set it in the **Fixed Cost** property available in the **Task Properties** dialog.

The task's total cost (shown in the **Cost** column of the task list) is calculated as the total of the Fixed Cost and the costs of assigned resources based on their costs/rates.

For more information on costs, see [Planning costs]({% link _tabs/planning-costs.md %}).

## % Complete

Once your project is running, you need to track its progress. If you have **% Complete** set and up-to-date for each task, you can see the overall **% Complete** of the project in its root summary task.

Use the **% Complete** field in the **Task Properties** dialog to set the % complete of a particular task.

> Updating this property updates the visual representation of a task and summary tasks above it in the Gantt chart. It also updates the **% Complete** column in the task list. However, changing this property in Ingantt does not affect your schedule.
{: .prompt-info }

![light mode only](/tabs/images/tasks/complete.png){: .light  .shadow .rounded-10 w='494' h='208' }
![dark mode only](/tabs/images/tasks/complete_d.png){: .dark .shadow .rounded-10 w='494' h='208' }

## Constraints

In combination with task dependencies (tasks linked to the task as predecessors), a task's constraint defines how the task is scheduled.

Constraints are set on the **Advanced** tab of the **Task Properties** dialog. The default constraint for a task is **As soon as possible** (in projects planned from the Finish date, the default constraint is **As late as possible**). This means that the task is set as close to the project's start date as possible with respect to dependencies with other tasks.

There are two constraints that force the task to start or finish at the specified date regardless of dependencies. These constraints are called _inflexible constraints_ and are **Must start on** and **Must finish on**. It is recommended to set such constraints only if you are absolutely confident they are necessary.

Other constraints (**Start/Finish no earlier/later than**) are called _flexible_, as they respect task dependencies. If such dependencies cause the task to start/finish at a different date, then the task starts/finishes at the different date.

| Constraint                 | Description                                                                                                                                   |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| **As soon as possible**    | The task is scheduled as soon as the predecessors allow. If no predecessors are linked, the task starts at the beginning of the parent's summary task. |
| **As late as possible**    | The task is scheduled as late as the predecessors allow. If no predecessors are linked, the task finishes at the end of the parent's summary task.    |
| **Start no earlier than**  | If the task starts later than the specified date due to predecessors, nothing changes. Otherwise, the task is scheduled to start on the specified date. |
| **Start no later than**    | If the task starts earlier than the specified date due to predecessors, nothing changes. Otherwise, the task is scheduled to start on the specified date.|
| **Finish no earlier than** | If the task finishes later than the specified date due to predecessors, nothing changes. Otherwise, the task is scheduled to finish on the specified date.|
| **Finish no later than**   | If the task finishes earlier than the specified date due to predecessors, nothing changes. Otherwise, the task is scheduled to finish on the specified date.|
| **Must start on**          | The task's start date is scheduled to be exactly as specified, regardless of predecessors.                                                   |
| **Must finish on**         | The task's finish date is scheduled to be exactly as specified, regardless of predecessors.                                                  |

If a flexible or inflexible constraint is applied to a task, a special icon is shown for the task in the list of tasks.

> Use default constraints for most tasks and use flexible constraints for tasks where Start or Finish depends on a particular date.
{: .prompt-tip }

## Type and Effort Driven

Work resource assignments (or units of assigned work resources), work, and duration depend on each other. So once you change one of these, the rest should somehow change. The task's **Type** (with the help of the **Effort Driven** flag) defines which of the remaining two properties should stay unchanged, so that only one of them is recalculated.

For example, you can set the **Type** to **Fixed units** (the default), in which case when you change Duration, Work is automatically recalculated.

| Type               | Description                                             |
|--------------------|---------------------------------------------------------|
| **Fixed units**    | When you change Duration: Work is recalculated.         |
|                    | When you change Work: Duration is recalculated.         |
|                    | When you change Units:                                  |
|                    | - If **Effort Driven** is set: Duration is recalculated |
|                    | - If **Effort Driven** is not set: Work is recalculated |
| **Fixed duration** | When you change Duration: Work is recalculated.         |
|                    | When you change Work: Units are recalculated.           |
|                    | When you change Units:                                  |
|                    | - If **Effort Driven** is set: Units are recalculated   |
|                    | - If **Effort Driven** is not set: Work is recalculated |
| **Fixed work**     | When you change Duration: Units are recalculated.       |
|                    | When you change Work: Duration is recalculated.         |
|                    | When you change Units: Duration is recalculated         |

In other words, the **Type** allows you to freeze one of the three properties, while the **Effort Driven** flag defines whether Work should stay unchanged among the remaining two.

## Notes

You can add any text to your task by filling in the **Notes** field in the **Task Properties** dialog. Use it for task descriptions, contact information, ideas, or any other text data.

If a task has the **Notes** field filled in, a special icon is shown for the task in the list of tasks. On Windows, macOS, and Web versions, hovering the mouse over the icon shows the note.

## Resource Assignments and Units

Resources can be assigned to a task on the **Resources** tab of the **Task Properties** dialog.

To assign a resource, simply check the checkbox in the row with the resource. To unassign a resource, uncheck the checkbox.

Resource assignments of work or material resource types have **Units** as shown in the corresponding column. By clicking the **Edit** button, you can change the value of **Units** set by default when assigning.

By default, work resources are assigned with 100% units. This means they will fully dedicate their available time in their calendar to the particular task. You can change the default value to any number.

By default, material resources are assigned with 1 unit. This means 1 unit (box, gallon, ton, etc., depending on how you define it for the material) of that material will be used when completing the task. You can change the default value and set any number of units.

## Predecessors and Dependencies

When you link tasks using the **Link selected tasks** toolbar button, you create a dependency between the tasks. The dependency is called **Finish to Start**, and it is one of four dependencies available:

| Type                | Description                                                                   |
|---------------------|-------------------------------------------------------------------------------|
| **Finish to Start** | The second task starts at the same time as the first task finishes.           |
| **Finish to Finish**| The second task finishes at the same time as the first task finishes.         |
| **Start to Finish** | The second task finishes at the same time as the first task starts.           |
| **Start to Start**  | The second task starts at the same time as the first task starts.             |

![light mode only](/tabs/images/tasks/dependencies.png){: .light  .shadow .rounded-10 w='499' h='326' }
![dark mode only](/tabs/images/tasks/dependencies_d.png){: .dark .shadow .rounded-10 w='499' h='326' }

To assign predecessors and edit dependencies, use the **Predecessors** tab in the **Task Properties** dialog.

## Lag and Lead Time

Sometimes you might need to set some waiting time between two dependent tasks.

Let's say your first task is "Paint the wall" and your second task is "Hang pictures on the wall." These tasks are linked (have a **Finish to Start** dependency). It's not possible to hang pictures until the paint is dry, so you need to wait. To reflect this in your schedule, set the **Lag** (for example, 2 days) for the dependency between the two tasks.

![light mode only](/tabs/images/tasks/lag.png){: .light  .shadow .rounded-10 w='569' h='129' }
![dark mode only](/tabs/images/tasks/lag_d.png){: .dark .shadow .rounded-10 w='569' h='129' }

Lags can also be used in a situation directly opposite to waiting, when the dependent task should start a bit earlier. To set this, make the **Lag** negative (for example, -1 day). This is called _lead time_.

To set lag or lead time, use the **Edit** button in the **Predecessors** tab in the **Task Properties** dialog to set such time between the task being edited and its predecessor in the list.

> Note that lags can be set in hours, days, weeks, months, or as a fraction of the predecessor task's duration (for example, 50%).
{: .prompt-info }

## Circular Dependencies

If you accidentally create two dependencies between two tasks, making each task a predecessor of the other, Ingantt detects this and reverts the last action. In more complex situations where circular dependencies occur, they are detected, and the last action causing them is reverted.
