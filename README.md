waituntil
=========

```
waituntil 1.0.0

Usage: waituntil [-hv] [-r <ss>] <start_time> [<command> [<args>]]

Wait until a specified time.

Run <command> at that specified time if one is specified.
If not, simply exit with code 0.

The <start_time> must be in ISO 8601 '%H:%M:%S'
or '%Y-%m-%d %H:%M:%S' format. When the date is not
specified, today is used.

Time zone can be set with TZ environment variable.

Will try to locate Homebrew gdate (GNU date) on macOS.
If not present, will adapt to use BSD date, which has
less precision due to lack of millisecond output.

Examples:

	# Wait until 2022-07-07 10:00:00 local time then run echo:
	waituntil '2022-07-07 10:00:00' && echo Hi

	# Wait until 2022-07-07 10:00:00 Tokyo time then run echo:
	TZ=Asia/Tokyo waituntil '2022-07-07 10:00:00' && echo Hi

	# or
	TZ=Asia/Tokyo waituntil '2022-07-07 10:00:00' echo Hi

Available options:

	-h          Show this help screen.
	-r <ss>     Add random delay between 0 and <ss> seconds.
	-v          Show script name and version number.

```

### Running as _runat_

```
waituntil 1.0.0

Usage: runat [-hv] [-r <ss>] <start_time> <command> [<args>]

Wait until a specified time then run <command>.

The <start_time> must be in ISO 8601 '%H:%M:%S'
or '%Y-%m-%d %H:%M:%S' format. When the date is not
specified, today is used.

Time zone can be set with TZ environment variable.

Will try to locate Homebrew gdate (GNU date) on macOS.
If not present, will adapt to use BSD date, which has
less precision due to lack of millisecond output.

Examples:

	# Wait until 2022-07-07 10:00:00 local time then run echo:
	runat '2022-07-07 10:00:00' echo Hi

	# Wait until 2022-07-07 10:00:00 Tokyo time then run echo:
	TZ=Asia/Tokyo runat '2022-07-07 10:00:00' echo Hi

Available options:

	-h          Show this help screen.
	-r <ss>     Add random delay between 0 and <ss> seconds.
	-v          Show script name and version number.

```
