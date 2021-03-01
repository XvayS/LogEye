 Version    | Notes
----------- | -----------
| v0.3.0    | **02 May 2015**
|           | + Added native Linux binaries (32/64-bit versions)
|           | + Added open database file via Drag&Drop onto LogEye executable in Explorer _[Windows]_
|           | - Removed deprecated MSAC GUIDs support
|           | ~ GUI controls glitches (reported by Bistoufly) _[Windows]_
|           | % Modified database structure (based on Prodigyx' suggestions)
|           | % Modified database format validation (checking for SQLite3 header now)
|           | % Modified `[Alt + 1..5]` and `[Alt + X]` shortcuts to `[Ctrl + 1..5]` and `[Ctrl + X]`
|           | % Modified icons set
| v0.2.0    | **22 Feb 2013**
|           | + Added 64-bit version
|           | + Added BakaAdmin logs support
|           | + Added Drag&Drop support for database open function
|           | + Added infotips for a toolbar buttons
|           | + Added keyboard shortcuts for a toolbar buttons
|           | + Added shortcut `[Alt + X]` for reseting all search fields
|           | + Added proper GUI resizing
|           | + Added restore window position feature
|           | % Modified search results sorting (made it bi-directional)
|           | % Modified log files detection algorithm
|           | ~ Fixed search results sorting bug with an empty results list
|           | ~ Fixed bug when manually disabled servers were processed incorrectly
|           | ~ Fixed bug with behaviour of Uncheck all option in servers list context menu
| v0.1.60   | **26 Oct 2011**
|           | + Added HWID field (based on Hardware Identifiers from SoldatServer 2.7.0 and above)
|           | + Added `hwid <hwid>` command line switch and `%hwid` export format placeholder
|           | + Added shortcuts for search fields focusing (`[Alt + 1]` for IP, `[Alt + 2]` for HWID, etc.)
|           | % Modified parser to work with Soldat 1.6.0+ (ARSSE/SoldatServer) logs
| v0.1.55   | **15 Jun 2011**
|           | + Added `help`, `ip <ip>`, `guid <guid>`, `serv <server>`, `date <date>` command line switches
|           | ~ Fixed search results sorting bug
|           | % Modified WhoisURL setting (new export format placeholders could be used in addition to the `%ip`)
|           | % Modified MSAC GUIDs parser (to support both new and old formats)
| v0.1.53   | **10 May 2011**
|           | + Added search results export feature (customizable Txt & HTML formats)
|           | + Added search results sorting feature
|           | ~ Fixed search by GUID case sensitivity bug (made insensitive)
|           | ~ Fixed few GUI bugs
|           | % Modified minor GUI settings
| v0.1.51   | **13 Mar 2011**
|           | + Added `silent` command line switch
|           | ~ Fixed QuickUpdate settings save bug
|           | % Modified MSAC GUIDs parser (to support both new and old formats)
| v0.1.50   | **02 Mar 2011**
|           | + Added an application auto update feature
|           | ~ Fixed a few bugs
|           | % Modified minor GUI settings
| v0.1.48   | **27 Feb 2011**
|           | + Added database QuickUpdate feature
|           | + Added command line switches
|           | ~ Fixed a few bugs
| v0.1.46   | **16 Feb 2011**
|           | + Added GUID field (based on MSAC's Globally Unique IDs for SoldatServer 2.6.5)
|           | + Added context menu for the results list
|           | ~ Fixed Unicode support bug
|           | ~ Fixed search by Name with "Case sensitive" option enabled bug
|           | ~ Fixed search by Date with "Use wildcards" option disabled bug
|           | % Modified INI settings
|           | % Modified GUI settings
| v0.1.45   | **08 Feb 2011**
|           | % Modified database format (switched to SQLite)
|           | * Code has been rewritten. Next changelogs will use this version as their base
| v0.0.36   | **28 Jun 2009**
|           | % Modified minor GUI settings
| v0.0.35   | **27 Jun 2009**
|           | + Added ARSSE logs support
|           | + Added "Use wildcards" as an option
|           | ~ Fixed minor GUI bug
|           | % Modified minor GUI settings
| v0.0.34   | **03 Apr 2009**
|           | ~ Fixed default open/save paths bug
|           | % Modified minor GUI settings
| v0.0.33   | **02 Apr 2009**
|           | * First public beta

> Note: `+` Added feature, `-` Removed feature, `~` Fixed feature, `%` Modified feature, `*` Comment
