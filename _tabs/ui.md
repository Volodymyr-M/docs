---
layout: post
toc: true
title: User Interface
icon: fas fa-window-maximize
order: 7
---

## Select multiple items

On **Android** and **iOS** versions use a long press to select another item. Just hold your finger on the item a little longer than when you tap.

On **Windows**, **macOS** and **Web** versions you can also use the following methods:

- hold _Ctrl_ while clicking items with your mouse to select more individual items
- hold _Shift_ to select groups of items in-between previously selected and the newly selected item.

This works in all lists (tasks, resources, calendars) and bars representing tasks in the Gantt chart.

## Add and insert items

- If you have an item (task, resource or calendar) selected, clicking on **+** button inserts a new item below the selected one.
- If you have multiple items selected, clicking on **+** button inserts a new button below all of them.
- If no items are selected, clicking on **+** button adds a new item to the end of the list.

## Task Views

There are multiple ways to see tasks in Ingantt. The following task views are available:

- **Split View**
- **Edit Mode**
- **Editable Split View**
- **Gantt Chart Only**
- **List Only**

All these views are fully functional, meaning that you can do every action available for tasks in any view, even when you use **Gantt Chart Only** view. Just use the ability to [select multiple items](#select-multiple-items) anywhere: in the task list or the Gantt chart, as well as the ability to open **Task Properties** by double tapping/clicking (in the list and the chart).

## Task columns

Columns in all lists of tasks (**Split View**, **Editable Split View** or **List Only** views) can be turned on or off as well as rearranged using the **Options** dialog (**Task Columns** tab).

## Create with AI

By using Artificial Intelligence (AI), Ingantt can generate full project plans for you based on the description of your project.

> See this page for a list of countries and languages supported by the AI: [https://ai.google.dev/gemini-api/docs/available-regions](https://ai.google.dev/gemini-api/docs/available-regions){:target="_blank"}.
{: .prompt-warning }

To create a project schedule with AI:

1. Click on **+** when viewing the list of your projects
2. Choose **Create new with AI**.
3. Enter the description of your project in the dialog box.
4. Click **Save**.

> Your descriptions can be as generic as _"Development of an iOS food delivery app"_ or as specific as possible. If your project is big, try splitting it into sub-projects and generating separate project plans for them.
{: .prompt-tip }

## Opening MPP files

Ingantt can open local files in Microsoft Project's MPP format (".mpp" extension). If you make changes to such a file, they are saved by Ingantt in a new file using XML format which can also be opened by Microsoft Project.

> To open MPP files Ingantt sends them through a secure connection to Ingantt web service which converts them to XML format. Your files are not stored on the service. Internet connection is required.
{: .prompt-info }

## Printing / PDF and PNG export

Ingantt outputs your Gantt chart as a PDF file when **Printable PDF** is chosen in the main menu. This file can be opened in your PDF reader app and then printed using the available printing functionality in that app.

The file is generated using the same options as the Gantt chart in the user interface. This means, for example, that if the names of your tasks are set to be not visible in the **Options** dialog, task names in the generated PDF file will not be shown as well. Also, when you zoom in or out the Gantt chart in the user interface, the resulting PDF file has the same zoom settings.

Similarly, when you choose **Export to PNG image** Ingantt creates a PNG file using the same options as the Gantt chart in the user interface, even including the current theme (light/dark).

## Supported languages

If the locale of your device is set to one of the supported languages, Ingantt uses the language in the user interface.

The following user interface languages are supported by Ingantt:

- English
- French
- German
- Italian
- Polish
- Portuguese
- Spanish
- Ukrainian

If the locale of your device is set to none of the supported languages, Ingantt uses English in the user interface.

Regardless of the language of the user interface, you can use any language in your task names and other texts within your schedules.

## Keyboard shortcuts

> Not applicable on **Android** and **iOS** versions.
> On **macOS** use ⌘ key instead of _Ctrl_.

Shortcut               | Description
:--------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
**Ctrl + X**           | Cut (copy and delete) the currently selected items to the clipboard.
**Ctrl + C**           | Copy the currently selected items to the clipboard.
**Ctrl + V**           | Paste the items in the clipboard to the current view. If an item is selected in the view, items are pasted below the item. If no items are selected, the items are pasted to the end of the list.
**Ctrl + Z**           | Undo the last action.
**Ctrl + Y**           | Redo the last action that was undone.
**Ctrl + S**           | Save changes to a file.
**A**                  | Add a new item.
**Del**                | Delete the currently selected items.
**Enter**              | Show **Properties** dialog for the currently selected item. If multiple items are selected, the dialog is shown for the top item.
**Arrow Up**           | Select the previous item.
**Arrow Down**         | Select the next item.
**Ctrl + Arrow Up**    | Move selected tasks up.
**Ctrl + Arrow Down**  | Move selected tasks down.
**Ctrl + Arrow Left**  | Decrease indent of selected tasks.
**Ctrl + Arrow Right** | Increase indent of selected tasks.
**R**                  | Switch to **Resources** view.
**C**                  | Switch to **Calendars** view.
**T**                  | Switch to **Tasks** view.
**P**                  | Show **Project Properties** dialog.
**I**                  | Zoom In the Gantt chart.
**O**                  | Zoom Out the Gantt chart.
**L**                  | Link selected tasks.
**U**                  | Unlink (break the link between) selected tasks.
