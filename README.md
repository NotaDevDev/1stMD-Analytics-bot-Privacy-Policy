# Privacy Policy for 1stMD Analytics Bot

**Effective date:** 13 September 2026  
**Last updated:** 19 September 2026

This policy explains how 1stMD Analytics Bot (the **Bot**) collects, uses, stores,
and discloses information when it is installed in a Discord server. The Bot is
operated by **NotaDevDev** (the **Operator**).

Server owners and administrators choose whether to install the Bot, which channels
and roles it covers, which optional modules are enabled, and who may view its
reports. Discord separately processes information under the
[Discord Privacy Policy](https://discord.com/privacy).

## Information we process

The Bot may process and store the following Discord data for servers where it is
installed:

- **Server and configuration data:** server IDs; channel, category, role, panel, and
  message IDs; configured timezone; enabled modules; analytics access roles; tracked
  roles and channels; saved report definitions and schedules; administrator-created
  labels; channel type, category placement and ordering; observed server-structure
  changes; alert delivery state; configuration history; and the user ID of an
  administrator who changes a setting.
- **Membership data:** user IDs, whether an account is a bot, join and departure
  times, role IDs, and the times at which observed role memberships begin and end.
- **Text activity metadata:** message IDs used to prevent duplicate counting,
  message timestamps, and per-user message counts grouped by server, channel, date,
  hour, and roles held at the time.
- **Voice activity metadata:** user and channel IDs, voice-session start and end
  times, roles held at the time, and observable Discord voice states such as AFK,
  mute, deafen, Stage speaker, or Stage audience status.
- **Scheduled-event data:** event IDs and names, associated channel IDs, scheduled
  and actual times, status, RSVP user IDs, and observed attendance metadata.
- **Command and moderation metadata:** command name, time bucket, outcome and
  duration; the invoking user's ID where needed for unique-user counts; and Discord
  audit-entry IDs, action types, moderator and target IDs, timestamps, and whether
  an action was automated.
- **Active ticket-claim data:** the claimant's Discord user ID, ticket or channel
  name, team, and claim timestamp for tickets that are currently claimed in the
  FirstMD logging system.
- **Operational data:** collection receipts, incomplete-coverage periods, health
  timestamps, bounded error codes, delivery attempts, and panel or counter state.

The Bot receives this information from Discord's Gateway and API, from settings
entered by authorized server administrators, and from a sanitized current-state
snapshot produced by the FirstMD logging bot from its configured Ticket Claims Sheet.
The Analytics Bot does not receive the Sheet's Google credentials.

## Information we do not collect

The Bot does **not** request, read, or store:

- message bodies or other message content;
- attachments, embeds, reactions, or polls;
- direct messages;
- voice audio, speech, or recordings;
- Discord presence or activity status;
- command arguments;
- email addresses, phone numbers, passwords, payment details, IP addresses, cookies,
  advertising identifiers, or precise location data.

The Bot counts that a message occurred. It cannot reconstruct the message from the
stored analytics record. Voice time means time connected to a voice or Stage channel;
it does not measure whether a person spoke, listened, or paid attention.

## How we use information

We use the information only to provide, secure, and maintain the Bot, including:

- member growth, joins, departures, and engagement measurements;
- text-channel and voice-channel activity totals and leaderboards;
- role-based and member-level analytics requested by authorized server staff;
- scheduled-event, command-usage, and moderation workload reports;
- current active-claim totals and team or member breakdowns;
- server statistics panels, scheduled reports, and configured counters;
- administrator-configured alerts when channels move between categories or their
  order changes;
- duplicate-event prevention, outage recovery, diagnostics, abuse prevention, and
  service reliability.

We do not use Discord data for advertising, data brokerage, credit, employment,
housing, insurance, or decisions based on protected characteristics. We do not sell
Discord data.

Where applicable law requires a lawful basis, the Operator processes this data to
provide the service requested by server owners and administrators and for the
legitimate interests of operating reliable, proportionate community analytics.
Individuals may object as described below.

## Who can see information

The normal server and active-claims panels contain aggregate statistics and are posted
only in channels or threads selected by a server administrator. Structure-change
alerts are also sent only to the administrator-configured staff destination. Detailed
member, role, channel, voice, claims, export, and moderation reports are restricted
using Discord permissions and the server's configured analytics roles. Some requested
reports are delivered as private Discord interaction responses.

Information is not shared between Discord servers. We may disclose information only:

- to Discord as needed to receive events and deliver commands, panels, and reports;
- to infrastructure and backup providers acting for the Operator and subject to
  access restrictions;
- when required by law or necessary to protect users, the service, or legal rights;
- when a user or authorized server administrator expressly directs us to do so.

## Storage, security, and international processing

Production data is stored in a dedicated PostgreSQL database on access-controlled
infrastructure. The database does not expose a public network port. The Bot uses
file-backed secrets, role-based report access, bounded queues and logs, health
monitoring, and encrypted backups. Access is limited to the Operator and people who
need it to operate or secure the service.

Discord, infrastructure providers, and the Operator may process information in
different countries. Where required, appropriate contractual or legal safeguards
will be used for international transfers.

No security measure can guarantee absolute protection. If an incident creates a
risk to Discord API data, the Operator will investigate it and provide legally
required notices to Discord and affected users.

## Retention

The Bot's user interface provides reports covering up to the previous **180 days**.
The current production service does not treat that reporting limit as an automatic
database-deletion deadline, so older metadata may remain while it is still needed to
operate the service, maintain historical membership and role attribution, resolve
data-quality issues, or comply with a verified request.

Incomplete setup drafts are deleted when setup is activated; otherwise they remain
until replaced or deleted with the server's data. Operational logs are size-limited
and rotate. The VDS retains encrypted managed backups for up to **2 days**;
independently transferred encrypted Windows backup history is retained for up to
**30 days**.

Active-claim analytics is a current-state feature. When a ticket is unclaimed and the
next valid snapshot is synchronized, that ticket is removed from active reports and
the active analytics database. The Bot retains the last successful snapshot during a
temporary Sheet or synchronization failure so an outage does not appear as a false
zero.

We delete or de-identify Discord API data when it is no longer needed for the Bot's
stated functions, when the service is discontinued, when Discord requires deletion,
or following a valid user or server-owner request, unless a legal obligation requires
limited continued retention. Removing the Bot stops new collection but does not by
itself immediately erase existing records; the server owner should submit a deletion
request.

After data is deleted from the active database, backup copies expire through the
retention cycles described above. If a backup must be restored for disaster recovery,
deletion requests completed after that backup was created will be reapplied.

## Your choices and rights

Depending on where you live, you may have rights to access, correct, delete, restrict,
or object to processing of your personal data, and to receive a portable copy. You
may also complain to your local data-protection authority.

To make a privacy request, contact **Deveire** privately on Discord (user ID
**`631393538592210965`**). Include your Discord user ID and the server ID concerned so
the correct records can be located. A server owner may request deletion of all data
associated with their server. Do not place Discord IDs or other personal information
in a public GitHub issue.

We may ask you to verify control of the relevant Discord account or authority over
the server. Verified requests will be handled promptly and normally within 30 days.
Some information may be provided in aggregated or redacted form where disclosure
would affect another person's rights, security, or privacy.

Server administrators can stop future collection by excluding channels, disabling
modules, or removing the Bot. Members may also contact their server administrators,
who can relay a request to the Operator.

## Children

The Bot is not directed to anyone below the minimum age required to use Discord in
their country. If you believe the Bot has processed data belonging to someone who
cannot lawfully use Discord, contact the Operator so it can be deleted.

## Changes to this policy

We may update this policy when the Bot's features, data practices, providers, or
legal obligations change. The date at the top will be updated, and material changes
will be communicated through an appropriate Discord or project channel where
practicable.

## Contact

- **Operator:** NotaDevDev
- **Privacy contact on Discord:** Deveire (`631393538592210965`)
- **Project:** <https://github.com/NotaDevDev/Server-Analytics-Bot>

This policy is intended to be consistent with the
[Discord Developer Terms of Service](https://support-dev.discord.com/hc/en-us/articles/8562894815383-Discord-Developer-Terms-of-Service)
and [Discord Developer Policy](https://support-dev.discord.com/hc/en-us/articles/8563934450327-Discord-Developer-Policy).
