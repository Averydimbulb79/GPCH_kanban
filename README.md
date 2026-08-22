# GPCH Kanban

A single-page operational Kanban dashboard designed for GPCH Crystal Club.

The dashboard consolidates daily tasks, ordering, receiving, guest notes, shift handovers and recurring operational schedules into one lightweight browser-based workspace.

## Live Dashboard

https://averydimbulb79.github.io/GPCH_kanban/

Current version: 6.1

---

## Core Features

• Five colour-coded operational workflows  
• Matching colour-coded dashboard summary cards  
• Automatic urgency-based card sorting  
• Full-window expanded column views  
• Expanded-view search and sorting controls  
• Card creation timestamps  
• Drag-and-drop workflow  
• Ordering and receiving workflow  
• Recurring scheduled tasks  
• Weekly and monthly scheduling rules  
• Floating Today's Scheduled Tasks overlay  
• Board-wide search and filtering  
• JSON data export and import  
• Automatic pre-import safety backups  
• Persistent browser storage  
• Single-page static architecture

---

# Board Structure

The dashboard uses five operational columns with a consistent colour identity.

| Column | Colour | Purpose |
| --- | --- | --- |
| TO DO | Blue | General tasks, duties and follow-ups |
| TO ORDER | Amber | Items requiring ordering or replenishment |
| TO RECEIVE | Green | Ordered items awaiting delivery or collection |
| GUEST NOTES | Pink | Guest preferences, requests and service information |
| HANDOVER | Violet | Outstanding matters requiring communication between shifts |

The colour system is used consistently across:

• Dashboard summary cards  
• Kanban column headers  
• "+ Add" category buttons  
• Expanded column windows

This allows each operational category to be recognised quickly throughout the interface.

---

# Dashboard Summary

The top of the dashboard provides an immediate count of active cards in each operational category.

For example:

`15 TO DO`

`15 TO ORDER`

`15 TO RECEIVE`

`15 GUEST NOTES`

`15 HANDOVER`

From Version 6.1, these summary cards use the same colour identity as their corresponding Kanban columns.

| Summary | Colour |
| --- | --- |
| TO DO | Blue |
| TO ORDER | Amber |
| TO RECEIVE | Green |
| GUEST NOTES | Pink |
| HANDOVER | Violet |

The matching backgrounds, borders and text colours create a consistent visual relationship between the dashboard summary and the working board.

---

# Expanded Column View

The main Kanban provides a five-column overview of Crystal Club operations.

Because five simultaneous columns can restrict usable card space on smaller laptop screens, each column can also be opened as a dedicated full-window workspace.

Click any column header:

`TO DO ↗`

`TO ORDER ↗`

`TO RECEIVE ↗`

`GUEST NOTES ↗`

`HANDOVER ↗`

The selected column opens in a large expanded window.

## Expanded Layout

Cards are displayed in a responsive grid rather than a single narrow vertical stack.

The number of cards displayed across each row automatically adjusts according to available screen width.

This provides two complementary working modes:

`5-column board = operational overview`

`Expanded column = focused workspace`

The expanded window retains the colour identity of its corresponding Kanban column.

## Expanded View Controls

Each expanded window provides:

• Search this column  
• Sort by  
• + Add Here  
• × Close

The window can also be closed by clicking outside it or pressing `Esc`.

## Card Actions

Cards remain fully operational inside the expanded view.

Depending on card type, available actions include:

• Edit  
• Delete  
• Move to Receive  
• Mark Received

Changes made in the expanded window immediately update the main Kanban because both views use the same underlying dataset.

---

# Expanded View Sorting

Expanded column windows include dedicated sorting controls.

The compact five-column Kanban continues to use automatic urgency sorting, while expanded views allow temporary alternative sorting without modifying card data.

## Standard Sorting Options

All expanded columns support:

• Urgency: High → Low  
• Urgency: Low → High  
• Newest First  
• Oldest First  
• Title: A → Z  
• Title: Z → A

Default:

`Urgency: High → Low`

## TO DO

Additional sorting:

• Due Time: Earliest First  
• Due Time: Latest First

## TO ORDER

Additional sorting:

• Status: A → Z

## TO RECEIVE

Additional sorting:

• Status: A → Z

## GUEST NOTES

Additional sorting:

• Arrival Date: Earliest First  
• Departure Date: Earliest First  
• Room Number: Low → High

## HANDOVER

Additional sorting:

• Follow-up Time: Earliest First

---

# Automatic Urgency Sorting

Cards on the main board are automatically arranged by descending urgency.

The general hierarchy is:

`URGENT → IMPORTANT → ATTENTION → ROUTINE / NORMAL`

Different card types may use different priority terminology. The dashboard maps these values into a common urgency hierarchy.

Cards with equal urgency are sorted newest first.

Sorting is automatically reapplied when cards are:

• Created  
• Edited  
• Moved  
• Imported  
• Searched  
• Filtered

This keeps operationally important matters near the top of each column.

---

# Card Creation Timestamps

Every newly created card automatically records its creation date and time.

Example:

`Created: 23 Aug 2026, 14:11`

Timestamps apply to:

• TO DO  
• TO ORDER  
• TO RECEIVE  
• GUEST NOTES  
• HANDOVER

The original timestamp remains attached when a card is edited or moved.

Cards created before Version 5.7 may display:

`Created: Date unavailable`

because their original creation time was not previously recorded.

---

# Card Types

## TO DO

For general operational work such as:

• Operational tasks  
• Follow-ups  
• Administrative work  
• Equipment issues  
• Time-sensitive duties

Cards can include priority, due time, assignment and notes.

## TO ORDER

For items requiring procurement or replenishment.

Cards can include:

• Item  
• Quantity  
• Urgency  
• Order status  
• Supplier or department  
• Notes

## TO RECEIVE

For items already ordered but awaiting delivery or collection.

This separates procurement requests from outstanding deliveries.

## GUEST NOTES

For guest-related operational information such as:

• Guest preferences  
• Special requests  
• Room information  
• Arrival details  
• Departure details  
• Service requirements  
• Follow-up information

## HANDOVER

For matters requiring continuity between shifts.

Cards can include:

• Handover subject  
• Room or area  
• Originating shift or colleague  
• Receiving shift  
• Priority  
• Follow-up time  
• Details

---

# Ordering Workflow

The procurement workflow follows:

`TO ORDER → TO RECEIVE → RECEIVED`

A TO ORDER card includes:

`Move to Receive`

Once an order has been placed, the card moves into TO RECEIVE.

When the physical item arrives, it can be marked as received and removed from the active board.

This distinguishes:

`Still needs to be ordered`

from:

`Already ordered and awaiting arrival`

---

# Today's Scheduled Tasks

Recurring operational duties appear in a floating "Today's Scheduled Tasks" overlay at the top-right of the dashboard.

The overlay:

• Uses an approximately 80% opaque background  
• Floats above the Kanban without occupying a column  
• Automatically displays tasks applicable to the current date  
• Allows today's tasks to be marked complete  
• Can be hidden or restored using "Toggle Schedule"

Completing today's occurrence does not delete the recurring schedule.

The task appears again on its next applicable date.

---

# Schedule Manager

Select:

`Manage Schedule`

The Schedule Manager provides an interface for creating, editing and deleting recurring operational duties.

Each scheduled task can include:

• Task name  
• Time  
• Category  
• Recurrence rule

## Supported Scheduling Rules

| Schedule | Function |
| --- | --- |
| Weekly | Selected weekdays |
| First N Days | First specified number of days each month |
| Last N Days | Final specified number of days each month |
| Monthly Day | Specific calendar day every month |
| One-Off | One specific date |

This supports routine weekly duties as well as month-start, month-end and date-specific operational requirements.

---

# Search and Filtering

The main dashboard includes universal search and column filtering.

Search can locate information such as:

• Tasks  
• Items  
• Room numbers  
• Guest names  
• Notes  
• Suppliers  
• Departments  
• Handover information

The board can be filtered by:

• All Columns  
• To Do  
• To Order  
• To Receive  
• Guest Notes  
• Handover

Expanded column windows also contain their own dedicated search field.

---

# Main Controls

The primary dashboard controls are grouped together:

`+ Add` · `Manage Schedule` · `Toggle Schedule` · `Export Data` · `Import Data`

---

# Data Storage

GPCH Crystal Club uses browser `localStorage`.

Cards, timestamps, schedules and operational information remain available after:

• Refreshing the page  
• Closing the browser  
• Restarting the computer  
• Reopening the dashboard

No external database or login is required.

## Important

Operational data belongs to the individual browser and computer.

GitHub Pages hosts the application itself but does not store the Kanban dataset.

Data entered on one computer therefore does not automatically synchronise with another computer.

---

# Export and Import

## Export Data

"Export Data" creates a portable JSON backup containing:

• Kanban cards  
• Card creation timestamps  
• Scheduled tasks  
• Scheduled-task completion state  
• Application version  
• Export timestamp  
• Record counts

Backups are automatically timestamped.

Example:

`GPCH_Crystal_Club_Backup_2026-08-23_1411.json`

## Import Data

"Import Data" restores a previously exported GPCH Crystal Club backup.

Before importing, the application:

1. Validates the JSON file.
2. Confirms that it contains GPCH Crystal Club data.
3. Displays the number of cards and scheduled tasks.
4. Displays the backup version.
5. Requests confirmation before replacing existing data.

Imported cards are automatically displayed according to the current sorting rules.

## Automatic Safety Backup

Before an import replaces existing browser data, the application automatically exports the current dataset.

Example:

`GPCH_Crystal_Club_PreImport_Backup_2026-08-23_1411.json`

This provides a recovery point if an incorrect or older backup is imported.

---

# Moving to Another Computer

## Old Computer

1. Open GPCH Crystal Club.
2. Select "Export Data".
3. Save the generated JSON file.
4. Transfer the file to the new computer.

## New Computer

1. Open GPCH Crystal Club.
2. Select "Import Data".
3. Choose the exported JSON file.
4. Review the backup information.
5. Confirm the import.

Cards, timestamps and scheduled-task data will then be restored in the new browser.

---

# Technology

The application uses a deliberately lightweight architecture:

• HTML  
• CSS  
• Vanilla JavaScript  
• Browser localStorage  
• JSON backup and restore  
• GitHub Pages

There is no JavaScript framework, external database, server-side application or installation requirement.

The entire operational application is contained within a single HTML page.

---

# Version History

## v6.1 · Dashboard Colour Integration

• Colour-coded the five dashboard summary cards  
• TO DO summary now matches the blue TO DO workflow  
• TO ORDER summary now matches the amber TO ORDER workflow  
• TO RECEIVE summary now matches the green TO RECEIVE workflow  
• GUEST NOTES summary now matches the pink GUEST NOTES workflow  
• HANDOVER summary now matches the violet HANDOVER workflow  
• Matched summary backgrounds, borders and text colours  
• Extended the established colour system across the complete dashboard  
• Improved rapid visual recognition of operational categories

## v6.0 · Expanded View Sorting

• Added Sort by controls to expanded column windows  
• Retained Urgency: High → Low as the default  
• Added Urgency: Low → High  
• Added Newest First and Oldest First  
• Added Title A → Z and Z → A  
• Added TO DO due-time sorting  
• Added TO ORDER and TO RECEIVE status sorting  
• Added GUEST NOTES arrival, departure and room sorting  
• Added HANDOVER follow-up-time sorting  
• Sorting affects only the expanded view and does not modify card data

## v5.9 · Expanded Column View

• Made all five column headers clickable  
• Added full-window expanded column workspaces  
• Added responsive multi-card grid layouts  
• Added dedicated expanded-column search  
• Added "+ Add Here"  
• Retained card actions inside expanded views  
• Retained urgency-based ordering  
• Added column-specific colour themes  
• Added × Close, click-outside and Esc closing  
• Improved usability on smaller laptop screens

## v5.8 · Priority Sorting

• Added automatic urgency-based sorting  
• Cards are ordered from highest to lowest urgency  
• Introduced a common ranking system across card types  
• Cards with equal urgency are sorted newest first  
• Sorting refreshes after creation, editing and movement  
• Sorting applies to imported data, search and filtering

## v5.7 · Card Creation Timestamps

• Added automatic creation date and time to every new card  
• Applied timestamps across all five categories  
• Preserved original timestamps during editing and movement  
• Included timestamps in exported backups  
• Added "Date unavailable" handling for legacy cards  
• Introduced a simple operational audit trail

## v5.6 · Visual Cohesion

• Colour-coded "+ Add" category buttons  
• Matched creation buttons with destination columns  
• Blue TO DO  
• Amber TO ORDER  
• Green TO RECEIVE  
• Pink GUEST NOTE  
• Violet HANDOVER  
• Added subtle hover feedback  
• Improved interface consistency

## v5.5 · Data Portability

• Added Export Data and Import Data  
• Added portable JSON backups  
• Added version and timestamp metadata  
• Added record counts and backup validation  
• Added import confirmation  
• Added automatic pre-import safety backup  
• Enabled migration between computers

## v5.4 · Schedule Management Fix

• Fixed scheduled-task deletion  
• Improved deletion event handling  
• Added deletion confirmation  
• Deleted schedules now disappear correctly from both schedule interfaces

## v5.3 · Receiving Workflow

• Added TO RECEIVE  
• Expanded the Kanban to five operational columns  
• Added TO ORDER → TO RECEIVE transfer  
• Added receipt-status workflow  
• Added Mark Received  
• Introduced distinct column colours

## v5.2 · Header Controls

• Consolidated primary controls into one header row  
• Added Toggle Schedule to the main controls  
• Removed the separate floating schedule restoration button  
• Prevented schedule controls from obstructing "+ Add"

## v5.1 · Rendering Reliability

• Rebuilt page rendering for improved reliability  
• Made Kanban columns immediately visible on page load  
• Improved browser compatibility  
• Strengthened localStorage handling

## v5.0 · Operational Redesign

• Rebuilt the dashboard around Crystal Club operations  
• Introduced TO DO, TO ORDER, GUEST NOTES and HANDOVER  
• Added specialised card forms  
• Added search and filtering  
• Added drag-and-drop workflow  
• Separated Today's Scheduled Tasks from the Kanban

## v4.0 · Floating Schedule

• Converted Today's Scheduled Tasks into a floating overlay  
• Added approximately 80% opaque background  
• Added hide and restore functionality  
• Removed the schedule from the Kanban column structure

## v3.x · Scheduling Expansion

• Added recurring schedule management  
• Added weekday scheduling  
• Added first and last days of month rules  
• Added specific monthly dates  
• Added one-off dated tasks  
• Removed Reset Demo to reduce accidental data loss  
• Renamed the application GPCH Crystal Club

---

# Current Architecture

GPCH Crystal Club remains a client-side application.

GitHub Pages distributes the application while operational data remains in browser localStorage.

## Advantages

• Fast loading  
• Simple deployment  
• No login required  
• No server maintenance  
• Local persistence  
• Portable backups  
• Easy migration between computers  
• Works as a static GitHub Pages application

## Current Limitation

The dashboard does not provide real-time synchronisation between multiple computers.

A shared backend or cloud database would be required if the project is later expanded into a simultaneously shared operational board across multiple Crystal Club workstations.

---

# Project Status

Active development.

The dashboard continues to evolve around practical GPCH Crystal Club operations, with emphasis on visibility, priority management, efficient use of limited screen space, intuitive workflows, shift communication, recurring task management, data portability and operational traceability.
