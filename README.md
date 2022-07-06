runat
=====

```
Usage: runat [options] start_time command

Run specified command at the specified time.

Start time must be in ISO 8601 '%Y-%m-%d %H:%M:%S' format.

Time zone can be set with TZ environment variable.

Will try to locate Homebrew gdate (GNU date) on macOS.
If not present, will adapt to use BSD date, which has
less precision due to lack of millisecond output.

Examples:

	# Run echo on 2022-07-07 10:00:00 local time:
	runat '2022-07-07 10:00:00' echo Hi

	# Run echo on 2022-07-07 10:00:00 in Tokyo time:
	TZ=Asia/Tokyo runat '2022-07-07 10:00:00' echo Hi

Available options:

	-h        Show this help screen.
```

