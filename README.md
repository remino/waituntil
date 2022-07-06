waituntil
=========

```
Usage: waituntil [options] start_time

Wait until a specified time.

Start time must be in ISO 8601 '%Y-%m-%d %H:%M:%S' format.

Time zone can be set with TZ environment variable.

Will try to locate Homebrew gdate (GNU date) on macOS.
If not present, will adapt to use BSD date, which has
less precision due to lack of millisecond output.

Examples:

	# Wait until 2022-07-07 10:00:00 local time then run echo:
	waituntil '2022-07-07 10:00:00' && echo Hi

	# Wait until 2022-07-07 10:00:00 Tokyo time then run echo:
	TZ=Asia/Tokyo waituntil '2022-07-07 10:00:00' && echo Hi

Available options:

	-h        Show this help screen.
```

