---
layout: post
toc: true
title: Planning Costs
icon: fas fa-sack-dollar
order: 6
---

Using individual tasks' fixed costs combined with the costs of resources assigned to the tasks, Ingantt calculates the total cost of each task as shown in the **Cost** column in the list of tasks.

*Task's **Cost** = Task's **Fixed Cost** + Costs of Resources assigned to the Task*

> If you don't see the **Cost** column in the list of tasks, make sure the **Cost column** flag is checked on the **Task Columns** tab of the **Options** dialog.
{: .prompt-info }

## Summary Tasks Cost

In its **Cost** field, each [summary task]({% link _tabs/tasks.md %}#summary-tasks) shows the total cost of all its subtasks.

However, just like with a regular task, you can [assign resources]({% link _tabs/tasks.md %}#resource-assignments-and-units) and set the **Fixed Cost** field for a summary task, thus affecting the **Cost** of the summary task by adding costs on top of the total cost of the subtasks.

*Summary Task's **Cost** = Total Cost of all the subtasks + Summary Task's **Fixed Cost** + Costs of Resources assigned to the Summary Task*

Use your project's [root summary task]({% link _tabs/tasks.md %}#root-summary-task) to see and adjust the total cost of the entire project.

## Task's Fixed Cost

By filling in the **Fixed Cost** property in the **Task Properties** dialog, you can set the cost of the task regardless of its resources. For example, if someone who does the task has already provided a total cost estimation, or if there is an additional cost for the task beyond the costs of its resources, you can set it here.

> If you need to assign the same fixed cost to multiple tasks, it might be easier to create a cost resource and assign it to the tasks, especially if the cost can change in the future. You'll only need to change it in one place.
{: .prompt-tip }

## Resource Cost

By filling in the **Cost** property in the **Resource Properties** dialog, you can set the cost of the resource, thus affecting the total cost of all tasks to which the resource is [assigned]({% link _tabs/tasks.md %}#resource-assignments-and-units). Depending on the [type of the resource]({% link _tabs/resources.md %}#resource-type), you set the property:

- As a rate (e.g., hourly rate of a contractor) for **work** resources
- As a cost per unit (e.g., piece, ton, box, gallon) for **material** resources
- As a total cost for **cost** resources

Any number of resources of any type can be assigned to a task.

### Work Resource Cost

Since **work** resources are the only type that has a calendar, the cost of this type of resource is specified [per hour, per day, per week, or per month]({% link _tabs/project.md %}#hours-per-day-days-per-week-days-per-month).

For example, when you assign a work resource with a **Cost (rate)** of $100 per hour to a task with a 5-hour **Duration**, $500 is added to the **Cost** of the task.

When a work resource is assigned to a task, you can specify the **Units** value as a number different from the default 100%. This impacts cost calculations. For example, if **Units** is 50%, the calculated cost for the resource in the task is half of what it would be with 100% Units.

### Material Resource Cost

For **material** resources, the cost is specified per unit based on how you define the unit. It can be a weight measurement (e.g., pound, kilogram, ton), length or volume measurement (e.g., foot, meter, mile, gallon, liter), or any other measurement (e.g., container, box, piece, square foot).

For example, if fuel is used in your project, you can add a "fuel" material resource and specify the cost per gallon in **Resource Properties**. Then, when assigning the resource to a task that uses fuel, you specify the number of gallons as **Units**, and Ingantt adds the calculated cost of the fuel to the **Cost** of the task.

### Cost Resource

A **cost** resource is a fixed expense you might want to assign to multiple tasks. Unlike material resources, cost resources do not have units when assigning. Use this type for fixed expenses not normally specified in measurements, like installation costs. If multiple tasks have the same fixed cost due to the same reason, create a cost resource and assign it to all these tasks instead of filling in the **Fixed Cost** field for each task separately.

## Currency

If your project uses a different currency than the default in Ingantt, you can change the default currency on the **Regional** tab in the **Project Properties** dialog. Specify the currency as a sign (e.g., €), shortcut (EUR), or full name (euro).

On the same tab, you can also specify the **Currency Position** (before or after the cost value, with or without a space in between).

> When you change currency, cost values are not recalculated.
