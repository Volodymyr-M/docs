---
layout: post
toc: true
title: Project
icon: fas fa-briefcase
order: 5
---

## Project Name

By filling in the **Name** field in the **Project Properties** dialog's **General** tab you set the name for your project. This name is also used by your project's [root summary task]({% link _tabs/tasks.md %}#root-summary-task).

## Start Date and planning from Start and Finish dates

By default, your project is set to be planned from the Start date, and you can set it in the **Project Start Date** field of the **Project Properties** dialog.

But in some (rather rare) cases it is convenient to plan your project knowing its Finish date first. For such cases Ingantt supports planning from the Finish date. To do so, just switch to **Plan from Finish date** in the **Project Properties** dialog and edit the **Project Finish date**.

There are some things to keep in mind:

- For projects planned from the Start date the default [constraint]({% link _tabs/tasks.md %}#constraints) for newly created tasks is **As soon as possible**.
- For projects planned from the Finish date the default constraint for newly created tasks is **As late as possible**.

Also, when you switch between planning from Start and Finish, constraints of existing tasks in your project are not changed except for [summary tasks]({% link _tabs/tasks.md %}#summary-tasks), including the [root summary task]({% link _tabs/tasks.md %}#root-summary-task).

For summary tasks:

- **As soon as possible** constraint is replaced with **As late as possible** when you switch from planning from Start to planning from Finish
- **As late as possible** constraint is replaced with **As soon as possible** when you switch from planning from Finish to planning from Start.

## First Day of Week

Depending on your country, a week can traditionally be considered to start either from Sunday or from Monday. You can update the **First day of week** field on the **Regional** tab of **Project Properties** dialog to change the default setting in your project.

Changing this property updates the user interface, including the Gantt chart on some of its zoom levels, but this change does not affect scheduling. If necessary, update [Calendars]({% link _tabs/calendars.md %}) in order for the schedule to be updated.

## Currency and Currency Position

You can change the default currency used in your project by filling in the **Currency** field on the **Regional** tab of **Project Properties** dialog. You can specify the currency as a sign (like €), shortcut (EUR), or full name (euro).

Different currencies have different rules of placing them next to a value. Set before or after, with or without space in-between in the **Currency Position** field.

When you change currency, cost values are not recalculated.

## Hours per Day, Days per Week, Days per Month

In Ingantt you can specify [Duration]({% link _tabs/tasks.md %}#duration), [Work]({% link _tabs/tasks.md %}#work) or [Lag]({% link _tabs/tasks.md %}#lag-and-lead-time) in Hours, Days, Weeks and Months.

For example, you can set your task's duration to 2 Days and using default settings, Ingantt knows that these 2 "Days" are actually equal to 16 hours.

By default, 1 Day is equal to 8 hours, 1 Week is equal to 5 days (40 hours), 1 Month is equal to 20 days (160 hours).

On the **Advanced** tab of **Project Properties** dialog the default settings of **Hours per Day**, **Days per Week** and **Days per Month** can be changed.

> You should have a very good reason to change any of these settings. Keep them set to defaults in most projects.
{: .prompt-info }
