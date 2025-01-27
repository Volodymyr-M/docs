---
layout: post
toc: true
title: User Interface
icon: fas fa-window-maximize
order: 7
---

## Select Multiple Items

On **Android** and **iOS** versions, use a long press to select additional items. Simply hold your finger on the item a little longer than when you tap.

On **Windows**, **macOS**, and **Web** versions, you can also use the following methods:

- Hold _Ctrl_ while clicking items with your mouse to select multiple individual items.
- Hold _Shift_ to select a group of items between the previously selected item and the newly selected item.

This works in all lists (tasks, resources, calendars) and for bars representing tasks in the Gantt chart.

## Add and Insert Items

- If an item (task, resource, or calendar) is selected, clicking the **+** button inserts a new item below the selected one.
- If multiple items are selected, clicking the **+** button inserts a new item below all of them.
- If no items are selected, clicking the **+** button adds a new item to the end of the list.

## Task Views

There are multiple ways to view tasks in Ingantt. The following task views are available:

- **Split View**
- **Edit Mode**
- **Editable Split View**
- **Gantt Chart Only**
- **List Only**

All these views are fully functional, meaning you can perform any action available for tasks in any view, even in the **Gantt Chart Only** view. Utilize the ability to [select multiple items](#select-multiple-items) anywhere—in the task list or the Gantt chart—and open **Task Properties** by double-tapping/clicking (in the list and the chart).

## Task Columns

Columns in all task lists (**Split View**, **Editable Split View**, or **List Only** views) can be turned on or off and rearranged using the **Options** dialog (**Task Columns** tab).

## Create with AI

Ingantt can generate full project plans for you based on the description of your project using Artificial Intelligence (AI).

{% include embed/youtube.html id='sOjhGy5BJso' %}

To create a project schedule with AI:

1. Click on **+** when viewing the list of your projects.
2. Choose **Create new with AI**.
3. Enter the description of your project in the dialog box.
4. Click **Save**.

> Your descriptions can be as generic as _"Development of an iOS food delivery app"_ or as specific as possible. If your project is large, try splitting it into sub-projects and generating separate project plans for them. The AI can generate different results, so if you are not happy with the output, try again.
{: .prompt-tip }

## Opening MPP Files

Ingantt can open local files in Microsoft Project's MPP format (".mpp" extension). If you make changes to such a file, they are saved by Ingantt in a new file using the XML format, which can also be opened by Microsoft Project.

> To open MPP files, Ingantt sends them through a secure connection to the Ingantt web service, which converts them to XML format. Your files are not stored on the service. An internet connection is required.
{: .prompt-info }

## Printing / PDF and PNG Export

Ingantt outputs your Gantt chart as a PDF file when **Printable PDF** is chosen in the main menu. This file can be opened in your PDF reader app and printed using the available printing functionality in that app.

The file is generated using the same options as the Gantt chart in the user interface. This means, for example, that if the names of your tasks are set to be not visible in the **Options** dialog, task names in the generated PDF file will not be shown either. Additionally, when you zoom in or out on the Gantt chart in the user interface, the resulting PDF file will have the same zoom settings.

Similarly, when you choose **Export to PNG image**, Ingantt creates a PNG file using the same options as the Gantt chart in the user interface, including the current theme (light/dark).

## Supported Languages

If the locale of your device is set to one of the supported languages, Ingantt uses that language in the user interface.

The following user interface languages are supported by Ingantt:

- Chinese (Simplified)
- English
- French
- German
- Hindi
- Indonesian
- Italian
- Japanese
- Korean
- Malay
- Polish
- Portuguese
- Spanish
- Thai
- Turkish
- Ukrainian

If the locale of your device is set to a language not supported by Ingantt, the user interface will default to English.

Regardless of the language of the user interface, you can use any language in your task names and other texts within your schedules.

## Keyboard Shortcuts

> Not applicable on **Android** and **iOS** versions.
> On **macOS**, use the ⌘ key instead of _Ctrl_.

| Shortcut               | Description                                                                                                                                       |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ctrl + X**           | Cut (copy and delete) the currently selected items to the clipboard.                                                                              |
| **Ctrl + C**           | Copy the currently selected items to the clipboard.                                                                                               |
| **Ctrl + V**           | Paste the items from the clipboard to the current view. If an item is selected, the items are pasted below it. If no items are selected, the items are pasted at the end of the list. |
| **Ctrl + Z**           | Undo the last action.                                                                                                                             |
| **Ctrl + Y**           | Redo the last action that was undone.                                                                                                             |
| **Ctrl + S**           | Save changes to a file.                                                                                                                           |
| **A**                  | Add a new item.                                                                                                                                   |
| **Del**                | Delete the currently selected items.                                                                                                              |
| **Enter**              | Show the **Properties** dialog for the currently selected item. If multiple items are selected, the dialog is shown for the top item.             |
| **Arrow Up**           | Select the previous item.                                                                                                                         |
| **Arrow Down**         | Select the next item.                                                                                                                             |
| **Ctrl + Arrow Up**    | Move selected tasks up.                                                                                                                           |
| **Ctrl + Arrow Down**  | Move selected tasks down.                                                                                                                         |
| **Ctrl + Arrow Left**  | Decrease indent of selected tasks.                                                                                                                |
| **Ctrl + Arrow Right** | Increase indent of selected tasks.                                                                                                                |
| **R**                  | Switch to **Resources** view.                                                                                                                     |
| **C**                  | Switch to **Calendars** view.                                                                                                                     |
| **T**                  | Switch to **Tasks** view.                                                                                                                         |
| **P**                  | Show the **Project Properties** dialog.                                                                                                           |
| **I**                  | Zoom In the Gantt chart.                                                                                                                          |
| **O**                  | Zoom Out the Gantt chart.                                                                                                                         |
| **L**                  | Link selected tasks.                                                                                                                              |
| **U**                  | Unlink (break the link between) selected tasks.                                                                                                   |

