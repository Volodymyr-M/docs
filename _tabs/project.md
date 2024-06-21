---
layout: post
toc: true
title: Project
icon: fas fa-briefcase
order: 5
---

## Project Name

By filling in the **Name** field in the **Project Properties** dialog's **General** tab, you set the name for your project. This name is also used by your project's [root summary task]({% link _tabs/tasks.md %}#root-summary-task).

## Start Date and Planning from Start and Finish Dates

By default, your project is planned from the Start date, which you can set in the **Project Start Date** field of the **Project Properties** dialog.

In some cases, it may be convenient to plan your project from the Finish date. To do so, switch to **Plan from Finish date** in the **Project Properties** dialog and edit the **Project Finish Date**.

Keep in mind:

- For projects planned from the Start date, the default [constraint]({% link _tabs/tasks.md %}#constraints) for newly created tasks is **As soon as possible**.
- For projects planned from the Finish date, the default constraint for newly created tasks is **As late as possible**.

When switching between planning from Start and Finish, constraints of existing tasks are not changed except for [summary tasks]({% link _tabs/tasks.md %}#summary-tasks), including the [root summary task]({% link _tabs/tasks.md %}#root-summary-task).

For summary tasks:

- The **As soon as possible** constraint is replaced with **As late as possible** when switching from planning from Start to Finish.
- The **As late as possible** constraint is replaced with **As soon as possible** when switching from planning from Finish to Start.

## First Day of the Week

Depending on your country, a week may start on Sunday or Monday. You can update the **First Day of Week** field on the **Regional** tab of the **Project Properties** dialog to change the default setting for your project.

Changing this property updates the user interface, including the Gantt chart on some zoom levels, but does not affect scheduling. Update [Calendars]({% link _tabs/calendars.md %}) if necessary to update the schedule.

## Currency and Currency Position

You can change the default currency used in your project by filling in the **Currency** field on the **Regional** tab of the **Project Properties** dialog. Specify the currency as a sign (like €), a shortcut (EUR), or the full name (euro).

Set the **Currency Position** field to specify whether the currency appears before or after the value, with or without a space.

When you change the currency, cost values are not recalculated.

## Hours per Day, Days per Week, Days per Month

In Ingantt, you can specify [Duration]({% link _tabs/tasks.md %}#duration), [Work]({% link _tabs/tasks.md %}#work), or [Lag]({% link _tabs/tasks.md %}#lag-and-lead-time) in Hours, Days, Weeks, and Months.

For example, setting a task's duration to 2 Days means 16 hours using the default settings.

By default:

- 1 Day equals 8 hours.
- 1 Week equals 5 days (40 hours).
- 1 Month equals 20 days (160 hours).

You can change these default settings on the **Advanced** tab of the **Project Properties** dialog.

> You should have a very good reason to change any of these settings. Keep them set to defaults for most projects.
{: .prompt-info }
