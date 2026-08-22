# GPCH Kanban

A single-page operational Kanban dashboard designed for GPCH Crystal Club.

The dashboard brings daily tasks, ordering, receiving, guest notes, shift handovers and recurring operational schedules into one lightweight browser-based workspace.

## Live Dashboard

https://averydimbulb79.github.io/GPCH_kanban/

Current version: 5.7

---

## Board Structure

The dashboard uses five colour-coded operational columns.

| Column | Colour | Purpose |
| --- | --- | --- |
| TO DO | Blue | General tasks, duties and follow-ups |
| TO ORDER | Amber | Items requiring ordering or replenishment |
| TO RECEIVE | Green | Ordered items awaiting delivery or collection |
| GUEST NOTES | Pink | Guest preferences, requests and service information |
| HANDOVER | Violet | Outstanding matters for communication between shifts |

Cards can be moved between columns using drag-and-drop.

The "+ Add" menu uses the same colours as the corresponding columns, providing a consistent visual language throughout the dashboard.

---

## Card Creation Timestamps

Every newly created card automatically records its creation date and time.

Example:

`Created: 22 Aug 2026, 14:11`

Creation timestamps apply to all five card types:

• TO DO  
• TO ORDER  
• TO RECEIVE  
• GUEST NOTES  
• HANDOVER

The original timestamp is preserved when a card is edited or transferred to another column, providing a simple operational audit trail.

Cards created before Version 5.7 may display:

`Created: Date unavailable`

because their original creation time was not previously stored.

---

## Ordering Workflow

The procurement workflow separates items that still need to be ordered from items already awaiting delivery.

`TO ORDER → TO RECEIVE → RECEIVED`

A TO ORDER card includes a "Move to Receive" control.

Once an order has been placed, the card moves to TO RECEIVE and becomes an item awaiting receipt.

When the item arrives, it can be marked as received and removed from the active board.

---

## Today's Scheduled Tasks

Recurring operational duties appear in a floating "Today's Scheduled Tasks" overlay at the top-right of the dashboard.

The overlay:

• Uses an approximately 80% opaque background  
• Floats above the Kanban without occupying a column  
• Automatically displays tasks applicable to the current date  
• Allows today's occurrences to be marked complete  
• Can be hidden or restored using "Toggle Schedule"

Completing a scheduled task does not delete its recurrence. It will appear again on its next scheduled date.

---

## Schedule Manager

"Manage Schedule" provides a dedicated interface for creating, editing and deleting recurring operational duties.

Each scheduled task can include:

• Task name  
• Time  
• Category  
• Recurrence rule

### Supported Recurrence Rules

| Schedule | Function |
| --- | --- |
| Weekly | Selected weekdays |
| First N Days | First specified number of days each month |
| Last N Days | Final specified number of days each month |
| Monthly Day | Specific calendar day every month |
| One-Off | One specific date |

This supports both routine weekly duties and month-start or month-end operational tasks.

---

## Card Types

### TO DO

Suitable for:

• Operational tasks  
• Follow-ups  
• Administrative work  
• Equipment issues  
• Time-sensitive duties

Cards can include priority, due time, assignment and notes.

### TO ORDER

Suitable for:

• Stock replenishment  
• Supplies  
• Equipment  
• Consumables  
• Procurement requests

Cards can include quantity, urgency, order status, supplier or department and notes.

### TO RECEIVE

For items that have already been ordered but have not yet been received.

Cards retain relevant ordering information so outstanding deliveries remain visible until completed.

### GUEST NOTES

Suitable for:

• Guest preferences  
• Special requests  
• Room information  
• Arrival and departure details  
• Service requirements  
• Follow-up information

### HANDOVER

For matters requiring continuity between shifts.

Cards can include room or area, originating shift, receiving shift, priority, follow-up time and details.

---

## Search and Filtering

The universal search function can locate information across the board, including:

• Tasks  
• Items  
• Room numbers  
• Guest names  
• Notes  
• Suppliers  
• Departments  
• Handover information

The board can also be filtered by:

• All Columns  
• To Do  
• To Order  
• To Receive  
• Guest Notes  
• Handover

---

## Main Controls

The primary dashboard controls are grouped together for quick access:

`+ Add` · `Manage Schedule` · `Toggle Schedule` · `Export Data` · `Import Data`

---

## Data Storage

GPCH Crystal Club uses browser `localStorage`.

Cards, timestamps, schedules and other operational information remain available after:

• Refreshing the page  
• Closing the browser  
• Restarting the computer  
• Reopening the dashboard

No external database or login is required.

### Important

Operational data is stored in the individual browser.

GitHub Pages hosts the application itself but does not store the Kanban data.

Data entered on one computer therefore does not automatically appear on another computer.

Version 5.5 introduced data export and import to provide backup and computer migration.

---

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

`GPCH_Crystal_Club_Backup_2026-08-22_1411.json`

The file can be retained as a backup or transferred to another computer.

---

## Import Data

"Import Data" restores a previously exported GPCH Crystal Club backup.

Before importing, the application:

1. Validates the JSON file.
2. Confirms that it is a GPCH Crystal Club backup.
3. Displays the number of cards and scheduled tasks.
4. Displays the backup version.
5. Requests confirmation before replacing existing data.

### Automatic Safety Backup

Before imported data replaces the current browser dataset, the application automatically exports the existing data.

Example:

`GPCH_Crystal_Club_PreImport_Backup_2026-08-22_1411.json`

This provides a recovery point if the wrong backup is imported.

---

## Moving to Another Computer

### Old Computer

1. Open GPCH Crystal Club.
2. Select "Export Data".
3. Save the generated JSON file.
4. Transfer the file to the new computer.

### New Computer

1. Open GPCH Crystal Club.
2. Select "Import Data".
3. Choose the exported JSON file.
4. Review the backup information.
5. Confirm the import.

The Kanban cards, creation timestamps and scheduled-task data will then be restored in the new browser.

---

## Technology

The application deliberately uses a lightweight architecture:

• HTML  
• CSS  
• Vanilla JavaScript  
• Browser localStorage  
• JSON backup and restore  
• GitHub Pages

There is no JavaScript framework, server-side application, external database or installation requirement.

The entire application is contained within a single HTML page.

---

# Version History

## v5.7 · Card Creation Timestamps

• Added automatic creation date and time to every new card  
• Applied timestamps across all five Kanban categories  
• Creation timestamps remain unchanged when cards are edited  
• Creation timestamps remain attached when cards move between columns  
• Added timestamps to exported backup data  
• Existing legacy cards display "Date unavailable" where no original timestamp exists  
• Added a simple operational audit trail for determining when notes and tasks were created

## v5.6 · Visual Cohesion

• Colour-coded "+ Add" category buttons  
• Add buttons correspond visually with their destination columns  
• Blue TO DO  
• Amber TO ORDER  
• Green TO RECEIVE  
• Pink GUEST NOTE  
• Violet HANDOVER  
• Added subtle hover feedback  
• Improved overall visual consistency

## v5.5 · Data Portability

• Added Export Data  
• Added Import Data  
• Added portable JSON backups  
• Added version and timestamp metadata  
• Added record counts  
• Added backup validation  
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
• Improved visual hierarchy

## v5.2 · Header Controls

• Consolidated primary controls into one header row  
• Added Toggle Schedule to the main controls  
• Removed the separate floating schedule restoration button  
• Prevented schedule controls from obstructing "+ Add"

## v5.1 · Rendering Reliability

• Rebuilt page rendering for improved reliability  
• Made Kanban columns immediately visible on page load  
• Reduced dependency on dynamically generated structural elements  
• Improved browser compatibility  
• Strengthened localStorage handling

## v5.0 · Operational Redesign

• Rebuilt the dashboard around Crystal Club operations  
• Introduced TO DO  
• Introduced TO ORDER  
• Introduced GUEST NOTES  
• Introduced HANDOVER  
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
• Added first-days-of-month rules  
• Added last-days-of-month rules  
• Added specific monthly dates  
• Added one-off dated tasks  
• Removed Reset Demo to reduce accidental data loss  
• Renamed the application GPCH Crystal Club

---

## Current Architecture

GPCH Crystal Club remains a client-side application.

GitHub Pages distributes the application while operational data remains in browser localStorage.

### Advantages

• Fast loading  
• Simple deployment  
• No login required  
• No server maintenance  
• Local persistence  
• Portable backups  
• Easy migration between computers

### Current Limitation

The dashboard does not provide real-time synchronisation between multiple computers.

A shared backend or cloud database would be required if the project is later expanded into a simultaneously shared live operational board across multiple Crystal Club workstations.

---

## Project Status

Active development.

The dashboard continues to evolve around practical GPCH Crystal Club operations, with emphasis on visibility, speed, intuitive workflows, shift communication, recurring task management, data portability and operational traceability.
