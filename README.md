# Vayrone PostMaster

**The office mail server that keeps your company's email safe, complete and under your control.**
By [Vayrone Infratech](https://vayrone.com), Agra, India.

**[⬇ Download the latest Windows installer](https://github.com/akhiljha079/vayrone-postmaster-releases/releases/latest)** · Linux packages (.deb / .rpm) are on the same page under *Assets* · Licences and purchase: **[info@vayrone.com](mailto:info@vayrone.com)**

---

## What it is

Your company keeps its mailboxes at a provider (Zoho, Hostinger, GoDaddy, cPanel, Microsoft 365, …). Vayrone PostMaster runs on one server **inside your office**:

- It downloads every employee's mail from the provider into a local mailbox on your server.
- Employees use Outlook, Thunderbird, their phone or the built-in webmail with a **LAN password**. They never know the provider password.
- All outgoing mail leaves through one provider account, with each employee's own address as sender.
- Every message that comes in or goes out passes through PostMaster. It is checked, filtered, archived forever and can be reviewed by management.

It installs in minutes on Windows or Linux, sets itself up with a wizard and updates itself.

## How it helps your company

| Your concern | What PostMaster does |
|---|---|
| **Data leaks.** Staff sending company files to personal Gmail. | Per-user policy: mail to personal addresses only with a company address in CC, and then after approval. Otherwise it is not delivered, the user is told why, and management is alerted. |
| **Phishing and fake domains.** `examp1e.com` pretending to be you or your bank. | Look-alike sender domains are detected and marked **[SUSPICIOUS]**, and the admins are alerted at once. |
| **Lost mail.** Deleted by employees, or gone when someone leaves. | Every sent and received email is kept in the compliance archive **forever**. No user, rule or admin can delete it. Mail a user deletes in Outlook also stays on the server for 30 days. |
| **No oversight** of what leaves the company. | Observation mode, sensitive-word alerts, per-user allowed domains and blocked addresses. Each alert opens the whole email with the suspicious words highlighted. |
| **Passwords** of provider mailboxes known to every employee. | Provider passwords are entered once by the admin and stored encrypted. Employees only have a LAN password. |
| **Slow or unreliable internet.** | Colleagues mail each other inside the LAN instantly. Mail is read from the local server, and outgoing mail queues and retries on its own. |
| **Audits and disputes.** | Search the archive by person, date, sender, words, or by alert / warning flag. Export as MBOX or .eml, one folder per person (Received / Sent). Every view and export is logged. |
| **Viruses, spam and dangerous files.** | Built-in spam filter (or Rspamd), ClamAV virus scanning, blocked file types (also inside ZIPs) and a quarantine where nothing is lost. |
| **Server failure.** | Scheduled, verified, encrypted backups to USB, NAS or cloud (S3, Wasabi, Backblaze, FTP). Restore a user, a folder or the whole server. |

## Features

### Mail server for the office
- SMTP, IMAP and POP3 for Outlook, Thunderbird, Apple Mail and phones (STARTTLS / TLS). Mail programs never download the same message twice.
- Webmail with live updates: read, write, search, folders, junk / not junk, personal rules, auto-reply.
- Domains, users, aliases, distribution lists and groups. Quotas and per-user access (IMAP, POP3, SMTP, webmail).
- Instant delivery between colleagues inside the LAN.

### External mailboxes (provider accounts)
- Connect each employee's provider mailbox over IMAP (with instant push / IDLE) or POP3, with presets for common providers.
- Choose what to download: from the PostMaster start date, from a date for one mailbox, or **all mail on the server**.
- Leave mail at the provider, delete it after download, or keep it N days. Downloaded mail keeps its original date and time.
- Duplicates are suppressed, also after provider-side restores. Temporary login refusals by a provider are retried; only a real wrong password pauses a mailbox, with an alert.

### Outgoing mail
- One relay account for everyone, or per domain / per user, with a queue that retries for 3 days.
- **Too large?** The sender gets a plain-language email explaining how to make it smaller.

### Mail guard: company mail policies
- **Suspicious senders:** domains that imitate yours or your partners' (typos, look-alike letters, `yourname-support.com`) are tagged **[SUSPICIOUS]** and alerted.
- **Public mail domains:** alerts for mail to or from gmail, yahoo, rediffmail, outlook.com and others (editable list); optional **[EXTERNAL]** tag on incoming mail.
- **Personal addresses need a company CC** (per user): with CC, waits for approval; without, not delivered, with a policy notice to the user and an alert.
- **Sensitive words** in the subject, text or attachment names: an alert, with the email held for approval for users in observation mode.
- **Observation mode** (per user or for everyone): outgoing mail waits for admin approval. Approve or refuse in one click; the sender is kept informed.
- **Allowed send domains per user**: a user may send outside only to the domains you list.
- **Blocked addresses** (per user or for everyone): no mail to or from them. A message to several people still reaches the others; the sender is told who was left out, and management is warned.
- **Alerts** on the dashboard and by email. Click an alert to open the **whole email with the flagged words highlighted**.

### Compliance archive and retention
- Every sent and received email is archived and **kept forever**, read-only. Archiving cannot be switched off and nothing can delete from it.
- One folder per address (Received / Sent), even for people who have left. Full-text search, including attachment names, and Hindi text.
- Flagged mail is marked **red (alert)** or **amber (warning)**, sent and received alike, and can be filtered.
- Mail users delete from their Inbox stays on the server (hidden, outside their quota) for a configurable number of days.
- Mailbox retention rules (for example Inbox or Trash after 30 days). A clear overview shows how long each copy is kept.
- Export to MBOX or .eml ZIP; restore a message into any mailbox; legal hold; every access in the audit log.

### Rules, journaling and forwarding
- **Easy rules** in plain sentences: copy all mail of a person to a manager, copy mail from a client to accounts, forward while on leave, …
- Full mail rules (conditions on sender, recipient, subject, body, size, attachments, direction, time) and journaling. Forwarding loops are stopped automatically.

### Spam, viruses and attachments
- Built-in spam scoring or Rspamd; company-wide and personal allow / block lists. **Allowed (whitelisted) senders always reach the inbox.**
- ClamAV virus scanning, blocked attachment types (also inside ZIP files), and a quarantine with release / delete.

### Insight and monitoring
- Dashboard with alerts, outgoing queue, storage, sign-ins, and a **graph of sent and received mail per user and per day**.
- System health tiles (database, disk, queue, mailboxes, backups, certificate, load, licence), alert emails, and Prometheus / Zabbix metrics.

### Backups, security and updates
- Scheduled full and incremental backups to folder, USB, NAS, S3-compatible cloud or FTP, encrypted before upload and verified every night.
- Roles (super admin, admin, auditor), two-factor sign-in for admins, account lockout, IP restrictions, audit log, TLS certificates.
- **Signed automatic updates:** *Admin → Updates → Check now*. Every update package is signed and verified before it is installed.

## System requirements

| | Requirement |
|---|---|
| Windows | Windows Server 2016 / 2019 / 2022 / 2025, or Windows 10 / 11 Pro (64-bit) |
| Linux | Ubuntu 22.04 / 24.04, Debian 12, RHEL / AlmaLinux / Rocky Linux 9 (x86-64 or ARM64) |
| CPU and memory | 4 cores, 8 GB RAM for up to ~200 users; 8 cores, 16 GB for 500 users |
| Disk | SSD with about 1 GB per user per year, plus a second disk, NAS or cloud for backups |
| Network | A fixed LAN IP and a server name (for example `mail.company.local`) |
| Licence | A licence key from Vayrone Infratech. Without one, it runs a 30-day, 5-user evaluation. |

## Install

- **Windows:** download `VayronePostMaster-Setup-<version>.exe` from the [latest release](https://github.com/akhiljha079/vayrone-postmaster-releases/releases/latest), run it, then open `https://<server>/` and follow the setup wizard.
- **Linux:** download the `.deb` (Ubuntu / Debian) or `.rpm` (RHEL / Alma / Rocky) for your processor and install it with your package manager, then open `https://<server>/`.

Our technicians can also install and configure everything on site. Contact [info@vayrone.com](mailto:info@vayrone.com).

## Updates

Installed servers update themselves from this page: **Admin → Updates → Check now**. The release notes of every version are listed under [Releases](https://github.com/akhiljha079/vayrone-postmaster-releases/releases).

## About this repository

This repository contains only the signed installers, Linux packages and update files. *Source code (zip / tar.gz)* on a release contains only this README. Vayrone PostMaster is proprietary software © Vayrone Infratech.

**Licences, pricing, renewals and demos:** [info@vayrone.com](mailto:info@vayrone.com) · [vayrone.com](https://vayrone.com)
