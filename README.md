# Draughtsmen Daily Status Dashboard: Setup Guide (Login Version)

Survey / Drafting Division. Admin: Istiyaque. Users: Irfan, Ali, Sudheer, Adil.

**Dashboard link:** https://claude.ai/artifact/Kune9G8TrCZMhWwNhBGLex

**Quick start:** sign in to Claude, open the link, check the badge says "Shared database · live" after login, then log in with your name and password. If the link gives an access error, ask Istiyaque or the dashboard owner to share it with your Claude account.

This dashboard has its own database. It is separate from any other copy of the dashboard, so tasks, logins and passwords are not shared between copies.

## 1. Roles at a glance

|  | Admin (Istiyaque) | Users (Irfan, Ali, Sudheer, Adil) |
| --- | --- | --- |
| See tasks and status | All users | Own tasks only |
| Reports, charts, filters, exports | All users | Own tasks only |
| Add tasks | For anyone | For themselves only |
| Edit tasks | Any task | Own tasks only |
| Transfer tasks | Any task, or all open tasks of one person | Own tasks only, to any other user or to the admin |
| Copy a task | Yes | No |
| Delete a task | Yes | No |
| Create or reset user logins | Yes | No |
| Change admin password | Yes | No |
| Clear all data, reload sample data, restore backup | Yes | No |
| Download backup | All tasks | Own tasks |

After login, the badge shows **Admin: all users** or **Logged in: \[name\] (own tasks only)**.

## 2. One-time setup

Do these steps in order.

### Step 1. Share the dashboard

Open the link while signed in to Claude, then add each person in the dashboard's share controls using their Claude account email:

- **Istiyaque:** Editor (or Owner). This is required for admin functions.
- **Irfan, Ali, Sudheer, Adil:** Contributor.
- **Managers or site staff who only need to look:** Viewer.

Everyone must be signed in to Claude when they open the link.

### Step 2. Create the admin password (Istiyaque)

1. Open the link. The sign-in screen appears.
2. Click **First-time admin setup** at the bottom of the sign-in card.
3. Enter the admin password twice (at least 6 characters). Use a long password that is not used anywhere else.
4. You are now logged in as admin.

If an admin password already exists, this button shows a message and does nothing. Log in normally instead.

### Step 3. Create a login for each user (Istiyaque)

1. Go to **Settings & Backup**.
2. Click **Set / reset user logins**.
3. Choose a user, enter a password (at least 6 characters) and click **Save**.
4. Repeat for Irfan, Ali, Sudheer and Adil.
5. Give each person their password privately (in person or by a private message, never in a group chat or in this repository).

### Step 4. First login for users

1. Open the link while signed in to Claude.
2. Select your name, enter your password and click **Log in**.
3. Check that the badge reads **Logged in: \[your name\] (own tasks only)**.

### Step 5. Optional test

Istiyaque can click **Load sample data** (visible to the admin while the dashboard is empty) to try the system. Sample records are labelled SAMPLE and can be deleted from the Task Register or removed with **Clear all data**.

Do not copy the dashboard's HTML file to GitHub Pages or another website. A copy cannot use the shared database.

## 3. Logging in and out

- Log in with your name and password each time you open or refresh the page. The login does not stay saved.
- Click **Log out** on the Dashboard before leaving a shared computer.
- Users cannot change their own password. If you forget it, ask Istiyaque to reset it using **Set / reset user logins**.
- The admin changes the admin password on **Settings & Backup** with **Change admin password**.
- There is no reset for a lost admin password. Contact whoever maintains the dashboard to have the stored admin password cleared.
- Admin login needs three things together: Editor or Owner access, the name **Istiyaque**, and the correct password.

## 4. Daily routine for users

1. Open the dashboard and log in.
2. Click **+ Add New Task** for new work, or **Edit** on one of your tasks.
3. Enter the Input Data Received Date when the site team supplies data. Leave it blank to show *Awaiting Site Data*.
4. Enter the **Input Data Path** (where site data is saved) and the **Output Data Path** (where finished drawings or files are saved). Both are optional text fields.
5. Update Processing Status (%). Status becomes Pending at 0% and In Progress from 1% to 99%.
6. Choose **Incomplete** if the work is blocked (missing data, corrections needed) and write the reason in Remarks.
7. When the work is finished and checked, set Overall Status to **Completed** (needs 100%).

If you need a task copied or deleted, ask Istiyaque.

## 5. Daily routine for the admin

1. Open the dashboard and log in as Istiyaque.
2. Check the Overdue, Due today and Awaiting Site Data warnings on the Dashboard. They cover all users.
3. Open **Draughtsman-wise Work Status** to review one person at a time.
4. Open **Daily / Range Reports** for the date, then print or export (PDF, Excel, CSV).
5. Chase the site team for any task awaiting input data.
6. Copy or delete records when needed (Copy and Del buttons appear only for the admin).
7. Download a JSON backup every week (section 9).

## 6. Transferring tasks

- **One task:** click **Transfer** on its row, choose who takes over (any other user or the admin), and optionally enter a reason, for example "on leave until 25/10".
- **All open tasks:** open **Draughtsman-wise Work Status**, click **Transfer all open tasks**. Users can do this only for their own tasks. The admin can do it for anyone. Completed tasks stay where they are.
- All details move with the task: progress, status, project, dates, description, remarks and paths. A line recording the transfer is added to the remarks, and the row shows a "Transferred from \[name\]" badge.
- After a transfer, the task disappears from the sender's list and appears in the receiver's list.
- To review transfers, use the purple **Transferred** card on the Dashboard or the **Transferred** filter button. The Transfer details table shows date, project, from, to, reason, progress and current owner.
- If someone is absent and cannot transfer their tasks, Istiyaque does it for them.

## 7. Who changed a task

The **Last Updated** column shows the date and time, with a yellow **by \[name\]** badge. The name is the person logged in when the task was saved, edited, copied or transferred. For a transfer, the badge shows who made the transfer, not who received it.

Tasks that were saved before this feature was added show no badge until they are edited again.

## 8. Status and warning rules

- **Completed** is never set automatically. At 100% a task shows "100% – confirm completion" until someone confirms it.
- **Overdue** appears as a red badge when the deadline has passed and the task is not completed.
- Warnings are shown for: overdue tasks, due today, due within 2 days, awaiting site data, and no update for 3 or more days.
- **Input Data Path** and **Output Data Path** are plain text, not clickable links, because a web page cannot open folders on a computer or network drive. Copy the path and paste it into File Explorer. Use paths the whole team can reach, such as a shared network folder, rather than a personal drive.
- The paths are included in searches and in Excel, CSV and PDF exports, and stay with a task when it is copied or transferred.
- Exports on **Export / Print** use the filters currently set, cover only the tasks you are allowed to see, and include the generation date. The browser asks you to confirm each file save.

## 9. Backup and recovery

- Istiyaque downloads a JSON backup from **Settings & Backup** at least weekly, and before any bulk change. The admin backup contains all tasks.
- Users can download a JSON file of their own tasks from **Settings & Backup** (My account).
- To recover, Istiyaque uses **Restore from file**. This replaces all current records with the backup.
- Deleting a record asks for confirmation and cannot be undone, except from a backup.
- User logins and the admin password are not part of the backup. After any rebuild of the dashboard, create them again.
- If this guide is stored in a public repository, do not commit backups, exports, passwords, or real project data or folder paths.

## 10. Known limitations

- "Own tasks only" is enforced by the dashboard screen, not by the database. A technically skilled Contributor could still read other tasks by other means. For strict secrecy, give users Viewer access and have Istiyaque enter their updates.
- Passwords are stored as salted hashes in the shared database. Anyone with access to the dashboard can read the stored hashes, so a short or common password could be guessed. Use long passwords.
- Only an Editor or Owner can write logins and the admin password, so a Contributor cannot overwrite them. This is also why users cannot change their own password.
- Logins are not tied to Claude accounts. Anyone with a user's password can log in as that user from any account that can open the dashboard.
- There is no full change history, only the last editor, the time and the transfer log.
- Data lives inside the dashboard. If the dashboard is deleted, the data goes with it, so keep backups.
- Everyone needs a Claude account to open the dashboard.
- A company database (PostgreSQL, MySQL, SQLite) with login-based roles would need a separate backend and developer time.

## 11. Troubleshooting

| Problem | Fix |
| --- | --- |
| Sign-in screen does not appear, badge says Local only | Sign in to Claude and reopen the link |
| Access error when opening the link | Ask the owner to share the dashboard with your Claude account |
| "No login has been set for \[name\]" | Ask Istiyaque to create it in Settings & Backup, Set / reset user logins |
| "Wrong name or password" | Check the name and password and try again. If forgotten, ask Istiyaque to reset it |
| "Admin needs Editor or Owner access" | The owner must change Istiyaque's access in the share controls |
| First-time admin setup says a password already exists | Log in as Istiyaque with that password |
| "This task belongs to \[name\]" message | Users can change only their own tasks. Ask Istiyaque |
| No Copy or Del buttons | Expected for users. Only the admin has them |
| "Could not save to the shared database" | You have Viewer access. Ask the owner for Contributor access |
| A transferred task vanished from my list | Expected. It now belongs to the receiver. The Transferred filter shows the record |
| No "by \[name\]" badge on an old task | The task was saved before the feature existed. Edit it once to add the badge |
| Path will not open when clicked | Paths are plain text. Copy the path and paste it into File Explorer |
| Export does nothing | Accept the save prompt, and check the filters are not hiding all records |
