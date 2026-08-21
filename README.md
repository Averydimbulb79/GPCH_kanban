# GPCH_kanban

A single-page operational Kanban dashboard designed for GPCH Crystal Club to organise daily tasks, ordering, receiving, guest notes, shift handovers and recurring operational schedules in one browser-based workspace.

## Live Dashboard

https://averydimbulb79.github.io/GPCH_kanban/

## Current Version

Version 5.5

## Core Features

### Kanban Board

The dashboard is organised into five operational columns:

1. TO DO
   General operational tasks and follow-ups.

2. TO ORDER
   Items requiring ordering, replenishment or procurement.

3. TO RECEIVE
   Items that have already been ordered and are awaiting delivery or collection.

4. GUEST NOTES
   Guest preferences, requests, room information and other service-related notes.

5. HANDOVER
   Outstanding matters and information requiring communication between shifts.

Cards support drag-and-drop movement between columns.

Each column has its own colour identity for faster visual recognition while retaining a clean operational interface.

## Ordering and Receiving Workflow

The ordering workflow separates items that still require action from items already ordered:

TO ORDER → TO RECEIVE → RECEIVED

TO ORDER cards include a dedicated "Move to Receive" control.

Once an order has been placed, the card can be transferred directly to TO RECEIVE.

When the item physically arrives, it can be marked as received and removed from the active board.

This keeps pending orders and pending deliveries visually separate.

## Today's Scheduled Tasks

Recurring operational duties are displayed separately from the Kanban as a floating overlay in the top-right corner.

The schedule overlay uses an 80% opaque background, allowing the Kanban underneath to remain visible while keeping scheduled tasks readable.

The overlay does not occupy a Kanban column or reduce the usable width of the board.

It can be shown or hidden using:

"Toggle Schedule"

Scheduled tasks can also be marked as completed for the current day.

## Schedule Manager

The built-in Schedule Manager supports multiple recurrence patterns:

• Weekly tasks on selected weekdays
• First N days of every month
• Last N days of every month
• Specific day of every month
• One-off dated tasks

Each scheduled task can contain:

• Task name
• Time
• Category
• Recurrence rule

Scheduled tasks can be added, edited and deleted through the Schedule Manager.

## Main Controls

The dashboard provides:

• + Add
• Manage Schedule
• Toggle Schedule
• Export Data
• Import Data
• Search
• Column filtering

The + Add interface allows users to create:

• To Do tasks
• To Order items
• To Receive items
• Guest Notes
• Handover notes

Each type uses fields appropriate to its operational purpose rather than forcing all information into a generic task format.

## Search and Filtering

The dashboard includes a universal search function for locating information across the board.

Search can identify information such as:

• Tasks
• Items
• Room numbers
• Guest names
• Notes
• Handover information

The board can also be filtered by operational column.

## Data Storage

The dashboard uses browser localStorage for persistent storage.

Board cards, scheduled tasks and schedule-completion information remain available after refreshing or closing the browser.

No external database or account is required.

IMPORTANT:

localStorage belongs to the individual browser and device.

Data entered on one computer will not automatically appear on another computer.

For this reason, Version 5.5 introduces a portable backup and restore system.

## Export Data

"Export Data" creates a downloadable JSON backup of the current Crystal Club dashboard.

The backup includes:

• Kanban board cards
• Scheduled tasks
• Completed scheduled-task state
• Application version
• Export timestamp
• Record counts

Backup files are automatically timestamped for easier identification.

Example:

GPCH_Crystal_Club_Backup_2026-08-21_0955.json

The exported file can be stored as a backup or transferred to another computer.

## Import Data

"Import Data" restores a previously exported GPCH Crystal Club JSON backup.

The system validates the selected file before allowing it to replace the current data.

Before importing, the dashboard displays information including:

• Number of board cards
• Number of scheduled tasks
• Backup version

The user must confirm the import before any existing data is replaced.

## Import Safety Backup

Importing data could otherwise overwrite information already stored on the receiving computer.

To protect against this, Version 5.5 automatically exports the existing browser data immediately before an import is performed.

The safety file uses a filename such as:

GPCH_Crystal_Club_PreImport_Backup_2026-08-21_0955.json

This provides a recovery point if the wrong backup is imported or the previous local dataset needs to be restored.

## Moving to Another Computer

To transfer the Crystal Club Kanban:

OLD COMPUTER

1. Open the dashboard.
2. Click "Export Data".
3. Save the generated JSON backup.

NEW COMPUTER

1. Open the GPCH Crystal Club dashboard.
2. Click "Import Data".
3. Select the exported JSON backup.
4. Review the import information.
5. Confirm the import.

The board and scheduled-task data will then be restored in the new browser.

## Technology

The application is deliberately lightweight and self-contained.

• HTML
• CSS
• Vanilla JavaScript
• Browser localStorage
• JSON backup and restore
• No external JavaScript framework
• No external database
• No installation required

The dashboard can therefore be deployed as a static webpage using GitHub Pages.

## Deployment

The project is hosted using GitHub Pages from the GPCH_kanban repository.

Live dashboard:

https://averydimbulb79.github.io/GPCH_kanban/

## Version History

### Version 5.5: Data Portability

• Added Export Data
• Added Import Data
• Added portable JSON backups
• Added application version information to backups
• Added export timestamps
• Added board and schedule record counts
• Added backup-file validation
• Added confirmation before replacing browser data
• Added automatic pre-import safety backup
• Added support for transferring the complete local dataset between computers

### Version 5.4

• Fixed scheduled-task deletion
• Improved deletion event handling
• Added confirmation before scheduled-task deletion
• Scheduled tasks correctly disappear from both the Schedule Manager and Today's Scheduled Tasks after deletion

### Version 5.3

• Added TO RECEIVE column
• Expanded the board from four to five operational columns
• Added direct transfer from TO ORDER to TO RECEIVE
• Added receipt-status workflow
• Added Mark Received function
• Added individual colour identities for Kanban columns
• Improved card and column visual hierarchy

### Version 5.2

• Reorganised primary controls into a single header row
• Established:
  + Add
  Manage Schedule
  Toggle Schedule
• Removed the separate floating schedule restoration button
• Prevented schedule controls from covering the + Add control

### Version 5.1

• Rebuilt page rendering for improved reliability
• Kanban columns made immediately visible on page load
• Reduced dependency on JavaScript-generated structural elements
• Improved browser compatibility
• Added more defensive localStorage handling

### Version 5.0

• Major Crystal Club operational redesign
• Replaced the generic Kanban workflow with purpose-specific operational columns
• Introduced TO DO
• Introduced TO ORDER
• Introduced GUEST NOTES
• Introduced HANDOVER
• Added specialised forms for different card types
• Added search
• Added column filtering
• Added drag-and-drop card movement
• Separated Today's Scheduled Tasks from the Kanban board

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
• Renamed the project GPCH Crystal Club

### Earlier Versions

Initial prototypes established the core concepts of:

• Single-page browser-based Kanban
• Recurring operational tasks
• Daily schedule display
• Task cards
• Browser persistence
• Crystal Club-specific workflow design

## Current Architecture

GPCH Crystal Club remains a client-side application.

GitHub Pages hosts the application itself, while operational data remains inside the user's browser.

This architecture provides:

• Fast loading
• No login requirement
• No server maintenance
• Simple GitHub Pages deployment
• Local data persistence
• Portable manual backups

It does not currently provide real-time multi-device synchronisation.

A shared backend or cloud database would be required if the dashboard is later developed into a simultaneously shared operational board for multiple Crystal Club workstations.

## Project Status

Active development.

The dashboard is being progressively refined around GPCH Crystal Club operational requirements, with emphasis on visibility, speed, practical shift communication, data portability and minimal administrative friction.
