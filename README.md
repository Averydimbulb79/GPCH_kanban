# GPCH_kanban

A single-page operational Kanban dashboard designed for GPCH Crystal Club to manage daily tasks, ordering, receiving, guest notes, shift handovers and recurring operational schedules in one lightweight browser-based workspace.

## Live Dashboard

https://averydimbulb79.github.io/GPCH_kanban/

## Current Version

Version 5.6

## Overview

GPCH Crystal Club is a purpose-built operational dashboard rather than a generic Kanban board.

It combines five operational workflows with a recurring schedule system, search and filtering tools, drag-and-drop card management, browser persistence and portable data backups.

The application is built entirely with HTML, CSS and vanilla JavaScript and can be hosted as a static site through GitHub Pages.

## Kanban Board

The dashboard contains five colour-coded operational columns:

### TO DO

Blue

For general operational tasks, follow-ups and duties requiring action.

Examples:

• Operational checks
• Guest follow-ups
• Administrative work
• Equipment issues
• Tasks with due times

### TO ORDER

Amber

For items requiring ordering, replenishment or procurement.

Cards can contain information such as:

• Item
• Quantity
• Urgency
• Order status
• Supplier or department
• Notes

Once an order has been placed, the card can be transferred directly to TO RECEIVE.

### TO RECEIVE

Green

For items that have already been ordered and are awaiting delivery or collection.

This separates procurement work from outstanding deliveries.

When an item arrives, it can be marked as received and removed from the active board.

### GUEST NOTES

Pink

For service information associated with guests.

Cards can contain:

• Room number
• Guest name
• Arrival date
• Departure date
• Importance
• Preferences
• Requests
• Service notes
• Required actions

### HANDOVER

Violet

For information or outstanding matters requiring communication between shifts.

Cards can contain:

• Handover subject
• Room or area
• Originating shift or colleague
• Receiving shift
• Priority
• Follow-up time
• Details

## Colour-Coded Interface

The five operational categories use consistent colour identities throughout the interface:

• TO DO: Blue
• TO ORDER: Amber
• TO RECEIVE: Green
• GUEST NOTES: Pink
• HANDOVER: Violet

Version 5.6 extends this visual system to the "+ Add" interface.

When creating a new card, each category button now uses the same colour as its corresponding Kanban column.

This creates a clearer visual relationship between card creation and the destination column.

## Adding Cards

Select:

"+ Add"

The dashboard presents five colour-coded choices:

• TO DO
• TO ORDER
• TO RECEIVE
• GUEST NOTE
• HANDOVER

Each category opens a form containing fields appropriate to that particular operational function.

This avoids forcing unrelated information into a single generic task template.

## Drag-and-Drop Workflow

Cards can be dragged between operational columns.

This allows information to move as its operational status changes without recreating the card.

The ordering workflow also includes dedicated controls for the most common transition.

## Ordering and Receiving Workflow

The procurement workflow follows:

TO ORDER → TO RECEIVE → RECEIVED

A TO ORDER card includes:

"Move to Receive"

Once an order has been placed, selecting this transfers the card into TO RECEIVE.

The status becomes:

"AWAITING RECEIPT"

When the physical item arrives, it can be marked as received and removed from the active board.

This keeps two fundamentally different situations separate:

"Something still needs to be ordered"

and

"Something has been ordered but has not arrived."

## Today's Scheduled Tasks

Recurring operational duties are displayed separately from the Kanban board in a floating overlay.

The overlay appears in the top-right area of the dashboard.

It uses an approximately 80% opaque background, allowing the underlying Kanban to remain visible while keeping schedule information readable.

Importantly, the schedule is NOT a Kanban column.

It floats above the board and therefore does not consume operational column space.

## Toggle Schedule

The main control row includes:

"Toggle Schedule"

This hides or restores the Today's Scheduled Tasks overlay.

The overlay itself also contains a Hide control.

## Scheduled Task Completion

Tasks appearing in Today's Scheduled Tasks can be checked off when completed.

Completion applies to that day's scheduled occurrence rather than deleting the recurring schedule itself.

This allows a recurring duty to appear again automatically on its next scheduled date.

## Schedule Manager

Select:

"Manage Schedule"

The Schedule Manager allows recurring operational duties to be created, edited and deleted.

Each scheduled task can include:

• Task
• Time
• Category
• Recurrence rule

## Supported Scheduling Rules

The scheduling engine supports:

### Weekly

Run a task on selected weekdays.

For example:

Monday, Wednesday and Friday

or

Every day

### First N Days of Month

Run a task during the first specified number of days each month.

For example:

First 3 days of every month

### Last N Days of Month

Run a task during the final specified number of days each month.

For example:

Last 3 days of every month

The calculation automatically accounts for different month lengths.

### Specific Day of Month

Run a task on a particular calendar date every month.

For example:

Day 15 of every month

### One-Off Date

Create a scheduled task that appears on one specific date.

## Scheduled Task Management

Scheduled tasks can be:

• Added
• Edited
• Deleted
• Marked complete for the current day

Deleting a scheduled task removes the recurrence itself.

Version 5.4 corrected scheduled-task deletion so deleted entries are removed correctly from both the Schedule Manager and Today's Scheduled Tasks.

## Main Controls

The primary dashboard controls are arranged together:

• + Add
• Manage Schedule
• Toggle Schedule
• Export Data
• Import Data

This keeps the schedule controls within the main interface rather than using separate floating buttons that could obstruct other controls.

## Search

The dashboard includes a universal search field.

Search can locate information across cards, including:

• Tasks
• Items
• Room numbers
• Guest names
• Notes
• Suppliers
• Departments
• Handover information

## Column Filtering

The dashboard can be filtered to display:

• All Columns
• To Do
• To Order
• To Receive
• Guest Notes
• Handover

This is useful when the board becomes operationally busy.

## Persistent Browser Storage

The application uses browser localStorage.

This allows operational information to remain available after:

• Refreshing the page
• Closing the browser
• Restarting the computer
• Reopening the GitHub Pages dashboard

No external database is required.

## Important Storage Limitation

localStorage belongs to the specific browser and computer being used.

Data entered on one workstation does not automatically synchronise with another workstation.

GitHub Pages hosts the application itself, but it does not store the operational Kanban data.

To address computer migration and backup requirements, Version 5.5 introduced portable data export and import.

## Export Data

Select:

"Export Data"

The application generates a downloadable JSON backup containing the current operational dataset.

The backup includes:

• Kanban cards
• Scheduled tasks
• Scheduled-task completion state
• Application version
• Export timestamp
• Record counts

Backup files are automatically timestamped.

Example:

GPCH_Crystal_Club_Backup_2026-08-21_1427.json

The JSON file can be retained as a backup or transferred to another computer.

## Import Data

Select:

"Import Data"

Choose a previously exported GPCH Crystal Club JSON backup.

Before importing, the application validates the file to ensure it contains the expected GPCH Crystal Club data structure.

The import confirmation displays information including:

• Number of board cards
• Number of scheduled tasks
• Backup version

The import proceeds only after confirmation.

## Automatic Pre-Import Backup

Importing a backup replaces the browser's current GPCH Crystal Club dataset.

As a safeguard, the application automatically exports the existing data immediately before completing an import.

The safety backup uses a filename such as:

GPCH_Crystal_Club_PreImport_Backup_2026-08-21_1427.json

This provides a recovery point if:

• The wrong backup is selected
• Older data is imported accidentally
• The previous local dataset needs to be restored

## Moving to Another Computer

To migrate the Kanban:

OLD COMPUTER

1. Open GPCH Crystal Club.
2. Click "Export Data".
3. Save the generated JSON file.
4. Transfer the file to the new computer.

NEW COMPUTER

1. Open the GPCH Crystal Club dashboard.
2. Click "Import Data".
3. Select the JSON backup.
4. Review the backup information.
5. Confirm the import.

The Kanban cards and scheduled-task data will then be restored in the new browser.

## Technology

The application deliberately uses a lightweight architecture:

• HTML
• CSS
• Vanilla JavaScript
• Browser localStorage
• JSON data export/import
• GitHub Pages

There is:

• No JavaScript framework
• No external database
• No server-side application
• No installation requirement
• No account or login system

The entire operational application remains contained within a single HTML page.

## Deployment

The dashboard is deployed through GitHub Pages.

Live dashboard:

https://averydimbulb79.github.io/GPCH_kanban/

## Version History

### Version 5.6: Visual Cohesion

• Extended Kanban colour coding into the "+ Add" interface
• TO DO creation button now matches the blue TO DO column
• TO ORDER creation button now matches the amber TO ORDER column
• TO RECEIVE creation button now matches the green TO RECEIVE column
• GUEST NOTE creation button now matches the pink GUEST NOTES column
• HANDOVER creation button now matches the violet HANDOVER column
• Added subtle hover feedback to category-selection buttons
• Improved visual relationship between card creation and destination columns
• Improved overall interface cohesion

### Version 5.5: Data Portability

• Added Export Data
• Added Import Data
• Added portable JSON backups
• Added application version metadata
• Added export timestamps
• Added board and schedule record counts
• Added backup validation
• Added import confirmation
• Added automatic pre-import safety backup
• Added support for transferring operational data between computers

### Version 5.4: Schedule Management Fix

• Fixed scheduled-task deletion
• Improved delete-event handling
• Added deletion confirmation
• Deleted scheduled tasks now disappear correctly from the Schedule Manager
• Deleted scheduled tasks also disappear from Today's Scheduled Tasks

### Version 5.3: Receiving Workflow

• Added TO RECEIVE
• Expanded the Kanban from four to five operational columns
• Added direct TO ORDER → TO RECEIVE transfer
• Added receipt-status workflow
• Added Mark Received functionality
• Added distinct colour identities for all Kanban columns
• Improved card and column visual hierarchy

### Version 5.2: Header Controls

• Reorganised primary controls into a single header row
• Established + Add
• Established Manage Schedule
• Established Toggle Schedule
• Removed the separate floating schedule restoration button
• Prevented schedule controls from obstructing + Add

### Version 5.1: Rendering Reliability

• Rebuilt page rendering for improved reliability
• Kanban columns made immediately visible on page load
• Reduced dependency on dynamically generated structural elements
• Improved browser compatibility
• Added more defensive localStorage handling

### Version 5.0: Operational Redesign

• Major Crystal Club workflow redesign
• Replaced generic Kanban structure with purpose-specific operational columns
• Introduced TO DO
• Introduced TO ORDER
• Introduced GUEST NOTES
• Introduced HANDOVER
• Added specialised card forms
• Added search
• Added filtering
• Added drag-and-drop workflow
• Separated Today's Scheduled Tasks from the Kanban board

### Version 4.0: Floating Schedule

• Converted Today's Scheduled Tasks into a floating overlay
• Added approximately 80% opaque background
• Added hide/show functionality
• Removed scheduled tasks from the Kanban column structure

### Version 3.x: Scheduling Expansion

• Added recurring schedule management
• Added weekday scheduling
• Added first-days-of-month scheduling
• Added last-days-of-month scheduling
• Added specific monthly dates
• Added one-off dated tasks
• Removed Reset Demo to reduce accidental data loss
• Renamed the application GPCH Crystal Club

### Earlier Versions

Initial prototypes established:

• Single-page browser-based Kanban
• Operational cards
• Recurring scheduled tasks
• Daily schedule display
• Browser persistence
• Crystal Club-specific workflow concepts

## Current Architecture

GPCH Crystal Club remains a client-side application.

GitHub Pages distributes the application while operational data remains in browser localStorage.

This architecture provides:

• Fast loading
• Simple deployment
• No login requirement
• No server maintenance
• Local persistence
• Manual data portability
• Portable backups

It does not currently provide real-time multi-device synchronisation.

A shared backend or cloud database would be required if the application is later developed into a simultaneously shared live board across multiple Crystal Club workstations.

## Project Status

Active development.

The dashboard continues to be refined around practical GPCH Crystal Club operations, with emphasis on visibility, speed, intuitive workflows, shift communication, scheduling, data portability and minimal administrative friction.
