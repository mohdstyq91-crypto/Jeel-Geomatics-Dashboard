# Draughtsmen Daily Status Dashboard: Setup and Office Workflow Guide

Survey / Drafting Division. Team: Istiyaque (admin, password protected), Irfan, Ali, Sudheer, Adil (users).

**[Open the dashboard](https://claude.ai/artifact/VMHrqzaZvyMs4JuKQkvkp8)** (or <a href="https://claude.ai/artifact/VMHrqzaZvyMs4JuKQkvkp8" target="_blank" rel="noopener noreferrer">open in a new window</a>)

Tip: if the link opens in the same tab, Ctrl+click (Windows) or Cmd+click (Mac) opens it in a new tab.

**Quick start:** sign in to Claude, open the link, check the badge says "Shared database · live", pick your name under "I am", then add or update your tasks. If you get an access error, ask the supervisor to share the dashboard with your account.

This repository holds documentation only. The dashboard and its data are not stored here.

## 1. Roles at a glance

| | Admin (Istiyaque, after entering the password) | Users (Irfan, Ali, Sudheer, Adil) |
|---|---|---|
| Add new tasks | Yes, for anyone | Yes, for themselves |
| Edit tasks | Any task | Own tasks only |
| Transfer tasks | Any task, or all open tasks of one person | Own tasks only |
| Copy a task | Yes | No |
| Delete a task | Yes | No |
| Clear all data, reload sample data, restore backup | Yes | No |
| Upload older local records to the shared database | Yes | No |
| Change the admin password | Yes | No |
| Reports, filters, exports, backup download | Yes | Yes |

The dashboard badge shows the current role: **Admin: all functions** or **User: add, edit, transfer**.

## 2. One-time setup (done by the dashboard owner and Istiyaque)

1. Open the dashboard link and sign in to Claude.
2. In the dashboard's share controls, add each person by the email of their Claude account:
   - **Istiyaque:** Editor (or Owner)
   - **Irfan, Ali, Sudheer, Adil:** Contributor
   - **Managers or site staff who only need to look:** Viewer
3. Ask everyone to open the link while signed in.
4. Check that the badge on the Dashboard reads **Shared database · live**. If it says **Local only**, the person is not signed in or cannot reach the shared database, and their entries will not be shared.
5. **Istiyaque goes first.** He selects **Istiyaque** under **I am** on the Dashboard. The dashboard asks him to create the admin password (at least 6 characters, entered twice). Choose a long password that is not used elsewhere.
6. Irfan, Ali, Sudheer and Adil each select their own name under **I am** (once per browser).
7. To try the system, Istiyaque clicks **Load sample data**. Sample records are labelled SAMPLE and can be deleted from the Task Register.

Do this in order. Until the password exists, the first Editor or Owner who selects **Istiyaque** gets to create it.

Do not copy the dashboard's HTML file to GitHub Pages or another website. A copy cannot use the shared database and will run in Local only mode.

## 3. Admin password

- **Unlocking:** selecting **Istiyaque** under **I am** asks for the password. The correct password turns on all admin functions. A wrong password leaves him as a user and he can try again with the **Unlock admin** button.
- **Locking:** admin functions stay on until the page is refreshed or someone selects another name under **I am**. After a refresh, he must enter the password again.
- **Changing it:** on **Settings & Backup**, the admin clicks **Change admin password**.
- **Requirements:** admin needs three things together: Editor or Owner access, **Istiyaque** selected under **I am**, and the correct password.
- **Lost password:** there is no reset button. Contact whoever maintains the dashboard to have the stored password cleared.

## 4. Daily routine for users

1. Open the dashboard and check that your name is selected under **I am**.
2. Click **+ Add New Task** for new work, or **Edit** on one of your tasks.
3. Enter the Input Data Received Date when the site team supplies data. Leave it blank to show *Awaiting Site Data*.
4. Enter the **Input Data Path** (where the site data is saved) and the **Output Data Path** (where the finished drawings or files are saved). Both are optional text fields.
5. Update Processing Status (%). Status becomes Pending at 0% and In Progress from 1% to 99%.
6. Choose **Incomplete** if the work is blocked (missing data, corrections needed) and write the reason in Remarks.
7. When the work is finished and checked, set Overall Status to **Completed** (needs 100%).

If you need a task deleted or copied, ask Istiyaque.

## 5. Daily routine for the admin

1. Open the dashboard, select **Istiyaque** and enter the password.
2. Check the Overdue, Due today and Awaiting Site Data warnings on the Dashboard.
3. Open **Daily / Range Reports** for the date, then print or export (PDF, Excel, CSV).
4. Chase the site team for any task awaiting input data.
5. Delete or copy records when needed (Del and Copy buttons appear only for the admin).
6. Download a JSON backup every week (section 8).

## 6. Transferring tasks when someone is absent

- **One task:** click **Transfer** on its row, choose who takes over, and optionally enter a reason (for example, "on leave until 25/10").
- **All open tasks:** open **Draughtsman-wise Work Status**, select the absent person's tab and click **Transfer all open tasks**. Completed tasks stay where they are.
- All details move with the task: progress, status, project, dates, description and remarks. A line recording the transfer is added to the remarks, and the row shows a "Transferred from [name]" badge.
- Users can transfer only their own tasks. If a person is absent and cannot transfer his tasks, Istiyaque does it for him.
- To review transfers, click the purple **Transferred** card on the Dashboard or the **Transferred** filter button. A Transfer details table lists the date, project, from, to, reason, progress and current owner.

## 7. Status and warning rules

- **Completed** is never set automatically. At 100% a task shows "100% – confirm completion" until someone confirms it.
- **Overdue** appears as a separate red badge when the deadline has passed and the task is not completed.
- Warnings are shown for: overdue tasks, due today, due within 2 days, awaiting site data, and no update for 3 or more days.
- Every record shows **by [name]** under Last Updated.
- **Input Data Path** and **Output Data Path** columns sit between Last Updated and Actions. They are plain text, not clickable links, because a web page cannot open folders on a computer or network drive. Copy the path and paste it into File Explorer. Use paths your whole team can reach, such as a shared network folder, rather than a personal drive.
- The paths are included in searches and in Excel, CSV and PDF exports, and they stay with a task when it is copied or transferred.
- Exports on **Export / Print** use the filters currently set and include the generation date. The browser asks you to confirm each file save.

## 8. Backup and recovery

- Istiyaque downloads a JSON backup from **Settings & Backup** at least weekly, and before any bulk change.
- To recover, Istiyaque uses **Restore from file**. This replaces all current records with the backup.
- Deleting a record asks for confirmation and cannot be undone, except from a backup.
- This repository is public. Do not commit backups or exports that contain real project data, and do not put real server or folder paths in this file.

## 9. Known limitations

- The role rules and the password are checked by the dashboard screen, not by the database. A user with Contributor access could still change data by other means, and the dashboard cannot stop that. For stricter control, give users Viewer access and have Istiyaque enter their updates.
- The password is stored as a salted hash in the shared database, which other staff with access can read. A short or common password could be guessed, so use a long one.
- "I am" is self-selected. Another person can choose **Istiyaque**, but admin functions stay off without Editor or Owner access and the password.
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
| No Copy or Del buttons | Expected for users. Only the unlocked admin has them |
| Istiyaque still sees "User" badge | Click **Unlock admin**, enter the password, and check he has Editor or Owner access |
| "Wrong password" | Try again. If the password is lost, see section 3 |
| "Admin needs Editor or Owner access" | The owner must change Istiyaque's access in the share controls |
| "Could not save to the shared database" | You have Viewer access. Ask the owner for Contributor access |
| Path will not open when clicked | Paths are plain text. Copy the path and paste it into File Explorer |
| Export does nothing | Accept the save prompt, and check the filters are not hiding all records |
