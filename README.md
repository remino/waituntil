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

## Migrating from `runat`

If you're migrating from [`runat`](https://github.com/remino/runat), keep in mind while it runs commands itself like `watch`, `waituntil` works more like `sleep`.

This way, it is easier to chain complex commands after `waituntil` than with `runat`.

Example:

```sh
waituntil '2022-07-07 10:00:00' && echo Hi
# is the equivalent of
runat '2022-07-07 10:00:00' echo Hi
```

