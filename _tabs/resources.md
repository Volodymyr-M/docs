---
layout: post
toc: true
title: Resources
icon: fas fa-user
order: 3
---

## Resource Type

Ingantt supports 3 types of resources:

Resource Type | Description
:------------ | :---------------------------------------------------------------------------------------------------
**Work**      | Someone or something doing your task. Can be a person, team, contractor company, or equipment.
**Material**  | Something which is used to do your task. Materials, ingredients, components.
**Cost**      | Cost which can be applied to multiple of your tasks. Delivery cost, deployment cost, any fixed cost.

Only work resources, when assigned to tasks, affect scheduling.

All types of resources affect cost calculations if **Cost** field is filled in for the resource.

## Resource Cost

All types of resources, if you specify their cost, affect the total cost of tasks to which they are [assigned]({% link _tabs/tasks.md %}#resource-assignments-and-units).

For **work** resources cost is specified as a rate: hourly, daily, weekly or monthly cost. Once such a resource is assigned to a task, Ingantt uses the task's scheduling data to calculate the cost of the resource for this task and add it to the task's total cost.

For **material** resources cost is specified per **Unit**. So that once the resource is assigned to a task, you can specify the number of Units used by the task and the total cost is calculated automatically. A Unit is something that you define for yourself: can be any measurement of material items (a ton, a box, a gallon etc.), so you set the price per this Unit as resource's **Cost**.

For **cost** resources you specify the total cost of the resource. Units are not applicable in this case, you just specify the **Cost** as a fixed price which is added to a task's cost once the resource is assigned to the task.

For more information on costs, see [Planning costs]({% link _tabs/planning-costs.md %}).

## Overallocated resources

A work resource can be **overallocated**, which means that it has more work assigned than it can do based on its calendar data. For example, if your project has only 2 tasks with a duration of 1 day with no [dependency]({% link _tabs/tasks.md %}#predecessors-and-dependencies) between them both assigned to the same work resource, the resource is overallocated: in that one calendar day the resource has to do 2 days of work! To resolve this, in this example simply linking the tasks fixes the issue.

If a task has overallocated resources assigned, Ingantt shows a special icon for it in the list of tasks.

If a resource is overallocated, Ingantt shows a special icon for it in **Resources** view and **Resource Usage** view.

Also, Ingantt counts such tasks and resources and shows the numbers in the navigation drawer.

## Auto-leveling

It's possible to set dependencies between tasks and thus modify their position on the timeline. In projects with many resources and tasks it's easy to miss setting a dependency, so that your schedule can contain 2 or more tasks assigned to the same work resource but which (because of the lack of dependency) are scheduled to be done at the same time. This means that the resource has to do more work than it can do in that time: it is overallocated, and you are notified about that by Ingantt using special icons in tasks and resources lists.

You can resolve the over-allocation manually by setting dependencies or constraints to move some tasks so that work is not done at the same time.

An alternative way to resolve over-allocation is auto-leveling. If you choose to **Auto-level resources** in the main menu Ingantt automatically shifts some tasks further in the timeline to prevent resources from being overallocated. You can clear these automatic adjustments by choosing **Clear leveling** in the main menu.

## Resource Usage

**Resource Usage** view allows to see all resource assignments and the amount of [Work]({% link _tabs/tasks.md %}#work) that each work resource does during each period in the timeline.

Just like with the Gantt chart, you can zoom the timeline in or out to see more or less detailed view.

If the resource has to perform more Work than the calendars allow for the given time period in the timeline, the corresponding Work is highlighted in red.
