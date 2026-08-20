# GPCH_kanban

A single-page operational Kanban dashboard designed for GPCH Crystal Club to organise daily tasks, ordering, receiving, guest notes, shift handovers and recurring operational schedules in one browser-based workspace.

## Live Dashboard

https://averydimbulb79.github.io/GPCH_kanban/

## Current Version

Version 5.4

## Core Features

### Kanban Board

The dashboard is organised into five operational columns:

1. TO DO
   General operational tasks and follow-ups.

2. TO ORDER
   Items requiring ordering, replenishment or procurement.

3. TO RECEIVE
   Items that have been ordered and are awaiting receipt.

4. GUEST NOTES
   Guest preferences, requests, room information and other relevant service notes.

5. HANDOVER
   Outstanding matters and information requiring communication between shifts.

Cards can be moved between columns using drag-and-drop.

TO ORDER cards also include a dedicated "Move to Receive" function for transferring ordered items directly into the TO RECEIVE workflow.

## Today's Scheduled Tasks

Recurring operational duties are displayed separately from the Kanban as a floating overlay in the top-right corner.

The overlay uses an 80% opaque background so the main board remains visible underneath while scheduled tasks remain readable.

The schedule can be shown or hidden using:

"Toggle Schedule"

Scheduled tasks can be marked as completed for the current day.

## Schedule Manager

The built-in schedule manager supports several recurrence patterns:

• Weekly tasks on selected weekdays
• First N days of every month
• Last N days of every month
• Specific day of every month
• One-off dated tasks

Each scheduled task can include:

• Task name
• Time
• Category
• Recurrence rule

Scheduled tasks can be added, edited and deleted through the Manage Schedule interface.

## Board Controls

The main toolbar provides:

• + Add
• Manage Schedule
• Toggle Schedule
• Search
• Column filtering

The + Add interface allows users to create:

• To Do tasks
• To Order items
• To Receive items
• Guest Notes
• Handover notes

Each card type uses fields appropriate to its operational purpose.

## Ordering Workflow

The ordering workflow follows:

TO ORDER → TO RECEIVE → RECEIVED

Once an order has been placed, the card can be transferred to TO RECEIVE.

When the item physically arrives, it can be marked as received and removed from the active board.

## Data Storage

The dashboard uses browser localStorage for persistent storage.

Tasks, guest notes, handovers and scheduled tasks remain available after the browser is closed or the page is refreshed.

IMPORTANT:

Data is stored locally in the browser and is not currently synchronised between devices.

Opening the dashboard on another computer or browser will therefore create a separate local dataset.

A shared database or backend would be required for multi-device synchronisation.

## Version History

### Version 5.4

• Fixed scheduled-task deletion
• Improved deletion handling and confirmation
• Scheduled tasks now correctly disappear from both the Schedule Manager and Today's Scheduled Tasks after deletion

### Version 5.3

• Added TO RECEIVE column
• Added direct transfer from TO ORDER to TO RECEIVE
• Added receipt-status workflow
• Added Mark Received function
• Expanded the board from four to five operational columns
• Introduced individual colour identities for each Kanban column
• Improved card and column visual hierarchy

### Version 5.2

• Reorganised primary controls into one header row
• Final control order:
  + Add
  Manage Schedule
  Toggle Schedule
• Removed the separate floating schedule restoration button
• Prevented schedule controls from covering the + Add button

### Version 5.1

• Rebuilt the page rendering architecture for improved reliability
• Four core Kanban columns made immediately visible on page load
• Reduced dependency on JavaScript-generated structural elements
• Improved browser compatibility and defensive localStorage handling

### Version 5.0

• Major operational redesign
• Replaced the generic Kanban structure with Crystal Club-specific workflows
• Introduced:
  TO DO
  TO ORDER
  GUEST NOTES
  HANDOVER
• Added specialised forms for different card types
• Added search and column filtering
• Added drag-and-drop movement
• Separated Today's Scheduled Tasks from the Kanban itself

### Version 4.0

• Converted Today's Scheduled Tasks into a floating overlay
• Added approximately 80% opaque background
• Added overlay hide/show functionality
• Removed scheduled tasks from the main Kanban layout

### Version 3.x

• Added advanced recurring schedule management
• Added first-days-of-month scheduling
• Added last-days-of-month scheduling
• Added specific monthly dates
• Added one-off dated tasks
• Removed the Reset Demo control to prevent accidental data loss
• Renamed project to GPCH Crystal Club

### Earlier Versions

Initial prototypes established the core concepts of:

• Browser-based single-page Kanban
• Recurring operational tasks
• Daily schedule display
• Task cards
• Browser persistence
• Crystal Club-specific operational workflow

## Technology

The application is deliberately lightweight and self-contained.

• HTML
• CSS
• Vanilla JavaScript
• Browser localStorage
• No external JavaScript framework
• No external database
• No installation required

The entire dashboard can be deployed as a static webpage through GitHub Pages.

## Deployment

The project is hosted using GitHub Pages from the GPCH_kanban repository.

Live version:

https://averydimbulb79.github.io/GPCH_kanban/

## Project Status

Active development.

The dashboard is being progressively refined around actual GPCH Crystal Club operational requirements, with emphasis on speed, visibility, simple handovers and minimal administrative friction.
