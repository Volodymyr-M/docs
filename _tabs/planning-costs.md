---
layout: post
toc: true
title: Planning Costs
icon: fas fa-sack-dollar
order: 6
---

Using individual tasks' fixed costs combined with the costs of resources assigned to the tasks, Ingantt calculates the total Cost of each task as shown in the **Cost** column in the list of tasks.

> If you don't see the **Cost** column in the list of tasks, make sure the **Cost column** flag is checked on the **Task Columns** tab of **Options** dialog.
{: .prompt-info }

Each [summary task]({% link _tabs/tasks.md %}#summary-tasks) shows the total Cost of all its subtasks.

Project's [root summary task]({% link _tabs/tasks.md %}#root-summary-task) shows the total Cost of the entire project.

## Task's Fixed Cost

By filling in the **Fixed Cost** property in the **Task Properties** dialog you can set the cost of the task regardless of its resources. For example, someone who does the task already has provided a total cost estimation of it for you, or there is some cost of the task, that you need to spend on top of the costs of its resources.

> If you need to assign the same fixed cost to multiple tasks, it might be easier to create a Cost resource and assign it to the tasks, especially if the cost can change in the future: you'll only need to change it in one place.
{: .prompt-tip }

## Resource's Cost

By filling in the **Cost** property in the **Resource Properties** dialog you can set the cost of the resource, thus affecting the total Cost of all tasks to which the resource is [assigned]({% link _tabs/tasks.md %}#resource-assignments-and-units). Depending on the [type of the resource]({% link _tabs/resources.md %}#resource-type), you set the property

- as a rate (like hourly rate of a contractor) for **work** resources
- as a cost per unit (per piece, per ton, per box etc.) for **material** resources
- as a cost in total for **cost** resources

As **work** resources is the only type which has a calendar, the cost of this type of resource is specified per hour, per day, per week or per month. By default, a day is 8 hours, a week is 5 days (40 hours) and a month is 20 days. These defaults can be changed on the **Advanced** tab of **Project Properties** dialog.

When a work resource is assigned to a task, you can specify **Units** value as a number different from the default 100%. This has impact on cost calculations, for example, if **Units** is 50% then the calculated cost for the resource in the task is half of what it would be with 100% Units.

In **material** resources cost is specified per unit depending on how you define the meaning of the unit. It can be some weight measurement (like a pound, kilogram, ton etc.), length or volume measurement (foot, meter, mile, gallon, liter etc.) or any other measurement (container, box, piece, square foot etc.).

For example, if fuel is used in your project, you can add "fuel" material resource and specify the cost per gallon for it in **Resource Properties**. Then when assigning the resource to tasks in which the fuel is used you specify the number of gallons necessary for each task as **Units**, and Ingantt calculates the total cost of the fuel (as well as other costs) automatically for you.

A **cost** resource is just another fixed expense that you might want to assign to multiple tasks. Unlike material resources, cost resources do not have Units when assigning, so use this type for fixed expenses which are not normally specified in any measurements, like installation cost. If you have multiple tasks with the same Fixed Cost caused by the same reason, create a cost resource and assign it to all these tasks, instead of filling in **Fixed Cost** field of each of them separately.

Multiple resources of any type can be assigned to a task.

## Currency

If your project uses a different currency than the one that is default in Ingantt, you can change the default currency on the **Regional** tab in **Project Properties** dialog. You can specify the currency as a sign (like €), shortcut (EUR), or full name (euro).

On the same tab you can also specify the **Currency Position** (before or after the cost value, with or without a space in-between).

> When you change currency, cost values are not recalculated.
