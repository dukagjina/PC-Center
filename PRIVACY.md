# PC Center privacy information

Applies to PC Center 0.14.9 distributed through GitHub. Updated October 24, 2026.

PC Center reads hardware measurements, Windows health signals, installed apps,
startup entries and services to show them to you. File tools inspect the files
you select or the scan scope you choose. This processing takes place on your
PC. PC Center has no advertising SDK, usage analytics uploader or automatic
crash-report uploader. It does not upload your scanned files or inventory to
the developer.

## Local storage

Profiles, window placement and the change journal are stored under your
Windows user profile. App update metadata/downloads use local application
data. The installed service stores operational logs, repair history and
configuration backups under ProgramData. Those records can include file
paths, application names and diagnostic output. Review logs before sharing
them. Windows, backup tools and any synchronization services you configure
may separately process local data.

Startup inventory comparisons retain a local baseline and up to 100 changes,
including startup names and command lines. The optional watch runs only while
PC Center is open. Storage Explorer scans filesystem metadata without opening
file contents. Its detailed results remain in memory until replaced or the app
closes. Up to 48 complete scan summaries (within a 4 MiB limit), including root and top-folder
paths, file counts, filesystem root identity and logical byte totals, are saved
locally in `storage-history.json`. You can remove those records with Clear
history in Storage Explorer. Partial or cancelled scans are not saved as baselines.
Process activity and network endpoint inventories are displayed locally and
are not uploaded. Context-menu visibility changes retain their original
values in the local change journal for undo. Scheduled-task commands, recorded startup
events and driver/disk inventories are shown locally and are not uploaded.

Uninstall removes the program and service. User settings and diagnostic or
recovery records may remain so that removal does not silently destroy your
saved configuration or recovery information.

PC Center offers optional machine-wide application traffic accounting. It is
off until explicitly started. Windows TCP/UDP events are aggregated into app
names, hashed executable-path identities and byte totals. Packet contents,
remote addresses and full executable paths are not saved by this collector.
Daily totals are retained for seven days, with bounded per-day app records;
history is visible to local PC Center users. Collection normally expires within
45 seconds after the app stops renewing its lease. The optional background mode
continues after the window closes until stopped or the service restarts. Clear
history is available while collection is stopped.

Browser extension inventory reads saved profile preferences, extension manifests
and declared permissions locally. It does not upload those records or alter
browser settings. Browser-native management pages run only when selected.

Delayed startup stores original commands and creates limited, current-user
sign-in tasks. Firewall reset exports the current policy to the protected
service data directory before resetting rules. CPU sensor providers already installed on the PC may have
their own data practices; PC Center does not install them automatically.

## Online connections

- PC Center automatically checks its official GitHub release feed. Successful
  checks are cached for 24 hours; unsuccessful checks may retry after five
  minutes. You can also request a check through the application update controls. An app update
  is downloaded and installed only after you choose it.
- Driver checks use Windows Update. Software checks use WinGet and its
  configured sources. User-approved update installations may contact Microsoft
  and the relevant software publisher.

These services receive connection information, including your IP address,
and may process request information under their own policies. PC Center does
not control their retention practices. Native Windows repair and update
tools may make connections according to your Windows configuration.

## Support information

PC Center has no in-app About popup or automatic diagnostic-report submission.
If you share screenshots or local log files with support, review them first;
they may contain device details or file paths. Nothing is sent automatically.

For privacy questions, use the project's
[issue tracker](https://github.com/dukagjina/PC-Center/issues). Issues are public;
do not include private logs, identifying information, secrets or passwords.

## Microsoft WebView2 Runtime

The GitHub installer requires Microsoft Edge WebView2 Runtime to be installed already. It does not bundle or automatically download that runtime. If it is missing, setup directs you to Microsoft's download page. WebView2 is a Microsoft component with its own update and diagnostic behavior, governed by Microsoft's settings and [privacy statement](https://privacy.microsoft.com/privacystatement). Its presence does not mean PC Center uploads the local files or inventories
described above. The shared runtime may remain installed after PC Center is
removed because other applications can use it.

## Personal files and disk tools

Backup and deleted-file recovery run locally. No file contents are uploaded. Backup manifests contain local source paths, file names, sizes, modification times and checksums; the backup is not encrypted. Disk and file result reports remain in the current application session; backup omissions are also saved in backup.json.

Recovery folders also retain durable reports containing source/destination
paths, file names, checksums and recovery results. Partition reconstruction saves
the replaced table sectors and a report containing the physical disk identity
and serial number. ReFS salvage keeps Windows scan data and recovered files.
These outputs may reveal private file names even when recovery is incomplete;
they stay in the destination you select and are not uploaded automatically.
EFS recovery preserves Windows encryption metadata and encrypted contents;
it does not export the user's private encryption key or decrypt files without it.
Startup-check ownership is recorded locally in the Windows registry, and the
check itself is recorded in the Windows event log. Exported reports stay at the
location you choose and should be reviewed before you share them.

## PC checkup reports

PC checkup keeps up to five local reports in your PC Center user-data folder.
Reports can include cleanup category totals, sample filenames, startup names and
commands, drive identifiers, activity measurements, and verification outcomes.
They are used to show results and restore supported startup settings. They are
not uploaded by PC Center. Save report exports a copy only to the location you
choose; review its contents before sharing it.
