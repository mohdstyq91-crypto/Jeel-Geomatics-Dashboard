# Draughtsmen Daily Status Dashboard: Setup and Office Workflow Guide

Survey / Drafting Division. Team: Istiyaque (admin), Irfan, Ali, Sudheer (users).

Dashboard link: https://claude.ai/artifact/VMHrqzaZvyMs4JuKQkvkp8

This repository holds documentation only. The dashboard and its data are not stored here.

## 1. Roles at a glance

| | Admin (Istiyaque) | Users (Irfan, Ali, Sudheer) |
|---|---|---|
| Add new tasks | Yes, for anyone | Yes, for themselves |
| Edit tasks | Any task | Own tasks only |
| Transfer tasks | Any task, or all open tasks of one person | Own tasks only |
| Copy a task | Yes | No |
| Delete a task | Yes | No |
| Clear all data, reload sample data, restore backup | Yes | No |
| Upload older local records to the shared database | Yes | No |
| Reports, filters, exports, backup download | Yes | Yes |

The dashboard badge shows the role: **Admin: all functions** or **User: add, edit, transfer**.

## 2. One-time setup (done by the dashboard owner)

1. Open the dashboard link and sign in to Claude.
2. In the dashboard's share controls, add each person by the email of their Claude account:
   - **Istiyaque:** Editor (or Owner)
   - **Irfan, Ali, Sudheer:** Contributor
   - **Managers or site staff who only need to look:** Viewer
3. Ask everyone to open the link while signed in.
4. Check that the badge on the Dashboard reads **Shared database · live**. If it says **Local only**, the person is not signed in or cannot reach the shared database, and their entries will not be shared.
5. Each person selects their name under **I am** on the Dashboard (once per browser). Istiyaque selects **Istiyaque**.
6. To try the system, Istiyaque clicks **Load sample data**. Sample records are labelled SAMPLE and can be deleted from the Task Register.

Admin rights need both things: Editor or Owner access, and **Istiyaque** selected under "I am". Anyone else is treated as a user, whatever their access level.

Do not copy the dashboard's HTML file to GitHub Pages or another website. A copy cannot use the shared database and will run in Local only mode.

## 3. Daily routine for users

1. Open the dashboard and check that your name is selected under **I am**.
2. Click **+ Add New Task** for new work, or **Edit** on one of your tasks.
3. Enter the Input Data Received Date when the site team supplies data. Leave it blank to show *Awaiting Site Data*.
4. Update Processing Status (%). Status becomes Pending at 0% and In Progress from 1% to 99%.
5. Choose **Incomplete** if the work is blocked (missing data, corrections needed) and write the reason in Remarks.
6. When the work is finished and checked, set Overall Status to **Completed** (needs 100%).

If you need a task deleted or copied, ask Istiyaque.

## 4. Daily routine for the admin

1. Check the Overdue, Due today and Awaiting Site Data warnings on the Dashboard.
2. Open **Daily / Range Reports** for the date, then print or export (PDF, Excel, CSV).
3. Chase the site team for any task awaiting input data.
4. Delete or copy records when needed (Del and Copy buttons appear only for the admin).
5. Download a JSON backup every week (section 8).

## 5. Transferring tasks when someone is absent

- **One task:** click **Transfer** on its row, choose who takes over, and optionally enter a reason (for example, "on leave until 25/10").
- **All open tasks:** open **Draughtsman-wise Work Status**, select the absent person's tab and click **Transfer all open tasks**. Completed tasks stay where they are.
- All details move with the task: progress, status, project, dates, description and remarks. A line recording the transfer is added to the remarks, and the row shows a "Transferred from [name]" badge.
- Users can transfer only their own tasks. If a person is absent and cannot transfer his tasks, Istiyaque does it for him.
- To review transfers, click the purple **Transferred** card on the Dashboard or the **Transferred** filter button. A Transfer details table lists the date, project, from, to, reason, progress and current owner.

## 6. Status and warning rules

- **Completed** is never set automatically. At 100% a task shows "100% – confirm completion" until someone confirms it.
- **Overdue** appears as a separate red badge when the deadline has passed and the task is not completed.
- Warnings are shown for: overdue tasks, due today, due within 2 days, awaiting site data, and no update for 3 or more days.
- Every record shows **by [name]** under Last Updated.

## 7. Reports and exports

Exports on **Export / Print** use the filters currently set on the Dashboard or Task Register and include the generation date. The browser asks you to confirm each file save. Use **Print daily report** for a paper copy of the selected date.

## 8. Backup and recovery

- Istiyaque downloads a JSON backup from **Settings & Backup** at least weekly, and before any bulk change.
- To recover, Istiyaque uses **Restore from file**. This replaces all current records with the backup.
- Deleting a record asks for confirmation and cannot be undone, except from a backup.
- This repository is public. Do not commit backups or exports that contain real project data.

## 9. Known limitations

- The role rules are enforced by the dashboard screen, not by the database. A user with Contributor access could still change data by other means, and the dashboard cannot stop that. For stricter control, give users Viewer access and have Istiyaque enter their updates.
- "I am" is self-selected, so a user could pick another person's name. Admin functions stay off unless that person also has Editor or Owner access.
- There is no full change history, only the last editor, the time and the transfer log.
- Data lives inside the dashboard. If the dashboard is deleted, the data goes with it, so keep backups.
- Everyone needs a Claude account to open the dashboard.
- A company database (PostgreSQL, MySQL, SQLite) with login-based roles would need a separate backend and developer time.

## 10. Troubleshooting

| Problem | Fix |
|---|---|
| Badge says Local only | Sign in to Claude and reopen the link |
| Access error when opening the link | Ask the owner to share the dashboard with your account |
| "Select who you are" message | Choose your name under **I am** |
| "This task belongs to [name]" message | Users can change only their own tasks. Ask Istiyaque |
| No Copy or Del buttons | Expected for users. Only the admin has them |
| Istiyaque sees "User" badge | Check Editor or Owner access, and that **Istiyaque** is selected under **I am** |
| "Could not save to the shared database" | You have Viewer access. Ask the owner for Contributor access |
| Export does nothing | Accept the save prompt, and check the filters are not hiding all records |
