# GPCH Kanban

Single-page operational Kanban dashboard designed for GPCH Crystal Club.

GPCH Kanban consolidates daily tasks, ordering, receiving, guest notes, shift handovers, leave requests, archived records and recurring operational schedules into one lightweight browser-based workspace.

## Live Dashboard

https://averydimbulb79.github.io/GPCH_kanban/

Current version: 6.8

---

# Overview

The dashboard is designed around a simple operational principle:

`See what needs attention → Act directly → Record completion → Preserve useful history`

The main board contains five colour-coded operational workflows:

| Workspace | Purpose |
| --- | --- |
| TO DO | General tasks, duties and follow-ups |
| TO ORDER | Items requiring ordering or replenishment |
| TO RECEIVE | Ordered items awaiting delivery or collection |
| GUEST NOTES | Guest preferences, requests and service information |
| HANDOVER | Matters requiring continuity between shifts |

LEAVE REQUESTS operates as an additional dedicated workspace but does not occupy permanent space on the main Kanban.

This keeps the daily board focused while allowing leave administration to follow the same familiar card-based interaction model.

---

# Core Features

• Five colour-coded main Kanban workflows  
• Dedicated Leave Requests workspace  
• Matching colour-coded dashboard count boxes  
• Clickable count boxes and column headers  
• Full-window workspace views  
• Consistent add-card workflow across workspaces  
• Workspace-specific search and sorting  
• Archive visibility within expanded workspaces  
• Automatic urgency-based card sorting  
• Card creation timestamps  
• One-click card duplication  
• Complete and archive workflow  
• Archived-card restoration  
• Drag-and-drop Kanban workflow  
• Streamlined ordering and receiving process  
• Contextual one-click workflow actions  
• Recurring scheduled tasks  
• Weekly and monthly scheduling rules  
• Floating Today's Scheduled Tasks overlay  
• Board-wide search and filtering  
• Centralised Settings menu  
• JSON data export and import  
• Automatic pre-import safety backups  
• Persistent browser storage  
• Single-page static architecture

---

# Main Dashboard

The main dashboard provides an overview of current Crystal Club operations.

Five count boxes show the number of active cards in:

`TO DO`

`TO ORDER`

`TO RECEIVE`

`GUEST NOTES`

`HANDOVER`

Archived cards are excluded from active counts.

Each count box matches the colour of its corresponding column.

The count boxes are also navigation controls.

Clicking either:

`Dashboard Count Box`

or:

`Column Header`

opens the corresponding full-window workspace.

Keyboard access using `Enter` and `Space` is also supported on the count boxes.

---

# Main Controls

The primary controls have been streamlined around frequently used daily functions:

`+ Add`

`Leave Request`

`Toggle Schedule`

`Show Archive / Hide Archive`

`Settings`

Administrative and data-management functions are deliberately separated from everyday operational controls.

---

# Settings

Version 6.7 introduced a central Settings menu to reduce header clutter.

Selecting:

`Settings`

opens access to:

`Manage Schedule`

`Export Data`

`Import Data`

This separates configuration and data-management functions from everyday operational actions.

---

# Full-Window Workspaces

The five Kanban columns can each be opened as dedicated full-window workspaces.

This is particularly useful on smaller laptop screens where displaying five columns simultaneously limits available card width.

The workspaces are:

`TO DO`

`TO ORDER`

`TO RECEIVE`

`GUEST NOTES`

`HANDOVER`

Version 6.8 extends the same interaction model to:

`LEAVE REQUESTS`

The design therefore provides two complementary operating modes:

`Main Kanban = operational overview`

`Full-window workspace = focused work`

---

# Consistent Workspace Interface

The expanded operational workspaces use a common interface.

Typical controls include:

`Search`

`Sort`

`+ Add Here`

`Show Archived / Hide Archived`

`× Close`

This consistency is intentional.

Users should not have to learn a different interaction pattern for each type of operational information.

The general workflow is:

`Open workspace → Review cards → Add or act on card → Save → Continue`

---

# Leave Requests

Version 6.8 redesigns Leave Requests as a full operational workspace.

Leave Requests no longer opens as a conventional administrative popup containing both the form and records.

Instead:

`Leave Request → Full-window Leave Requests workspace`

This matches the behaviour of the existing Kanban column workspaces.

Importantly, Leave Requests does not become a sixth permanent column on the main dashboard.

This avoids further reducing horizontal screen space.

---

# Leave Requests Workspace

Selecting:

`Leave Request`

opens:

`LEAVE REQUESTS`

as a full-window card workspace.

The toolbar provides:

`Search leave requests`

`Sort`

`+ Add Here`

`Show Archived / Hide Archived`

`× Close`

Leave request cards are displayed using the same responsive grid principle as cards in the other expanded workspaces.

---

# Adding Leave Requests

Select:

`+ Add Here`

inside the Leave Requests workspace.

A card-entry form opens using the same interaction pattern as other Kanban card forms.

A leave request can contain:

• Staff Name  
• Leave Type  
• Start Date  
• End Date  
• Status  
• Notes

Available leave types include:

• Annual Leave  
• Off in Lieu  
• Medical Leave  
• Childcare Leave  
• Unpaid Leave  
• Other

Available statuses include:

• Pending  
• Approved  
• Declined

Every newly created leave request receives its own creation timestamp.

---

# Leave Request Cards

Leave requests are stored as cards rather than rows in a separate administrative table.

Cards can display:

• Staff name  
• Leave type  
• Start date  
• End date  
• Approval status  
• Notes  
• Creation timestamp  
• Archive information where applicable

Card actions include:

`Copy`

`Edit`

`Complete`

Archived leave cards provide:

`Copy`

`Restore`

---

# Leave Request Sorting

The Leave Requests workspace supports dedicated sorting options:

• Start Date: Earliest First  
• Start Date: Latest First  
• Newest First  
• Oldest First  
• Staff Name: A → Z  
• Staff Name: Z → A  
• Status: A → Z

The default view prioritises upcoming leave chronologically.

---

# Leave Request Search

The Leave Requests workspace includes its own search field.

Search can locate matching information contained within leave request records, allowing staff to quickly locate requests by information such as:

• Staff name  
• Leave type  
• Status  
• Dates  
• Notes

---

# Leave Request Archive

Completed leave requests do not need to remain visible during normal operations.

Select:

`Complete`

to archive a leave request.

Archived requests are hidden from the normal Leave Requests workspace.

Select:

`Show Archived`

to display them.

The control then changes to:

`Hide Archived`

Archived leave requests can be restored to active status when necessary.

---

# Leave Request Duplication

Leave request cards support:

`Copy`

Copying creates a new request based on an existing card.

The copied request receives:

• A new unique ID  
• A new creation timestamp  
• Active status  
• No inherited archive timestamp

The prefilled information can be changed before saving.

This is useful when similar leave arrangements need to be entered without repeatedly retyping common information.

---

# Board Structure

The main board uses five permanent columns.

## TO DO

For:

• Operational tasks  
• Follow-ups  
• Administrative duties  
• Equipment matters  
• Time-sensitive work

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

For items already ordered but awaiting physical delivery or collection.

This distinguishes:

`Needs ordering`

from:

`Already ordered and awaiting receipt`

## GUEST NOTES

For guest-related operational information such as:

• Preferences  
• Special requests  
• Room information  
• Arrival details  
• Departure details  
• Service requirements  
• Follow-up matters

## HANDOVER

For matters requiring continuity between shifts.

Cards can include:

• Handover subject  
• Room or area  
• Originating staff or shift  
• Receiving shift  
• Priority  
• Follow-up time  
• Details

---

# Card Actions

Active Kanban cards use three common management controls:

`Copy`

`Edit`

`Complete`

Workflow-specific actions are positioned separately where appropriate.

This prevents narrow cards from becoming overloaded with buttons while keeping common actions one click away.

---

# Copy Card

Selecting:

`Copy`

opens a new-card form prefilled with the selected card's information.

The copied card is a new record.

It receives:

• A new unique ID  
• A new creation timestamp  
• Active status  
• No inherited archive timestamp

The original card remains unchanged.

Archived cards can also be copied into new active records.

---

# TO ORDER Workflow

TO ORDER cards place the primary workflow action directly beside Quantity.

Example:

`Quantity: 1     Move to Receive →`

Selecting:

`Move to Receive →`

moves the card from:

`TO ORDER → TO RECEIVE`

The footer remains focused on universal card controls:

`Copy · Edit · Complete`

---

# TO RECEIVE Workflow

TO RECEIVE cards use the same contextual design.

Example:

`Quantity: 4     ✓ Mark Received`

Selecting:

`✓ Mark Received`

moves the item into the completion workflow.

The footer remains:

`Copy · Edit · Complete`

---

# Workflow Design Principle

Workflow transitions are kept close to the information they affect.

General card-management actions remain grouped separately.

Therefore:

`TO ORDER → Move to Receive`

`TO RECEIVE → Mark Received`

while:

`Copy · Edit · Complete`

remain universal card-management actions.

This keeps actions immediately accessible without introducing additional menus or unnecessary clicks.

---

# Complete and Archive Workflow

Active Kanban cards use:

`Complete`

instead of direct deletion.

Selecting Complete provides:

`Archive`

`Delete Permanently`

`Cancel`

## Archive

Archive:

• Records completion  
• Stores an archive timestamp  
• Removes the card from normal active views  
• Preserves the original information  
• Preserves the original creation timestamp  
• Keeps the card associated with its original workspace

## Delete Permanently

Delete Permanently removes the card from browser storage after confirmation.

Recovery is only possible if the data exists in a previous backup.

## Restore

Archived cards can be returned to active status using:

`Restore`

---

# Archive Access

Archive visibility is available at both board and workspace level.

## Main Board

Use:

`Show Archive / Hide Archive`

to control archived cards across the main Kanban.

## Expanded Workspaces

Each expanded Kanban workspace includes:

`Show Archived / Hide Archived`

This allows historical records to be reviewed without leaving the current workspace.

For example, archived HANDOVER cards can be reviewed directly inside HANDOVER without displaying archived records from unrelated sections.

## Leave Requests

Leave Requests provides its own:

`Show Archived / Hide Archived`

control.

---

# Automatic Urgency Sorting

The main Kanban automatically orders cards by operational urgency.

General hierarchy:

`URGENT → IMPORTANT → ATTENTION → ROUTINE / NORMAL`

Different card types may use different terminology, which is mapped into a common urgency hierarchy.

Cards with equal urgency are generally sorted newest first.

Automatic sorting is reapplied when cards are:

• Created  
• Copied  
• Edited  
• Moved  
• Restored  
• Imported  
• Searched  
• Filtered

---

# Expanded Workspace Sorting

All five expanded Kanban workspaces support:

• Urgency: High → Low  
• Urgency: Low → High  
• Newest First  
• Oldest First  
• Title: A → Z  
• Title: Z → A

Additional workspace-specific sorting is available.

## TO DO

• Due Time: Earliest First  
• Due Time: Latest First

## TO ORDER

• Status: A → Z

## TO RECEIVE

• Status: A → Z

## GUEST NOTES

• Arrival Date: Earliest First  
• Departure Date: Earliest First  
• Room Number: Low → High

## HANDOVER

• Follow-up Time: Earliest First

---

# Card Creation Timestamps

Every newly created card automatically records its creation date and time.

Example:

`Created: 28 Aug 2026, 06:47`

Creation timestamps apply to:

• TO DO  
• TO ORDER  
• TO RECEIVE  
• GUEST NOTES  
• HANDOVER  
• LEAVE REQUESTS

The original timestamp remains attached when a card is edited, moved or archived.

Legacy cards created before timestamp support may display:

`Created: Date unavailable`

---

# Today's Scheduled Tasks

Recurring operational duties appear in a floating:

`Today's Scheduled Tasks`

overlay at the top-right of the dashboard.

The overlay:

• Floats above the Kanban  
• Uses an approximately 80% opaque background  
• Automatically displays tasks applicable to the current date  
• Allows today's occurrence to be completed  
• Can be hidden or restored using Toggle Schedule

Completing today's occurrence does not delete the recurring schedule.

The task returns on its next applicable date.

---

# Schedule Manager

Schedule management is accessed through:

`Settings → Manage Schedule`

The Schedule Manager supports recurring operational duties.

Each scheduled task can include:

• Task name  
• Time  
• Category  
• Recurrence rule

Supported scheduling rules include:

| Schedule | Function |
| --- | --- |
| Weekly | Selected weekdays |
| First N Days | First specified number of days each month |
| Last N Days | Final specified number of days each month |
| Monthly Day | Specific calendar day each month |
| One-Off | One specific date |

This supports weekly routines, month-start procedures, month-end procedures and date-specific duties.

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

The main board can be filtered by:

• All Columns  
• To Do  
• To Order  
• To Receive  
• Guest Notes  
• Handover

Expanded workspaces provide their own focused search fields.

Leave Requests also provides dedicated search.

---

# Data Storage

GPCH Crystal Club uses browser `localStorage`.

Stored information includes:

• Active Kanban cards  
• Archived Kanban cards  
• Card creation timestamps  
• Archive timestamps  
• Leave request cards  
• Archived leave requests  
• Scheduled tasks  
• Schedule completion information

Data remains available after:

• Refreshing the page  
• Closing the browser  
• Restarting the computer  
• Reopening the dashboard

No external database or login is required.

---

# Export and Import

Data-management controls are located under:

`Settings`

## Export Data

Export Data creates a portable JSON backup containing operational data including:

• Active cards  
• Archived cards  
• Creation timestamps  
• Archive timestamps  
• Leave requests  
• Archived leave requests  
• Scheduled tasks  
• Scheduled-task completion state  
• Application version  
• Export timestamp  
• Record counts

## Import Data

Import Data restores a previously exported GPCH Crystal Club backup.

The application validates the backup before replacing current data.

## Leave Request Portability

Leave Request data is included in Version 6.7 and later backups.

Older valid GPCH backups that do not contain Leave Request data remain supported.

---

# Automatic Safety Backup

Before imported data replaces the current browser dataset, GPCH Crystal Club automatically exports the existing data.

This provides a recovery point if an incorrect or outdated backup is imported.

---

# Moving to Another Computer

On the existing computer:

1. Open GPCH Crystal Club.
2. Select Settings.
3. Select Export Data.
4. Save the JSON backup.
5. Transfer it to the new computer.

On the new computer:

1. Open GPCH Crystal Club.
2. Select Settings.
3. Select Import Data.
4. Choose the exported JSON file.
5. Review the backup information.
6. Confirm the import.

The operational dataset is then restored.

---

# Technology

GPCH Kanban deliberately uses a lightweight architecture:

• HTML  
• CSS  
• Vanilla JavaScript  
• Browser localStorage  
• JSON backup and restore  
• GitHub Pages

There is no JavaScript framework, external database, server-side application or installation requirement.

The application remains contained within a single HTML page.

---

# Version History

## v6.8 · Unified Leave Request Workspace

• Redesigned Leave Requests to use the same full-window interaction pattern as expanded Kanban columns  
• Removed the previous combined leave-entry and card-list popup workflow  
• Added dedicated LEAVE REQUESTS full-window workspace  
• Added responsive leave-request card grid  
• Added Search Leave Requests control  
• Added dedicated leave-request sorting  
• Added `+ Add Here`  
• Added `Show Archived / Hide Archived`  
• Added `× Close`  
• Standardised leave request creation around the same card-entry modal pattern used elsewhere  
• Added Staff Name, Leave Type, Start Date, End Date, Status and Notes fields  
• Added leave-request creation timestamps  
• Retained Copy, Edit, Complete and Restore actions  
• Retained archived leave-request support  
• Leave Requests remains outside the five-column main Kanban to preserve horizontal screen space  
• Improved UX consistency by making workspace navigation and card creation behaviour predictable across the application

## v6.7 · Settings and Leave Requests

• Added dedicated Leave Request functionality  
• Added persistent Leave Request storage  
• Added Leave Request data to export/import backups  
• Added backward compatibility for backups created before Leave Requests  
• Added Settings button  
• Moved Manage Schedule under Settings  
• Moved Export Data under Settings  
• Moved Import Data under Settings  
• Reduced main-header control clutter  
• Separated administrative controls from daily operational controls

## v6.6 · Expanded Archive Access

• Added Show Archived directly to every expanded Kanban workspace  
• Added Hide Archived state  
• Archived records can be reviewed without returning to the main board  
• Archive display remains limited to the current workspace  
• Expanded workspaces inherit main-board archive visibility when opened  
• Archive visibility can subsequently be controlled within the expanded workspace  
• Retained search and sorting while archived records are displayed

## v6.5 · Streamlined Card Actions

• Separated workflow actions from universal card-management actions  
• Moved Move to Receive beside TO ORDER Quantity  
• Moved Mark Received beside TO RECEIVE Quantity  
• Retained direct one-click workflow transitions  
• Standardised active card footer around Copy, Edit and Complete  
• Reduced button congestion on narrow cards  
• Avoided secondary action menus

## v6.4 · Card Duplication

• Added Copy to cards  
• Copy opens a new-card form prefilled with source-card information  
• Copied cards receive new unique IDs  
• Copied cards receive new creation timestamps  
• Original cards remain unchanged  
• Archive state is not inherited  
• Archived cards can be copied into new active cards

## v6.3 · Dashboard Quick Access

• Made all five dashboard count boxes clickable  
• Each count opens its corresponding expanded workspace  
• Added hover feedback  
• Added keyboard access using Enter and Space  
• Count boxes and column headers provide equivalent navigation

## v6.2 · Complete and Archive Workflow

• Replaced direct card deletion with Complete  
• Added Archive, Delete Permanently and Cancel choices  
• Added archive timestamps  
• Added Show Archive / Hide Archive  
• Added archive-mode notification  
• Added archived-card styling  
• Added ARCHIVED status  
• Added Restore functionality  
• Archived cards remain associated with their original columns  
• Archived cards are excluded from active dashboard counts  
• Archived cards cannot be dragged between active columns

## v6.1 · Dashboard Colour Integration

• Colour-coded the five dashboard count boxes  
• Matched count boxes to their corresponding workflows  
• Extended the colour system across the dashboard

## v6.0 · Expanded View Sorting

• Added sorting controls to expanded workspaces  
• Added urgency sorting  
• Added creation-date sorting  
• Added alphabetical sorting  
• Added workspace-specific sorting criteria

## v5.9 · Expanded Column View

• Made all five column headers clickable  
• Added full-window expanded workspaces  
• Added responsive card grids  
• Added dedicated workspace search  
• Added + Add Here  
• Retained card actions inside expanded views  
• Added workspace colour themes  
• Added multiple closing methods  
• Improved usability on smaller laptop screens

## v5.8 · Priority Sorting

• Added automatic urgency-based sorting  
• Cards ordered from highest to lowest urgency  
• Introduced common urgency ranking across card types  
• Cards with equal urgency sorted newest first

## v5.7 · Card Creation Timestamps

• Added automatic creation date and time  
• Applied timestamps across the five main card categories  
• Preserved timestamps during editing and movement  
• Included timestamps in exported backups  
• Added Date unavailable handling for legacy cards

## v5.6 · Visual Cohesion

• Colour-coded + Add category buttons  
• Matched creation controls to destination columns  
• Added hover feedback

## v5.5 · Data Portability

• Added Export Data  
• Added Import Data  
• Added portable JSON backups  
• Added backup metadata  
• Added backup validation  
• Added import confirmation  
• Added automatic pre-import safety backup  
• Enabled migration between computers

## v5.4 · Schedule Management Fix

• Fixed scheduled-task deletion  
• Improved deletion event handling  
• Added deletion confirmation

## v5.3 · Receiving Workflow

• Added TO RECEIVE  
• Expanded Kanban to five operational columns  
• Added TO ORDER → TO RECEIVE transfer  
• Added receipt-status workflow  
• Added Mark Received  
• Introduced distinct column colours

## v5.2 · Header Controls

• Consolidated primary controls into one header row  
• Added Toggle Schedule  
• Prevented schedule controls from obstructing + Add

## v5.1 · Rendering Reliability

• Improved initial board rendering  
• Improved browser compatibility  
• Strengthened localStorage handling

## v5.0 · Operational Redesign

• Rebuilt dashboard around Crystal Club operations  
• Introduced TO DO, TO ORDER, GUEST NOTES and HANDOVER  
• Added specialised card forms  
• Added search and filtering  
• Added drag-and-drop workflow  
• Separated Today's Scheduled Tasks from Kanban columns

## v4.0 · Floating Schedule

• Converted Today's Scheduled Tasks into a floating overlay  
• Added approximately 80% opaque background  
• Added hide and restore functionality  
• Removed schedule from Kanban column structure

## v3.x · Scheduling Expansion

• Added recurring schedule management  
• Added weekday scheduling  
• Added first and last days of month rules  
• Added specific monthly dates  
• Added one-off dated tasks  
• Removed Reset Demo  
• Renamed application GPCH Crystal Club

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
• Dedicated Leave Requests workspace  
• Consistent workspace interaction  
• One-click card duplication  
• Direct workflow controls  
• Easy migration between computers  
• Static GitHub Pages deployment

## Current Limitation

The dashboard does not provide real-time synchronisation between multiple computers.

A shared backend or cloud database would be required for simultaneous multi-workstation synchronisation.

---

# Project Status

Active development.

The dashboard continues to evolve around practical GPCH Crystal Club operations, with emphasis on consistent interaction patterns, minimal-click workflows, efficient use of limited screen space, operational visibility, historical records, shift communication, staff leave tracking, recurring task management, data portability and traceability.
