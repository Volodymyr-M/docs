---
layout: post
toc: true
title: Resources
icon: fas fa-user
order: 3
---

## Resource Type

Ingantt supports 3 types of resources:

| Resource Type | Description                                                                                      |
|---------------|--------------------------------------------------------------------------------------------------|
| **Work**      | Someone or something performing your task. This can be a person, team, contractor company, or equipment. |
| **Material**  | Items used to complete your task, such as materials, ingredients, or components.                 |
| **Cost**      | Costs that can be applied to multiple tasks, such as delivery costs, deployment costs, or any fixed costs. |

Only work resources, when assigned to tasks, affect scheduling.

All types of resources affect cost calculations if the **Cost** field is filled in for the resource.

## Resource Cost

All types of resources, when their cost is specified, affect the total cost of tasks to which they are [assigned]({% link _tabs/tasks.md %}#resource-assignments-and-units).

For **work** resources, the cost is specified as a rate: hourly, daily, weekly, or monthly. Once such a resource is assigned to a task, Ingantt uses the task's scheduling data to calculate the resource's cost for that task and add it to the task's total cost.

For **material** resources, the cost is specified per **Unit**. Once the resource is assigned to a task, you can specify the number of units used by the task, and the total cost is calculated automatically. A Unit is something that you define: can be any measurement of material items (e.g., a ton, a box, a gallon). You define what a Unit means in your case implicitly and set the price per Unit as the resource's **Cost**.

For **cost** resources, you specify the total cost of the resource. Units are not applicable in this case. You simply specify the **Cost** as a fixed price, which is added to a task's cost once the resource is assigned to the task.

For more information on costs, see [Planning costs]({% link _tabs/planning-costs.md %}).

## Overallocated Resources

A work resource can be **overallocated**, meaning it has more work assigned than it can complete based on its calendar data. For example, if your project has two tasks, each with a duration of one day and no [dependency]({% link _tabs/tasks.md %}#predecessors-and-dependencies) between them, both assigned to the same work resource, the resource is overallocated. The resource has to do two days of work in one calendar day! To resolve this, simply linking the tasks can fix the issue.

If a task has overallocated resources assigned, Ingantt shows a special icon for it in the list of tasks.

If a resource is overallocated, Ingantt shows a special icon for it in the **Resources** view and the **Resource Usage** view.

Additionally, Ingantt counts such tasks and resources and shows the numbers in the navigation drawer.

## Auto-Leveling

It's possible to set dependencies between tasks and thus modify their position on the timeline. In projects with many resources and tasks, it's easy to miss setting a dependency, resulting in multiple tasks assigned to the same work resource being scheduled simultaneously. This means that the resource has to do more work than it can do in that time, it is overallocated, and Ingantt notifies you with special icons in the task and resource lists.

You can resolve overallocation manually by setting dependencies or constraints to move some tasks so that work is not done simultaneously.

An alternative way to resolve overallocation is auto-leveling. If you choose to **Auto-level resources** in the main menu, Ingantt automatically shifts some tasks further on the timeline to prevent resource overallocation. You can clear these automatic adjustments by choosing **Clear leveling** in the main menu.

## Resource Usage

The **Resource Usage** view allows you to see all resource assignments and the amount of [Work]({% link _tabs/tasks.md %}#work) that each work resource performs during each period on the timeline.

Similar to the Gantt chart, you can zoom the timeline in or out to see a more or less detailed view.

If a resource has to perform more work than the calendars allow for the given time period, the corresponding **Work** is highlighted in red.
