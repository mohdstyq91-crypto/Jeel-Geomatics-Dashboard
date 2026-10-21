# Draughtsmen Daily Status Dashboard: Setup and Office Workflow Guide

Survey / Drafting Division. For supervisors and draughtsmen (Istiyaque, Irfan, Ali, Sudheer).

Dashboard link: https://claude.ai/artifact/VMHrqzaZvyMs4JuKQkvkp8

## 1. What this is

A web dashboard that records each draughtsman's daily project status: input data received from site, work description, progress %, status, deadline and remarks. Records are saved in a shared database, so everyone sees the same live data.

This repository only holds documentation. The dashboard and its data are not stored here.

## 2. Installation

Nothing needs to be installed. The dashboard opens in a web browser.

1. The owner (supervisor) opens the dashboard link and signs in to Claude.
2. In the dashboard's share controls, add each team member by their Claude account email and choose an access level (section 3).
3. Each person opens the link while signed in. The Dashboard should show the badge **Shared database · live**.
4. If the badge says **Local only**, the person is not signed in or the shared database is not available to them. Entries made in that state are not shared.
5. To try it out, click **Load sample data** on the Dashboard. Sample records are labelled SAMPLE and can be deleted from the Task Register. Admins can also use **Settings & Backup** to reload or clear data.

Do not copy the dashboard's HTML file to GitHub Pages or another website. A copy cannot use the shared database and will run in Local only mode.

## 3. Access levels

| Person | Suggested access | What they can do |
|---|---|---|
| Supervisor / owner | Owner or Editor | Edit every record, clear or restore all data |
| Draughtsmen | Contributor | Add, edit, copy, transfer and delete tasks |
| Managers, site team | Viewer | Read-only |

## 4. Who can change which task

Each draughtsman chooses their name under **I am** on the Dashboard (once per browser). They can then add and change only tasks assigned to that name. Owners and Editors are marked **Admin** and can change any task.

This is a working-practice guard, not strict security. A Contributor could choose another name. For tighter control, give draughtsmen Viewer access and have the supervisor enter updates.

Every record shows **by [name]** under Last Updated, so changes can be traced to the last person who saved.

## 5. Daily routine

**Each draughtsman, every working day**

1. Open the dashboard and select your name under **I am**.
2. Click **+ Add New Task** for new work, or **Edit** on an existing task.
3. Set Input Data Received Date when the site team supplies data. Leave it blank to show *Awaiting Site Data*.
4. Update Processing Status (%). Status becomes Pending at 0% and In Progress from 1% to 99%.
5. Choose **Incomplete** if the work is blocked (missing data, corrections needed). Write the reason in Remarks.
6. When the work is finished and checked, set Overall Status to **Completed** (requires 100%).

**Supervisor, daily**

1. Check the Overdue, Due today and Awaiting Site Data warnings on the Dashboard.
2. Use **Daily / Range Reports** for the date, then print or export (PDF, Excel, CSV).
3. Chase the site team for any task awaiting input data.

## 6. Transferring tasks when someone is absent

- **One task:** click **Transfer** on its row, choose the draughtsman who takes over, and optionally enter a reason (for example, "on leave until 25/10").
- **All open tasks:** open **Draughtsman-wise Work Status**, select the absent person's tab and click **Transfer all open tasks**. Completed tasks stay where they are.
- All details move with the task: progress, status, project, dates, description and remarks. A line recording the transfer is added to the remarks, and the row shows a "Transferred from [name]" badge.
- A draughtsman can transfer only his own tasks. If the absent person cannot do it, the supervisor (Admin) transfers on their behalf.
- To review transfers, click the purple **Transferred** card on the Dashboard, or the **Transferred** filter button. A Transfer details table lists the date, project, from, to, reason, progress and current owner.

## 7. Status and warning rules

- **Completed** is never set automatically. At 100% a task shows "100% – confirm completion" until someone confirms it.
- **Overdue** appears as a separate red badge when the deadline has passed and the task is not completed.
- Warnings are shown for: overdue tasks, due today, due within 2 days, awaiting site data, and no update for 3 or more days.

## 8. Reports and exports

Exports on **Export / Print** use the filters currently set on the Dashboard or Task Register and include the generation date. The browser asks you to confirm each file save. Use **Print daily report** for a paper copy of the selected date.

## 9. Backup and recovery

- Supervisor: download a JSON backup from **Settings & Backup** at least weekly, and before any bulk change.
- To recover, use **Restore from file** (admins only). This replaces all current records with the backup.
- Deleting a record asks for confirmation and cannot be undone, except from a backup.
- This repository is public. Do not commit backups or exports containing real project data.

## 10. Known limitations

- Access is set per dashboard, not per task. Everyone with write access can write to the shared data.
- There is no change history, only the last editor and time (plus the transfer log).
- Data lives inside the dashboard. If the dashboard is deleted, the data goes with it, so keep backups.
- Everyone needs a Claude account to open the dashboard.
- Moving to a company database (PostgreSQL, MySQL, SQLite) with login-based roles would need a separate backend and developer time.

## 11. Troubleshooting

| Problem | Fix |
|---|---|
| Badge says Local only | Sign in to Claude and reopen the link |
| Access error when opening the link | Ask the supervisor to share the dashboard with your account |
| "Select who you are" message | Choose your name under **I am** |
| "Could not save to the shared database" | You have Viewer access. Ask the owner for Contributor access |
| Export does nothing | Accept the save prompt, and check the filters are not hiding all records |
