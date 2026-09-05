# GPCH Kanban

Single-page operational Kanban dashboard designed for GPCH Crystal Club.

GPCH Kanban consolidates daily tasks, ordering, receiving, guest notes, shift handovers, leave requests, inventory, archived records and recurring operational schedules into one lightweight browser-based workspace.

## Live Dashboard

https://averydimbulb79.github.io/GPCH_kanban/

Current version: 7.0

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

This keeps the five-column board focused while allowing supporting operational functions to use the same full-window card interface.

---

# Core Features

• Five colour-coded main Kanban workflows  
• Dedicated Leave Requests workspace  
• Two-column Pending and Approved leave workflow  
• Direct leave approval and decline controls  
• Declined requests remain editable  
• Dedicated Inventory workspace  
• Quick inventory quantity adjustments  
• Matching colour-coded dashboard count boxes  
• Clickable count boxes and column headers  
• Full-window workspace views  
• Consistent card creation and editing workflow  
• Workspace-specific search and sorting  
• Archive visibility within expanded workspaces  
• Automatic urgency-based card sorting  
• Card creation timestamps  
• Inventory Last Updated timestamps  
• One-click card duplication  
• Complete and archive workflow  
• Archived-card restoration  
• Drag-and-drop Kanban workflow  
• Streamlined ordering and receiving process  
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

The interface therefore provides two complementary operating modes:

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

# Leave Requests

Leave Requests operates as a dedicated full-window workflow.

Selecting:

`Leave Request`

opens:

`LEAVE REQUESTS`

The workspace does not occupy another permanent column on the main Kanban.

Version 7.0 introduces a two-column leave-management workflow:

`PENDING | APPROVED`

This separates requests requiring action from requests that have already been approved.

---

# Leave Request Workflow

## Pending Column

The left side of the workspace contains:

`PENDING`

This column contains requests with either:

`Pending`

or:

`Declined`

status.

Pending requests can be:

`✓ Approve`

`Decline`

`Copy`

`Edit`

`Complete`

Approving a request immediately moves it to the Approved column.

Declining a request changes its status to:

`Declined`

but deliberately keeps the card in the Pending column.

This allows the requester or staff member managing the request to edit the information and resubmit or correct it without having to recover the request from another screen.

## Approved Column

The right side contains:

`APPROVED`

Approved requests automatically appear here.

Approved cards remain available for normal card management.

If an approval needs to be reversed, the request can be changed to:

`Declined`

The card then returns to the Pending column.

---

# Leave Request Status Logic

Leave requests use three statuses:

| Status | Workspace Column | Purpose |
| --- | --- | --- |
| Pending | PENDING | Awaiting decision |
| Declined | PENDING | Requires correction, amendment or reconsideration |
| Approved | APPROVED | Request accepted |

The physical workspace therefore has only two columns even though three statuses are supported.

This is intentional.

`Declined` is treated as an actionable state rather than a completed state.

---

# Leave Request Counts

Each Leave Request column displays its current card count.

For example:

`PENDING  3`

`APPROVED  2`

The counts automatically update when requests are:

• Added  
• Approved  
• Declined  
• Archived  
• Restored  
• Filtered through the current workspace view

This gives an immediate indication of outstanding leave administration.

---

# Leave Request Controls

The top Leave Requests toolbar retains:

`Search leave requests`

`Sort`

`+ Add Here`

`Show Archived / Hide Archived`

`× Close`

These controls apply across the Leave Requests workspace.

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

# Approving Leave

A request awaiting approval appears in the Pending column.

Select:

`✓ Approve`

The request status changes to:

`Approved`

and the card immediately moves:

`PENDING → APPROVED`

No additional card needs to be created.

---

# Declining Leave

Select:

`Decline`

on a Pending request.

The status changes to:

`Declined`

The request remains in the Pending column.

This is important because a declined request may require the requester to:

• Correct the dates  
• Change the leave type  
• Amend the notes  
• Clarify the request  
• Resubmit the request

The existing:

`Edit`

control remains available.

Once amended, the card can subsequently be approved.

---

# Reversing an Approval

Approved leave is not permanently locked into the Approved column.

An Approved card provides:

`Move to Declined`

Selecting this changes the status to:

`Declined`

and returns the card to:

`PENDING`

This provides a simple correction mechanism if circumstances change or an approval was made incorrectly.

---

# Leave Request Search

Search operates across both Pending and Approved leave requests.

It can locate information contained within the leave record, including:

• Staff name  
• Leave type  
• Status  
• Dates  
• Notes

Matching cards remain displayed in their appropriate workflow column.

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

Sorting is applied within the two-column workflow.

---

# Leave Request Archive

Leave requests can still be completed and archived.

Archived requests are hidden from the normal Leave Requests workspace.

Select:

`Show Archived`

to include archived records.

The control changes to:

`Hide Archived`

while archive visibility is active.

Archived leave cards can be returned to active status using:

`Restore`

The request then returns to the appropriate Pending or Approved column according to its status.

---

# Leave Request Duplication

Leave cards support:

`Copy`

Copy opens a new Leave Request form prefilled using the selected request.

The copied request receives:

• A new unique ID  
• A new creation timestamp  
• Active status  
• No inherited archive timestamp

The copied information can be edited before saving.

---

# Inventory

Version 6.9 introduced Inventory as a dedicated full-window operational workspace.

Inventory does not occupy another permanent column on the main Kanban.

Instead:

`Inventory → Full-window Inventory workspace`

This provides stock visibility without making the existing five-column dashboard narrower or more crowded.

---

# Inventory Workspace

Selecting:

`Inventory`

opens:

`INVENTORY`

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

# Inventory Quantity Controls

Inventory cards provide two direct stock-adjustment controls:

`− Use`

`+ Restock`

Selecting:

`− Use`

asks how many units were used and deducts that quantity from the current stock.

The system prevents a deduction greater than the recorded quantity.

Selecting:

`+ Restock`

asks how many units were added and increases the recorded quantity.

Both actions automatically update the item's Last Updated timestamp.

---

# Inventory Timestamps

Inventory records maintain:

`Created`

and:

`Updated`

timestamps.

Created records when the inventory card was originally created.

Updated records the most recent inventory change.

The Updated timestamp changes when quantity is adjusted, the card is edited, archived or restored.

---

# Inventory Search and Sorting

Inventory search can locate:

• Item name  
• Item type  
• Category  
• Storage location  
• Unit  
• Notes

Sorting options include:

• Item: A → Z  
• Item: Z → A  
• Item Type: A → Z  
• Location: A → Z  
• Quantity: Low → High  
• Quantity: High → Low  
• Recently Updated  
• Oldest Updated

---

# Inventory Archive

Inventory records that are no longer required can be archived using:

`Complete`

Archived inventory cards are removed from the normal active Inventory workspace.

Select:

`Show Archived`

to display them.

Archived inventory cards can be returned to active status using:

`Restore`

---

# Board Structure

The main Kanban retains five permanent columns.

## TO DO

For operational tasks, follow-ups, administrative duties, equipment matters and time-sensitive work.

## TO ORDER

For items requiring procurement or replenishment.

Cards can include item, quantity, urgency, order status, supplier or department and notes.

## TO RECEIVE

For items already ordered but awaiting delivery or collection.

This distinguishes:

`Needs ordering`

from:

`Already ordered and awaiting receipt`

## GUEST NOTES

For guest preferences, special requests, room information, arrival and departure details, service requirements and follow-up matters.

## HANDOVER

For matters requiring continuity between shifts.

---

# Card Actions

Active Kanban cards use three common management controls:

`Copy`

`Edit`

`Complete`

Workflow-specific actions are positioned separately where appropriate.

This prevents narrow cards from becoming overloaded with buttons while keeping frequently used actions one click away.

---

# TO ORDER Workflow

TO ORDER cards position the primary workflow action directly beside Quantity.

`Move to Receive →`

moves the card:

`TO ORDER → TO RECEIVE`

The standard footer remains:

`Copy · Edit · Complete`

---

# TO RECEIVE Workflow

TO RECEIVE cards provide:

`✓ Mark Received`

This moves the item into the completion workflow.

The standard footer remains:

`Copy · Edit · Complete`

---

# Complete and Archive Workflow

Active Kanban cards use:

`Complete`

instead of immediate deletion.

The main Kanban completion workflow provides:

`Archive`

`Delete Permanently`

`Cancel`

Archive preserves the record while removing it from normal active operations.

Archived records can subsequently be restored.

---

# Automatic Urgency Sorting

The main Kanban automatically orders cards by operational urgency.

General hierarchy:

`URGENT → IMPORTANT → ATTENTION → ROUTINE / NORMAL`

Cards with equal urgency are generally sorted newest first.

---

# Expanded Workspace Sorting

The five expanded Kanban workspaces support common sorting including:

• Urgency: High → Low  
• Urgency: Low → High  
• Newest First  
• Oldest First  
• Title: A → Z  
• Title: Z → A

Additional workspace-specific sorting is available.

TO DO supports due-time sorting.

TO ORDER and TO RECEIVE support status sorting.

GUEST NOTES supports arrival, departure and room sorting.

HANDOVER supports follow-up-time sorting.

Leave Requests and Inventory use their own purpose-specific sorting controls.

---

# Today's Scheduled Tasks

Recurring operational duties appear in a floating:

`Today's Scheduled Tasks`

overlay.

The overlay automatically displays tasks applicable to the current date.

Completing today's occurrence does not delete the recurring schedule.

The task returns on its next applicable date.

---

# Schedule Manager

Schedule management is accessed through:

`Settings → Manage Schedule`

Supported scheduling rules include:

| Schedule | Function |
| --- | --- |
| Weekly | Selected weekdays |
| First N Days | First specified number of days each month |
| Last N Days | Final specified number of days each month |
| Monthly Day | Specific calendar day each month |
| One-Off | One specific date |

---

# Data Storage

GPCH Crystal Club uses browser `localStorage`.

Stored information includes:

• Active and archived Kanban cards  
• Creation and archive timestamps  
• Leave requests and their approval status  
• Archived leave requests  
• Inventory records and quantities  
• Inventory updated timestamps  
• Archived inventory records  
• Scheduled tasks  
• Schedule completion information

Data remains available after refreshing the page, closing the browser, restarting the computer and reopening the dashboard.

No external database or login is required.

---

# Export and Import

Data-management controls are located under:

`Settings`

Export Data creates a portable JSON backup containing the operational dataset.

This includes:

• Kanban cards  
• Archived records  
• Leave requests  
• Leave approval statuses  
• Inventory records  
• Inventory quantities  
• Scheduled tasks  
• Schedule completion state  
• Application version  
• Export timestamp  
• Record counts

Import Data restores a previously exported GPCH Crystal Club backup.

Older valid backups that do not contain newer Leave Request or Inventory data remain supported.

---

# Automatic Safety Backup

Before imported data replaces the current browser dataset, GPCH Crystal Club automatically exports the existing data.

This provides a recovery point if an incorrect or outdated backup is imported.

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

## v7.0 · Leave Approval Workflow

• Redesigned Leave Requests into a two-column workflow  
• Added dedicated PENDING column  
• Added dedicated APPROVED column  
• Added live card counts to both leave columns  
• Pending requests remain in PENDING  
• Approved requests automatically move to APPROVED  
• Declined requests remain in PENDING for correction or amendment  
• Added direct `✓ Approve` action  
• Added direct `Decline` action  
• Added `Move to Declined` action for previously approved requests  
• Preserved Edit access for declined requests  
• Preserved Copy, Edit and Complete controls  
• Preserved Leave Request search  
• Preserved Leave Request sorting  
• Preserved archive visibility  
• Archived requests restore into the correct workflow column according to status  
• Added distinct visual treatment for Pending, Approved and Declined statuses  
• Added responsive behaviour so the two-column leave workflow remains usable on smaller screens

## v6.9 · Inventory Workspace

• Added dedicated Inventory button  
• Added full-window INVENTORY workspace  
• Kept Inventory outside the five-column Kanban  
• Added responsive inventory card grid  
• Added Inventory search and sorting  
• Added `+ Add Here`  
• Added `Show Archived / Hide Archived`  
• Added Item Name  
• Added Item Type / Category  
• Added Kept Location  
• Added Quantity  
• Added Unit  
• Added Notes  
• Added creation timestamps  
• Added automatic Last Updated timestamps  
• Added `− Use` quick quantity adjustment  
• Added `+ Restock` quick quantity adjustment  
• Prevented stock usage greater than recorded quantity  
• Added Copy, Edit, Complete and Restore  
• Added Inventory data to JSON export and import  
• Maintained compatibility with backups created before Inventory support

## v6.8 · Unified Leave Request Workspace

• Redesigned Leave Requests as a full-window workspace  
• Added responsive leave-request card grid  
• Added Leave Request search and sorting  
• Added `+ Add Here`  
• Added archive visibility  
• Standardised leave request creation around the common card-entry pattern  
• Added Staff Name, Leave Type, Start Date, End Date, Status and Notes  
• Added creation timestamps  
• Kept Leave Requests outside the five-column main Kanban

## v6.7 · Settings and Leave Requests

• Added persistent Leave Request storage  
• Added Leave Request data to backups  
• Added Settings menu  
• Moved Manage Schedule, Export Data and Import Data under Settings  
• Reduced main-header clutter

## v6.6 · Expanded Archive Access

• Added archive visibility directly inside expanded Kanban workspaces  
• Archived records can be reviewed without returning to the main board  
• Retained search and sorting while archived records are displayed

## v6.5 · Streamlined Card Actions

• Separated workflow actions from universal card-management actions  
• Moved Move to Receive beside TO ORDER Quantity  
• Moved Mark Received beside TO RECEIVE Quantity  
• Standardised active card footer around Copy, Edit and Complete  
• Reduced button congestion

## v6.4 · Card Duplication

• Added Copy to cards  
• Copied cards receive new IDs and creation timestamps  
• Original cards remain unchanged  
• Archived cards can be copied into new active cards

## v6.3 · Dashboard Quick Access

• Made all five dashboard count boxes clickable  
• Each count opens its corresponding expanded workspace  
• Added keyboard access

## v6.2 · Complete and Archive Workflow

• Replaced direct card deletion with Complete  
• Added Archive, Delete Permanently and Cancel  
• Added archive timestamps  
• Added archive visibility  
• Added Restore functionality  
• Excluded archived cards from active counts

## v6.1 · Dashboard Colour Integration

• Colour-coded dashboard count boxes  
• Matched count boxes to corresponding workflows

## v6.0 · Expanded View Sorting

• Added sorting controls to expanded workspaces  
• Added urgency, creation-date, alphabetical and workspace-specific sorting

## v5.9 · Expanded Column View

• Added full-window expanded workspaces  
• Added responsive card grids  
• Added dedicated workspace search  
• Added + Add Here  
• Improved usability on smaller laptop screens

## v5.8 · Priority Sorting

• Added automatic urgency-based sorting  
• Cards ordered from highest to lowest urgency

## v5.7 · Card Creation Timestamps

• Added automatic creation date and time  
• Preserved timestamps during editing and movement  
• Included timestamps in backups

## v5.6 · Visual Cohesion

• Colour-coded + Add category buttons  
• Matched creation controls to destination columns

## v5.5 · Data Portability

• Added Export Data and Import Data  
• Added portable JSON backups  
• Added validation and import confirmation  
• Added automatic pre-import safety backup

## v5.4 · Schedule Management Fix

• Fixed scheduled-task deletion  
• Added deletion confirmation

## v5.3 · Receiving Workflow

• Added TO RECEIVE  
• Expanded Kanban to five operational columns  
• Added TO ORDER → TO RECEIVE workflow  
• Added Mark Received

## v5.2 · Header Controls

• Consolidated primary controls into one header row  
• Added Toggle Schedule

## v5.1 · Rendering Reliability

• Improved initial board rendering  
• Improved browser compatibility  
• Strengthened localStorage handling

## v5.0 · Operational Redesign

• Rebuilt dashboard around Crystal Club operations  
• Introduced operational card types  
• Added search, filtering and drag-and-drop workflow

## v4.0 · Floating Schedule

• Converted Today's Scheduled Tasks into a floating overlay  
• Added hide and restore functionality

## v3.x · Scheduling Expansion

• Added recurring schedule management  
• Added weekly and monthly scheduling rules  
• Added one-off tasks  
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
• Dedicated Leave Request approval workflow  
• Editable declined leave requests  
• Dedicated Inventory workspace  
• Fast inventory quantity adjustments  
• Consistent workspace interaction  
• Direct workflow controls  
• Easy migration between computers  
• Static GitHub Pages deployment

## Current Limitation

The dashboard does not provide real-time synchronisation between multiple computers.

A shared backend or cloud database would be required for simultaneous multi-workstation synchronisation.

---

# Project Status

Active development.

The dashboard continues to evolve around practical GPCH Crystal Club operations, with emphasis on consistent interaction patterns, minimal-click workflows, efficient use of limited screen space, operational visibility, leave approval management, editable declined requests, inventory tracking, historical records, shift communication, recurring task management, data portability and traceability.
