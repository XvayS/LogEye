<div align="center">
    <img src="https://apps.soldat2d.com/projects/logeye/logo/48x48.png">
</div>

# LogEye

## About

**LogEye** is an IP/HWID tracking tool for [Soldat](https://github.com/Soldat/soldat) that works with ARSSE/BakaAdmin/SoldatServer logs<sup>*</sup>.

_<sup>*</sup> ARSSE dev. version 1.2.9 or newer_

This application is similar to [iFrag's ARSSE IP Tracker](http://forums.soldat.pl/index.php?topic=32729.0). In fact I started writting it before I saw iFrag's work :)


## How does it work

It scans log files and creates a database file based on scanned items.

For further work it reads the database file created earlier, not the logs files.

## Features

- Search by Player's IP, HWID, Name, Server, Date
- Search using glob patterns (wildcards)
- Update database files with unique entries only<sup>*</sup>

_<sup>*</sup> You'd need to select an existing database file while saving scanning results and hit the "Update" button_

## Interface

### Main window

![numeric references](https://apps.soldat2d.com/projects/logeye/screenshots/numeric_references.png)
![Main window screenshot](https://apps.soldat2d.com/projects/logeye/screenshots/v0300_1_windows.png)

Button              | Description
------------------- | -------------------
| 1. "Open"         | Open a saved database file
| 2. "Save"         | Export search results as Txt or HTML<sup>*</sup>
| 3. "Scan"         | Show the scanning menu (ARSSE/Baka Admin/SoldatServer)
| 4. "QuickUpdate"  | Run the database QuickUpdate function
| 5. "Stop"         | Stop the scanning process (enabled while scanning only)
| 6. "Settings"     | Show the settings menu
| 7. "Help"         | Show wildcards manual
| 8. "About"        | Show application information

_<sup>*</sup> You could customize both Txt & HTML output formats in the settings file (LogEye.ini)_

### Update/Replace dialog

![Update/Replace dialog screenshot](https://apps.soldat2d.com/projects/logeye/screenshots/v0300_2_windows.png)

In case of saving a database file with the name of the existing one, you will be able to choose an action:
- "Update" - to update selected database file with the new unique entries from the log files
- "Replace" - to replace (rewrite) the file and create a new database

### Servers dialog

![Servers dialog screenshot](https://apps.soldat2d.com/projects/logeye/screenshots/v0300_3_windows.png)

You are able to change server names and exclude servers (folders) from scanning before the scanning process begins.

### QuickUpdate settings dialog

![QuickUpdate settings dialog screenshot](https://apps.soldat2d.com/projects/logeye/screenshots/v0300_4_windows.png)

QuickUpdate is an easy way to update your database with only one click.
To set up the QuickUpdate options for the first time click on the "QuickUpdate" button or use "Settings" menu to access the options dialog again.
You are able to set the default scanning path and the last update date<sup>*</sup> for both ARSSE and SoldatServer logs.

_<sup>*</sup> Date automatically alters while updating_

> Note: As it's a "quick" update, you are not able to change server names and/or exclude some of them from scanning. For example: If you have logs from the same server in ARSSE and SoldatServer format and want them to auto-merge together with QuickUpdate, then folder names with log files of both types must be the same.

## Step by step manual

1. Creating database files:

    - Click "Scan" button and select ARSSE/BakaAdmin/SoldatServer item from the popup menu
    - Select log files directory (if you select a folder with no log files in it, program will try to find logs in first-level subfolders)
    - Select path/file name for saving scanned data

1. Updating database files:

    - Click "Scan" button and select ARSSE/BakaAdmin/SoldatServer item from the popup menu
    - Select log files directory (if you select a folder with no log files in it, program will try to find logs in first-level subfolders)
    - Select file name of the existing database file you want to update
    - Click "Update" button in Update/Replace dialog

1. Searching:

    - Click "Open" button and select previously saved database file<sup>*</sup>
    - Fill search fields (IP, HWID, Name, Server, Date) and click "Search" button or press the `[Enter]` key

    _<sup>*</sup> Database opens automatically after scanning finished_

## Additional functions

1. Double click the cell to use its value as a search parameter

1. Right click on the row in results list to show the context menu:

   - Copy IP/HWID/Name/Server/Date&Time
   - Copy entire row
   - WhoIs lookup<sup>*</sup>
   
   _<sup>*</sup> WhoIs service URL can be changed in the settings file (LogEye.ini)_

## Wildcards manual

Wildcards can substitute for one or more characters when searching for data in a database. The following wildcards can be used:

Value           | Description 
--------------- | ---------------
`*`             | Substitutes zero or more characters
`?`             | Substitutes any one character
`[charlist]`    | Substitutes one character from a group. A group can be a list of characters, e.g. `[abcd]`, or a range of characters, e.g. `[a-d]` which is the same as `[abcd]`
`[^charlist]`   | Substitutes any single character NOT in the group, e.g. `[^a-zA-Z0-9]` substitutes any character that is NOT alphanumeric

> Tip: Use `[charlist]` to substitute `*`,  `?` and `[` characters, e.g. `[*]` for `*`

## Command line switches

Value               | Description 
------------------- | -------------------
`/db <path>`        | Use to load the specified database on application startup
`/upd`              | Use with the `/db` switch to update the loaded database
`/ip <ip>`          | Use with the `/db` switch to search by IP
`/hwid <hwid>`      | Use with the `/db` switch to search by HWID
`/serv <server>`    | Use with the `/db` switch to search by Server
`/date <date>`      | Use with the `/db` switch to search by Date
`/silent`           | Use with the `/upd` switch to run database update in a silent mode, without the GUI
`/debug`            | For debugging purpose only
`/help`             | To show this help

> Tip: You could use either `/` or `-` symbol to prefix command line switches

Examples:

```bat
LogEye.exe /db servers.db
```

```bat
LogEye.exe /db "D:\Games\SoldatServer\Logs\Big Brother Is Watching You.db" /upd
```

```bat
LogEye.exe /db data.db /upd /silent
```

```bat
LogEye.exe /db MyDatabase.db /upd /date "2015-05" /serv "MyServ"
```

## Changelog

See [CHANGELOG.md](CHANGELOG.md) for details.

## Discussion

See the post on [forums.soldat.pl](https://forums.soldat.pl/index.php?topic=34125.0).
