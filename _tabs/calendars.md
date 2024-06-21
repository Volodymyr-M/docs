---
layout: post
toc: true
title: Calendars
icon: fas fa-calendar
order: 4
---

Calendars define days and times when work can be done. This is determined through two types of calendar data:

- **Weekdays**: Work time is set for each day of the week: Sunday, Monday, Tuesday, etc. This defines the typical, routine calendar for work.
- **Exceptions**: If work is not done or is done at different times on a particular date, this is defined as a calendar exception.

## Project Calendar

A project has a **Calendar** associated with it as specified in the **Project Properties** dialog. This calendar defines how tasks not assigned to work resources or their own calendars are scheduled. Also, days off like weekends are shown in the Gantt chart according to this calendar.

## Resource Calendar

Each [work resource]({% link _tabs/resources.md %}#resource-type) has a calendar associated with it as specified in the **Base Calendar** field of the **Resource Properties** dialog. Once the work resource is [assigned]({% link _tabs/tasks.md %}#resource-assignments-and-units) to a task, its calendar affects the scheduling of the task.

> If you have multiple resources working according to a similar work schedule, you can create a Calendar and assign it to them. At the same time, you can specify exceptions for each of them separately in **Resource Properties** if they have personal events like vacations or shorter/longer work periods on some dates.
{: .prompt-tip }

## Task Calendar

A task has a **Calendar** property in the **Task Properties** dialog. It is set to **NONE** by default. In this case:

- If a task is not assigned to any work resources, the task is scheduled according to the project's calendar.
- If a task is assigned to work resources, the task is scheduled according to their calendars.

If the task's **Calendar** property is set to a calendar instead of **NONE**:

- If a task is not assigned to any work resources, the task is scheduled according to the specified calendar.
- If a task is assigned to work resources, the task is scheduled according to the intersection of the specified calendar with the calendars of the assigned work resources. You can also check the **Ignore resource calendars** flag to schedule the task only according to the specified calendar.

## Predefined Calendars

Ingantt has 3 predefined calendars, one of which (**Standard**) is assigned to the project by default.

| Default Calendar | Description                                                                                     |
|------------------|-------------------------------------------------------------------------------------------------|
| **Standard**     | Work is done each day Monday to Friday, 8 AM to 5 PM with a 1-hour (12 PM to 1 PM) break.       |
| **Night Shift**  | Work is done Monday night through Saturday morning, 11 PM to 8 AM with an hour off (3 AM to 4 AM) break. |
| **24-hours**     | Work is done 24 hours a day, every day.                                                         |

As mentioned above, the **Standard** calendar defines that work is done Monday-Friday, 8 AM - 5 PM with a 1-hour break. This means that when using this calendar, Ingantt will not schedule tasks on Saturday, Sunday, or at night.

You can edit any of the predefined calendars using the **Calendar Properties** dialog or create your own calendars based on them using the **Add Calendar** dialog.

## Calendar Exceptions

Calendar exceptions are dates on which work is done (or not done at all) differently than specified in Weekdays.

Calendar exceptions can be specified:

- In the **Resource Properties** dialog for a particular resource.
- In the **Calendar Properties** for a particular calendar to make projects, resources, or tasks using this calendar have this exception.

For example, if you want to configure a vacation for a person, add it as an exception for this resource. If you want to configure a holiday for everyone, add it as an exception to a calendar that everyone uses.

When adding or editing calendar exceptions, you specify working time periods for the exception. If you don't specify any, the exception has no working time, meaning it defines a day off.

## Empty and Partial Calendars

If you do not add any working time to a calendar, it is empty and cannot be used for scheduling. Such calendars are marked with a warning icon in the list of calendars, and the number of such calendars is shown in the navigation drawer.

However, there are situations when your calendar is not empty but still doesn't have enough working time to schedule a particular task. These situations can only be detected when scheduling is done.

If you assign an empty calendar, or a calendar that doesn't have enough working time, to any entity (task, resource, project) and scheduling cannot proceed, an error is shown, and the last action is reverted.
