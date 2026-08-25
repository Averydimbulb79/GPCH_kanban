# GPCH Kanban

A single-page operational Kanban dashboard designed for GPCH Crystal Club.

The dashboard consolidates daily tasks, ordering, receiving, guest notes, shift handovers, archived records and recurring operational schedules into one lightweight browser-based workspace.

## Live Dashboard

https://averydimbulb79.github.io/GPCH_kanban/

Current version: 6.6

---

## Core Features

• Five colour-coded operational workflows  
• Matching colour-coded dashboard count boxes  
• Clickable count boxes and column headers  
• Full-window expanded column views  
• Archive visibility inside expanded views  
• Expanded-view search and sorting  
• Automatic urgency-based card sorting  
• Card creation timestamps  
• One-click card duplication  
• Complete, archive and permanent-delete workflow  
• Archived-card viewing and restoration  
• Drag-and-drop workflow  
• Streamlined ordering and receiving workflow  
• Contextual workflow actions  
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

• Dashboard count boxes  
• Kanban column headers  
• "+ Add" category buttons  
• Expanded column windows

This provides rapid visual recognition of each operational category.

---

# Dashboard Count Boxes

The top of the dashboard provides an immediate count of active cards in each operational category.

Example:

`15 TO DO`

`15 TO ORDER`

`15 TO RECEIVE`

`15 GUEST NOTES`

`15 HANDOVER`

Archived cards are excluded from these active counts.

Each count box uses the same colour as its corresponding workflow.

| Count Box | Colour |
| --- | --- |
| TO DO | Blue |
| TO ORDER | Amber |
| TO RECEIVE | Green |
| GUEST NOTES | Pink |
| HANDOVER | Violet |

## Quick Access

The count boxes also function as navigation controls.

Clicking a count box immediately opens the corresponding expanded workspace.

Both navigation methods perform the same action:

`Count Box → Expanded View`

`Column Header → Expanded View`

Count boxes include hover feedback and keyboard access using `Enter` or `Space`.

---

# Expanded Column View

The main Kanban provides a five-column overview of Crystal Club operations.

Because displaying five columns simultaneously can restrict usable card space on smaller laptop screens, each column can also be opened as a dedicated full-window workspace.

Expanded views can be opened by clicking either:

• The dashboard count box  
• The corresponding column header

Clickable column headers are identified by:

`TO DO ↗`

`TO ORDER ↗`

`TO RECEIVE ↗`

`GUEST NOTES ↗`

`HANDOVER ↗`

## Expanded Layout

Cards are displayed in a responsive grid rather than a single narrow vertical stack.

The number of cards across each row automatically adjusts according to available screen width.

This creates two complementary working modes:

`5-column board = operational overview`

`Expanded column = focused workspace`

The expanded window retains the colour identity of its corresponding workflow.

## Expanded View Controls

Each expanded window provides:

`Search this column`

`Sort by`

`+ Add Here`

`Show Archived / Hide Archived`

`× Close`

The window can also be closed by clicking outside it or pressing `Esc`.

All applicable card actions remain available from the expanded workspace.

---

# Expanded Archive View

Version 6.6 extends archive access directly into every expanded column window.

Staff no longer need to close an expanded section and return to the main board simply to inspect archived records.

Select:

`Show Archived`

to display archived cards belonging to the currently expanded section.

The button changes to:

`Hide Archived`

while archived records are visible.

For example, inside HANDOVER:

`Show Archived`

reveals archived HANDOVER records without displaying archived TO DO, TO ORDER, TO RECEIVE or GUEST NOTES cards.

This provides section-specific historical access while maintaining the focused expanded-column workflow.

## Archive State Inheritance

When an expanded window is opened, it inherits the archive visibility state of the main board.

If the main board is currently displaying archived cards, the expanded window opens with archived cards visible.

If the main board is displaying only active cards, the expanded window initially displays only active cards.

Archive visibility can then be independently changed within the expanded window.

---

# Expanded View Sorting

Expanded column windows contain dedicated sorting controls.

The compact five-column board continues to use automatic urgency sorting, while expanded views allow temporary alternative sorting without changing card data.

## Standard Sorting

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
• Copied  
• Edited  
• Moved  
• Restored  
• Imported  
• Searched  
• Filtered

This keeps operationally important matters near the top of each column.

---

# Card Creation Timestamps

Every newly created card automatically records its creation date and time.

Example:

`Created: 25 Aug 2026, 13:51`

Creation timestamps apply to:

• TO DO  
• TO ORDER  
• TO RECEIVE  
• GUEST NOTES  
• HANDOVER

The original timestamp remains attached when a card is edited, moved or archived.

Cards created before Version 5.7 may display:

`Created: Date unavailable`

because their original creation time was not previously recorded.

---

# Card Actions

The dashboard separates two types of card actions:

`Workflow actions`

and

`Card-management actions`

This distinction keeps cards compact while preserving direct one-click access to frequently used functions.

## Universal Card Actions

Active cards provide:

`Copy` · `Edit` · `Complete`

These controls remain grouped in the card footer.

## Workflow Actions

Actions that move an item through an operational process are positioned beside the information associated with that workflow.

This reduces visual clutter without hiding frequently used actions behind additional menus.

---

# Copy Card

Every card includes:

`Copy`

Selecting Copy opens a new-card form already populated with the selected card's information.

The original card remains unchanged.

The copied card is treated as a new record and receives:

• A new unique ID  
• A new creation timestamp  
• Active status  
• No inherited archive timestamp

Staff can modify any prefilled information before saving.

## Copying Archived Cards

Archived cards can also be copied.

The copied card becomes a new active record rather than another archived record.

This is useful when a previously completed task, order, guest requirement or handover matter occurs again.

---

# TO ORDER Workflow

TO ORDER cards represent items that still require procurement.

A typical card may display:

`Printer cartridge`

`Quantity: 1     Move to Receive →`

The workflow transition is positioned directly beside Quantity rather than in the card footer.

The footer remains:

`Copy` · `Edit` · `Complete`

Selecting:

`Move to Receive →`

moves the card from:

`TO ORDER → TO RECEIVE`

The card then enters the receiving workflow.

---

# TO RECEIVE Workflow

TO RECEIVE cards represent items that have already been ordered and are awaiting physical receipt.

A card may display:

`Quantity: 4 cartons     ✓ Mark Received`

The footer remains:

`Copy` · `Edit` · `Complete`

Selecting:

`✓ Mark Received`

uses the completion workflow so the received item can be archived rather than automatically discarded.

---

# Workflow Design Principle

Workflow transitions and general card management are deliberately separated.

Workflow-specific actions appear inside the relevant card information:

`TO ORDER → Move to Receive`

`TO RECEIVE → Mark Received`

Universal controls remain together:

`Copy · Edit · Complete`

This reduces footer congestion while avoiding additional menus and unnecessary clicks.

The design prioritises direct actions and minimal interaction steps.

---

# Complete and Archive Workflow

Active cards use:

`Complete`

rather than a direct Delete button.

Selecting Complete opens three choices:

`Archive`

`Delete Permanently`

`Cancel`

## Archive

Selecting Archive:

• Marks the card as completed  
• Records the archive date and time  
• Removes it from the normal active board  
• Preserves the card information  
• Preserves its original creation timestamp  
• Keeps it associated with its original operational column

## Delete Permanently

Selecting Delete Permanently removes the card from browser storage after an additional confirmation.

This action cannot be undone unless the record exists in an exported backup.

## Cancel

Cancel closes the completion window without changing the card.

---

# Archive Access

Archive records can be accessed at two levels.

## Main Board

The main toolbar includes:

`Show Archive`

Selecting it reveals archived cards across the board.

The control then changes to:

`Hide Archive`

## Expanded Column

Every expanded section also includes:

`Show Archived`

This displays archived records for that section directly inside its expanded workspace.

This means archived records can be inspected without leaving the operational context currently being viewed.

---

# Archived Card Appearance

Archived cards are visually subdued so they remain distinguishable from active work.

Archived cards display:

• ARCHIVED status  
• Original creation timestamp  
• Archive timestamp  
• Copy  
• Restore

Archived cards cannot be dragged between active workflow columns.

## Restore

Selecting:

`Restore`

returns an archived card to active status in its original column.

The card then re-enters normal urgency sorting.

## Active Counts

Archived cards are excluded from the five dashboard count boxes.

The dashboard counts therefore represent current active workload rather than historical records.

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

This separates outstanding procurement from outstanding delivery.

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

# Today's Scheduled Tasks

Recurring operational duties appear in a floating "Today's Scheduled Tasks" overlay at the top-right of the dashboard.

The overlay:

• Uses an approximately 80% opaque background  
• Floats above the Kanban without occupying a column  
• Automatically displays tasks applicable to the current date  
• Allows today's tasks to be marked complete  
• Can be hidden or restored using Toggle Schedule

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

Expanded column windows contain their own dedicated search field.

Search, sorting and archive visibility can therefore be used together within a focused section.

---

# Main Controls

The primary dashboard controls include:

`+ Add`

`Manage Schedule`

`Toggle Schedule`

`Show Archive / Hide Archive`

`Export Data`

`Import Data`

Expanded windows provide:

`Search`

`Sort`

`+ Add Here`

`Show Archived / Hide Archived`

`× Close`

---

# Data Storage

GPCH Crystal Club uses browser `localStorage`.

Stored information includes:

• Active cards  
• Archived cards  
• Creation timestamps  
• Archive timestamps  
• Scheduled tasks  
• Schedule completion information

Data remains available after:

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

Export Data creates a portable JSON backup containing:

• Active cards  
• Archived cards  
• Card creation timestamps  
• Archive timestamps  
• Scheduled tasks  
• Scheduled-task completion state  
• Application version  
• Export timestamp  
• Record counts

Backups are automatically timestamped.

Example:

`GPCH_Crystal_Club_Backup_2026-08-25_1351.json`

## Import Data

Import Data restores a previously exported GPCH Crystal Club backup.

Before importing, the application:

1. Validates the JSON file.
2. Confirms that it contains GPCH Crystal Club data.
3. Displays the number of cards and scheduled tasks.
4. Displays the backup version.
5. Requests confirmation before replacing existing data.

## Automatic Safety Backup

Before imported data replaces the existing browser dataset, the application automatically exports the current data.

This provides a recovery point if an incorrect or older backup is imported.

---

# Moving to Another Computer

## Old Computer

1. Open GPCH Crystal Club.
2. Select Export Data.
3. Save the generated JSON file.
4. Transfer the file to the new computer.

## New Computer

1. Open GPCH Crystal Club.
2. Select Import Data.
3. Choose the exported JSON file.
4. Review the backup information.
5. Confirm the import.

Active cards, archived records, timestamps and scheduled-task data will then be restored.

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

## v6.6 · Expanded Archive Access

• Added `Show Archived` directly to every expanded column window  
• Added `Hide Archived` state when archived records are visible  
• Archived records can now be reviewed without returning to the main board  
• Archive display is limited to the currently expanded operational section  
• Expanded windows inherit the main board's archive visibility when opened  
• Archive visibility can subsequently be controlled independently within the expanded window  
• Retained search and sorting while archived cards are displayed  
• Reduced navigation steps when reviewing historical operational records

## v6.5 · Streamlined Card Actions

• Reorganised card controls to reduce visual clutter  
• Separated workflow actions from universal card-management actions  
• Moved Move to Receive from the TO ORDER footer to the Quantity row  
• Added compact `Move to Receive →` beside order quantity  
• Moved Mark Received from the TO RECEIVE footer to the Quantity row  
• Added compact `✓ Mark Received` beside receiving quantity  
• Retained direct one-click workflow transitions  
• Standardised active card footer around `Copy · Edit · Complete`  
• Reduced button congestion on narrow cards  
• Avoided secondary menus so common actions remain immediately accessible

## v6.4 · Card Duplication

• Added Copy to every card  
• Copy opens a new-card form prefilled with the source card's details  
• Copied cards receive a new unique ID  
• Copied cards receive a new creation timestamp  
• Original cards remain unchanged  
• Archive state is not inherited by copied cards  
• Archived cards can be copied into new active cards  
• Reduced repetitive data entry for similar operational records

## v6.3 · Dashboard Quick Access

• Made all five dashboard count boxes clickable  
• Each count opens its corresponding expanded workspace  
• Added hover feedback  
• Added keyboard access using Enter and Space  
• Count boxes and column headers now provide equivalent navigation

## v6.2 · Complete and Archive Workflow

• Replaced direct card deletion with Complete  
• Added Archive, Delete Permanently and Cancel choices  
• Added archive timestamps  
• Added Show Archive / Hide Archive  
• Added archive-mode notification  
• Added subdued archived-card styling  
• Added ARCHIVED status indicator  
• Added Restore functionality  
• Archived cards remain associated with their original columns  
• Archived cards are excluded from active dashboard counts  
• Archived cards cannot be dragged between active columns  
• Mark Received integrated with the completion workflow

## v6.1 · Dashboard Colour Integration

• Colour-coded the five dashboard count boxes  
• TO DO matches the blue workflow  
• TO ORDER matches the amber workflow  
• TO RECEIVE matches the green workflow  
• GUEST NOTES matches the pink workflow  
• HANDOVER matches the violet workflow  
• Matched summary backgrounds, borders and text colours

## v6.0 · Expanded View Sorting

• Added Sort by controls to expanded column windows  
• Retained Urgency: High → Low as default  
• Added Urgency: Low → High  
• Added Newest First and Oldest First  
• Added Title A → Z and Z → A  
• Added TO DO due-time sorting  
• Added TO ORDER and TO RECEIVE status sorting  
• Added GUEST NOTES arrival, departure and room sorting  
• Added HANDOVER follow-up-time sorting

## v5.9 · Expanded Column View

• Made all five column headers clickable  
• Added full-window expanded column workspaces  
• Added responsive multi-card grid layouts  
• Added dedicated expanded-column search  
• Added "+ Add Here"  
• Retained card actions inside expanded views  
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
• Added Date unavailable handling for legacy cards

## v5.6 · Visual Cohesion

• Colour-coded "+ Add" category buttons  
• Matched creation buttons with destination columns  
• Blue TO DO  
• Amber TO ORDER  
• Green TO RECEIVE  
• Pink GUEST NOTE  
• Violet HANDOVER  
• Added subtle hover feedback

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
• Archived operational history  
• Section-specific archive access  
• One-click card duplication  
• Direct workflow controls  
• Easy migration between computers  
• Works as a static GitHub Pages application

## Current Limitation

The dashboard does not provide real-time synchronisation between multiple computers.

A shared backend or cloud database would be required if the project is later expanded into a simultaneously shared operational board across multiple Crystal Club workstations.

---

# Project Status

Active development.

The dashboard continues to evolve around practical GPCH Crystal Club operations, with emphasis on visibility, priority management, minimal-click workflows, efficient use of limited screen space, operational history, shift communication, recurring task management, data portability and traceability.
