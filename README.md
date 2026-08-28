# GPCH Kanban

Single-page operational Kanban dashboard designed for GPCH Crystal Club.

GPCH Kanban consolidates daily tasks, ordering, receiving, guest notes, shift handovers, leave requests, inventory, archived records and recurring operational schedules into one lightweight browser-based workspace.

## Live Dashboard

https://averydimbulb79.github.io/GPCH_kanban/

Current version: 6.9

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

Two additional operational workspaces are available without occupying permanent Kanban columns:

`LEAVE REQUESTS`

`INVENTORY`

This keeps the five-column board focused while allowing supporting operational functions to use the same familiar full-window card interface.

---

# Core Features

• Five colour-coded main Kanban workflows  
• Dedicated Leave Requests workspace  
• Dedicated Inventory workspace  
• Matching colour-coded dashboard count boxes  
• Clickable count boxes and column headers  
• Full-window workspace views  
• Consistent card creation and editing workflow  
• Workspace-specific search and sorting  
• Archive visibility within expanded workspaces  
• Automatic urgency-based card sorting  
• Card creation timestamps  
• Last-updated timestamps for inventory  
• One-click card duplication  
• Complete and archive workflow  
• Archived-card restoration  
• Drag-and-drop Kanban workflow  
• Streamlined ordering and receiving process  
• Quick inventory quantity adjustments  
• Contextual one-click workflow actions  
• Recurring scheduled tasks  
• Weekly and monthly scheduling rules  
• Floating Today's Scheduled Tasks overlay  
• Board-wide search and filtering  
• Centralised Settings menu  
• JSON data export and import  
• Leave Request and Inventory backup support  
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

Clicking either a dashboard count box or column header opens the corresponding full-window workspace.

Keyboard access using `Enter` and `Space` is also supported on the count boxes.

---

# Main Controls

The primary controls are organised around frequently used operational functions:

`+ Add`

`Leave Request`

`Inventory`

`Toggle Schedule`

`Show Archive / Hide Archive`

`Settings`

Leave Requests and Inventory are intentionally accessed from dedicated buttons rather than being added as permanent Kanban columns.

This preserves horizontal screen space while keeping both functions immediately accessible.

---

# Settings

Administrative and data-management functions are grouped under:

`Settings`

Settings provides access to:

`Manage Schedule`

`Export Data`

`Import Data`

This reduces header clutter and separates configuration functions from everyday operational actions.

---

# Full-Window Workspaces

The five Kanban columns can each be opened as dedicated full-window workspaces:

`TO DO`

`TO ORDER`

`TO RECEIVE`

`GUEST NOTES`

`HANDOVER`

Additional full-window workspaces are provided for:

`LEAVE REQUESTS`

`INVENTORY`

The overall interface therefore provides two complementary operating modes:

`Main Kanban = operational overview`

`Full-window workspace = focused work`

This is particularly useful on smaller laptop screens where displaying five Kanban columns simultaneously limits card width.

---

# Consistent Workspace Interface

Expanded workspaces follow a common interaction pattern.

Typical controls include:

`Search`

`Sort`

`+ Add Here`

`Show Archived / Hide Archived`

`× Close`

The general interaction model is:

`Open workspace → Review cards → Add or act on card → Save → Continue`

This consistency reduces the number of different interaction patterns staff need to learn.

---

# Inventory

Version 6.9 introduces Inventory as a dedicated full-window operational workspace.

Inventory does not occupy another permanent column on the main Kanban.

Instead:

`Inventory → Full-window Inventory workspace`

This provides stock visibility without making the existing five-column dashboard narrower or more crowded.

---

# Inventory Workspace

Selecting:

`Inventory`

opens the dedicated:

`INVENTORY`

workspace.

The toolbar provides:

`Search inventory`

`Sort`

`+ Add Here`

`Show Archived / Hide Archived`

`× Close`

Inventory cards are displayed in a responsive grid using the same visual and interaction principles as other expanded workspaces.

---

# Adding Inventory Items

Select:

`+ Add Here`

inside Inventory.

The inventory card form contains:

• Item Name  
• Item Type / Category  
• Kept Location  
• Quantity  
• Unit  
• Notes

Available units include:

• pcs  
• boxes  
• bottles  
• packets  
• cartons  
• sets  
• units  
• other

Inventory deliberately does not require minimum stock levels, par levels or automatically calculated stock statuses.

The workspace is intended to remain a straightforward operational stock record rather than a complex inventory-management system.

---

# Inventory Cards

A typical inventory card contains:

`ITEM TYPE`

`LOCATION`

`Item Name`

`Quantity: 6 boxes`

`− Use     + Restock`

`Updated: 28 Aug 2026, 15:01`

`Created: 28 Aug 2026, 14:30`

Standard card controls remain:

`Copy`

`Edit`

`Complete`

Archived inventory cards provide:

`Copy`

`Restore`

---

# Inventory Quantity Controls

Inventory cards provide two direct stock-adjustment controls:

`− Use`

`+ Restock`

These allow quantity changes without opening the full Edit form.

## Use

Selecting:

`− Use`

asks how many units were used.

The entered quantity is deducted from the current stock quantity.

The system prevents a deduction greater than the recorded quantity.

## Restock

Selecting:

`+ Restock`

asks how many units were added.

The entered quantity is added to the existing stock quantity.

Both actions automatically update the inventory item's Last Updated timestamp.

This provides a faster operational workflow than repeatedly opening and editing inventory cards.

---

# Inventory Timestamps

Inventory records maintain two timestamps.

## Created

Records when the inventory card was originally created.

## Updated

Records the most recent inventory change.

The Updated timestamp changes when:

• Quantity is reduced using `− Use`  
• Quantity is increased using `+ Restock`  
• The inventory card is edited  
• The inventory card is archived  
• The inventory card is restored

This provides a simple indication of how recently an inventory record was maintained.

---

# Inventory Search

Inventory includes dedicated search.

Search can locate information contained within inventory records, including:

• Item name  
• Item type  
• Category  
• Storage location  
• Unit  
• Notes

This allows staff to locate an item without manually scanning the entire inventory.

---

# Inventory Sorting

The Inventory workspace supports:

• Item: A → Z  
• Item: Z → A  
• Item Type: A → Z  
• Location: A → Z  
• Quantity: Low → High  
• Quantity: High → Low  
• Recently Updated  
• Oldest Updated

The default inventory view sorts items alphabetically.

---

# Inventory Archive

Inventory records that are no longer required can be completed and archived.

Select:

`Complete`

to archive an inventory item.

Archived inventory cards are removed from the normal active Inventory workspace.

Select:

`Show Archived`

to display them.

The control changes to:

`Hide Archived`

while archived records are visible.

Archived inventory cards can be returned to active status using:

`Restore`

---

# Inventory Duplication

Inventory cards support:

`Copy`

Copy opens a new Inventory Item form prefilled with information from the selected inventory record.

The copied card receives:

• A new unique ID  
• A new creation timestamp  
• A new updated timestamp  
• Active status  
• No inherited archive timestamp

Information can be changed before the copied record is saved.

This is useful when creating similar inventory items stored in different locations or recorded in different units.

---

# Leave Requests

Leave Requests operates as another dedicated full-window workspace.

Selecting:

`Leave Request`

opens:

`LEAVE REQUESTS`

without adding a sixth permanent column to the main Kanban.

The toolbar provides:

`Search leave requests`

`Sort`

`+ Add Here`

`Show Archived / Hide Archived`

`× Close`

---

# Adding Leave Requests

Select:

`+ Add Here`

inside Leave Requests.

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

Every leave request receives its own creation timestamp.

---

# Leave Request Cards

Leave request cards can display:

• Staff name  
• Leave type  
• Start date  
• End date  
• Approval status  
• Notes  
• Creation timestamp  
• Archive information

Card actions include:

`Copy`

`Edit`

`Complete`

Archived cards provide:

`Copy`

`Restore`

---

# Leave Request Sorting

Leave Requests supports:

• Start Date: Earliest First  
• Start Date: Latest First  
• Newest First  
• Oldest First  
• Staff Name: A → Z  
• Staff Name: Z → A  
• Status: A → Z

The default view prioritises upcoming leave chronologically.

---

# Board Structure

The main Kanban retains five permanent columns.

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

For items already ordered but awaiting delivery or collection.

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

This prevents narrow cards from becoming overloaded with buttons while keeping frequently used actions one click away.

---

# Copy Card

Selecting:

`Copy`

opens a new-card form prefilled with information from the selected card.

The copied card receives:

• A new unique ID  
• A new creation timestamp  
• Active status  
• No inherited archive timestamp

The original card remains unchanged.

Archived cards can also be copied into new active records.

---

# TO ORDER Workflow

TO ORDER cards position the primary workflow action directly beside Quantity.

Example:

`Quantity: 1     Move to Receive →`

Selecting:

`Move to Receive →`

moves the card from:

`TO ORDER → TO RECEIVE`

The footer remains:

`Copy · Edit · Complete`

---

# TO RECEIVE Workflow

TO RECEIVE cards follow the same contextual design.

Example:

`Quantity: 4     ✓ Mark Received`

Selecting:

`✓ Mark Received`

moves the item into the completion workflow.

The footer remains:

`Copy · Edit · Complete`

---

# Workflow Design Principle

Workflow transitions are positioned close to the information they affect.

General card-management actions remain grouped separately.

Therefore:

`TO ORDER → Move to Receive`

`TO RECEIVE → Mark Received`

while:

`Copy · Edit · Complete`

remain universal card-management actions.

This keeps frequently used actions immediately accessible without adding secondary menus.

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

Recovery is only possible if the information exists in a previous exported backup.

## Restore

Archived cards can be returned to active status using:

`Restore`

---

# Archive Access

Archive visibility is available at multiple levels.

## Main Board

Use:

`Show Archive / Hide Archive`

to control archived cards across the main Kanban.

## Expanded Kanban Workspaces

Each expanded workspace provides:

`Show Archived / Hide Archived`

This allows historical records to be reviewed without leaving the current workspace.

## Leave Requests

Leave Requests provides its own archive visibility control.

## Inventory

Inventory provides its own archive visibility control.

This keeps historical records separated according to operational context.

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

Leave Requests and Inventory use their own purpose-specific sorting controls.

---

# Card Creation Timestamps

New cards automatically record their creation date and time.

Creation timestamps apply to:

• TO DO  
• TO ORDER  
• TO RECEIVE  
• GUEST NOTES  
• HANDOVER  
• LEAVE REQUESTS  
• INVENTORY

The original creation timestamp remains attached when a record is edited or archived.

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

Search can locate:

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

Leave Requests and Inventory each provide dedicated search functions.

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
• Inventory cards  
• Inventory quantities  
• Inventory updated timestamps  
• Archived inventory records  
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

• Active Kanban cards  
• Archived Kanban cards  
• Creation timestamps  
• Archive timestamps  
• Leave requests  
• Archived leave requests  
• Inventory records  
• Inventory quantities  
• Inventory timestamps  
• Archived inventory records  
• Scheduled tasks  
• Scheduled-task completion state  
• Application version  
• Export timestamp  
• Record counts

## Import Data

Import Data restores a previously exported GPCH Crystal Club backup.

The application validates the backup before replacing current data.

Older valid GPCH backups that do not contain Leave Request or Inventory data remain supported.

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

The operational dataset, including Leave Requests and Inventory, is then restored.

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

## v6.9 · Inventory Workspace

• Added dedicated Inventory button to the main dashboard  
• Added full-window INVENTORY workspace  
• Kept Inventory outside the five-column Kanban to preserve screen space  
• Added responsive inventory card grid  
• Added Inventory search  
• Added Inventory sorting  
• Added `+ Add Here`  
• Added `Show Archived / Hide Archived`  
• Added `× Close`  
• Added Item Name field  
• Added Item Type / Category field  
• Added Kept Location field  
• Added Quantity field  
• Added Unit field  
• Added Notes field  
• Added inventory creation timestamps  
• Added automatic Last Updated timestamps  
• Added `− Use` quick quantity adjustment  
• Added `+ Restock` quick quantity adjustment  
• Prevented stock usage greater than the recorded quantity  
• Added Copy support  
• Added Edit support  
• Added Complete and Archive support  
• Added Restore support for archived inventory items  
• Added Item A → Z and Z → A sorting  
• Added Item Type sorting  
• Added Location sorting  
• Added Quantity Low → High and High → Low sorting  
• Added Recently Updated and Oldest Updated sorting  
• Added Inventory data to JSON export and import  
• Added Inventory record counts to backup metadata  
• Maintained compatibility with backups created before Inventory support

## v6.8 · Unified Leave Request Workspace

• Redesigned Leave Requests to use the same full-window interaction pattern as expanded Kanban columns  
• Added dedicated LEAVE REQUESTS workspace  
• Added responsive leave-request card grid  
• Added Leave Request search  
• Added dedicated leave-request sorting  
• Added `+ Add Here`  
• Added `Show Archived / Hide Archived`  
• Added `× Close`  
• Standardised leave request creation around the common card-entry pattern  
• Added Staff Name, Leave Type, Start Date, End Date, Status and Notes  
• Added creation timestamps  
• Retained Copy, Edit, Complete and Restore  
• Kept Leave Requests outside the five-column main Kanban

## v6.7 · Settings and Leave Requests

• Added persistent Leave Request storage  
• Added Leave Request data to export/import backups  
• Added backward compatibility for older backups  
• Added Settings button  
• Moved Manage Schedule under Settings  
• Moved Export Data under Settings  
• Moved Import Data under Settings  
• Reduced main-header clutter  
• Separated administrative controls from daily operational controls

## v6.6 · Expanded Archive Access

• Added Show Archived directly to every expanded Kanban workspace  
• Added Hide Archived state  
• Archived records can be reviewed without returning to the main board  
• Archive display remains limited to the current workspace  
• Retained search and sorting while archived records are displayed

## v6.5 · Streamlined Card Actions

• Separated workflow actions from universal card-management actions  
• Moved Move to Receive beside TO ORDER Quantity  
• Moved Mark Received beside TO RECEIVE Quantity  
• Retained direct one-click workflow transitions  
• Standardised active card footer around Copy, Edit and Complete  
• Reduced button congestion on narrow cards

## v6.4 · Card Duplication

• Added Copy to cards  
• Copy opens a new-card form prefilled with source-card information  
• Copied cards receive new unique IDs and timestamps  
• Original cards remain unchanged  
• Archived cards can be copied into new active cards

## v6.3 · Dashboard Quick Access

• Made all five dashboard count boxes clickable  
• Each count opens its corresponding expanded workspace  
• Added hover feedback  
• Added keyboard access using Enter and Space

## v6.2 · Complete and Archive Workflow

• Replaced direct card deletion with Complete  
• Added Archive, Delete Permanently and Cancel  
• Added archive timestamps  
• Added Show Archive / Hide Archive  
• Added archived-card styling  
• Added Restore functionality  
• Excluded archived cards from active dashboard counts

## v6.1 · Dashboard Colour Integration

• Colour-coded the five dashboard count boxes  
• Matched count boxes to corresponding workflows  
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
• Improved usability on smaller laptop screens

## v5.8 · Priority Sorting

• Added automatic urgency-based sorting  
• Cards ordered from highest to lowest urgency  
• Introduced common urgency ranking across card types

## v5.7 · Card Creation Timestamps

• Added automatic creation date and time  
• Preserved timestamps during editing and movement  
• Included timestamps in exported backups

## v5.6 · Visual Cohesion

• Colour-coded + Add category buttons  
• Matched creation controls to destination columns  
• Added hover feedback

## v5.5 · Data Portability

• Added Export Data  
• Added Import Data  
• Added portable JSON backups  
• Added backup metadata and validation  
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
• Dedicated Inventory workspace  
• Fast inventory quantity adjustments  
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

The dashboard continues to evolve around practical GPCH Crystal Club operations, with emphasis on consistent interaction patterns, minimal-click workflows, efficient use of limited screen space, operational visibility, inventory tracking, historical records, shift communication, staff leave tracking, recurring task management, data portability and traceability.
