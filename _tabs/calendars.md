---
layout: post
toc: true
title: Calendars
icon: fas fa-calendar
order: 4
---

Calendars define days/time when work can be done. This definition is done through 2 types of calendar data:

- **Weekdays**. Work time is set for each day of a week: Sunday, Monday, Tuesday etc. This defines typical, routine calendar for work.
- **Exceptions**. If work is not done or done in different time periods on a particular date, this is defined as a calendar exception.

## Project Calendar

Project has a **Calendar** associated with it as specified in **Project Properties** dialog. This calendar defines how tasks not assigned to work resources or their own calendars are scheduled. Also, days off like weekends are shown in the Gantt chart according to this calendar.

## Resource Calendar

Each [work resource]({% link _tabs/resources.md %}#resource-type) has a calendar associated with it as specified in **Base Calendar** field of **Resource Properties** dialog. Once the work resource is [assigned]({% link _tabs/tasks.md %}#resource-assignments-and-units) to a task, its calendar affects scheduling of the task.

> If you have multiple resources working according to a similar work schedule, you can create a Calendar and assign it to them. At the same time, you can specify Exceptions for each of them separately in **Resource Properties** if they have personal events like vacations or shorter/longer work periods on some dates.
{: .prompt-tip }

## Task Calendar

Task has **Calendar** property in **Task Properties** dialog. It is set to **NONE** by default, in this case:

- If a task is not assigned to any work resources, the task is scheduled according to the project's calendar.
- If a task is assigned to work resources, the task is scheduled according to their calendars.

If task's **Calendar** property is set to a calendar instead of **NONE**:

- If a task is not assigned to any work resources, the task is scheduled according to the specified calendar.
- If a task is assigned to work resources, the task is scheduled according to the intersection of the specified calendar with calendars of the assigned work resources. You can also check **Ignore resource calendars** flag in order to schedule the task only according to the specified calendar.

## Pre-defined calendars

Ingantt has 3 predefined calendars, one of which (Standard) is assigned to the Project by default.

Default Calendar | Description
:--------------- | :------------------------------------------------------------------------------------------------------
**Standard**     | Work is done each day Monday to Friday, 8 AM to 5 PM with 1 hour (12 AM to 1 PM) break.
**Night Shift**  | Work is done Monday night through Saturday morning, 11 PM to 8 AM with an hour off (3 AM to 4AM) break.
**24-hours**     | Work is done 24 hours a day each day.

As mentioned above, the Standard calendar defines that work is done Monday-Friday 8 AM - 5 PM with 1-hour break. This means that when using this calendar Ingantt will not schedule tasks on Saturday, Sunday or at night.

You can edit any of the pre-defined calendars using **Calendar Properties** dialog or make your own calendars based on them using **Add Calendar** dialog.

## Calendar exceptions

Calendar Exceptions are dates on which work is done (or not done at all) differently than specified in Weekdays.

Calendar Exceptions can be specified:

- in **Resource Properties** dialog for a particular resource
- in **Calendar Properties** for a particular calendar to make project, resources or tasks using this Calendar have this exception

For example, if you would like to configure a vacation for a person, add it as an exception for this resource. If you would like to configure a holiday for everyone, add it as an exception to a calendar which everyone uses.

When adding or editing calendar exceptions you specify working time periods for the exception. If you don't specify any, you make the Exception having no working time, which means that the exception defines a day off.

## Empty and partial calendars

If you do not add any working time to a calendar, it is empty, so it cannot be used for scheduling. Such calendars are marked with a warning icon in the list of calendars and the number of such calendars is shown in the navigation drawer.

However, there are situations, when your calendar is not empty, but still doesn't have enough working time to schedule a particular task. These situations can only be detected when scheduling is done.

If you assign an empty calendar, or a calendar which doesn't have enough working time, to any entity (task, resource, project) and thus scheduling cannot proceed, an error is shown, and the last action is reverted.
