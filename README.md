# force_drive

A personal productivity log. Work is measured in **units**: a unit is
whatever you could get done in about an hour of relaxed effort. Some
units take 25 minutes, some take two of them to fill an hour — the
unit tracks scope, not the clock.

Goalposts:

- **8 units** in a day = a good day
- **16+ units** = an incredible day

## Usage

```
./track add <category> "<note>" [-u UNITS]   # log a completed unit (default 1)
./track today                                 # today's entries + total
./track undo                                  # remove the last entry logged today
./track report [-d DAYS]                      # summary over the last N days (default 7)
./track categories                            # all-time totals by category
```

Examples:

```
./track add laundromat-work "folded and sorted inventory"
./track add fundraiser "called 5 potential sponsors" -u 2
./track add surveillance-system "wired up second camera" -u 0.5
./track today
./track report -d 30
```

Categories are free-form strings — use whatever fits (e.g.
`laundromat-work`, `fundraiser`, `surveillance-system`).

## Storage

Each day's entries live in `logs/YYYY-MM-DD.csv`. Commit these as you
go so the git history doubles as a dated record of your work.
