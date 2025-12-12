*******
- `Chainsaw` - An advanced, high-speed log parsing program.
	- Takes advantage of [Sigma](https://github.com/SigmaHQ/sigma) rules for threat hunting.
	- `Sigma` - a SIEM-agnostic set of rules that embody behaviors of threat actors.
	- Parses through `EVTX` files - Windows proprietary binary log file format.
## CLI Commands

```bash
# Search Operation
# Mimikatz is the string to be matched
# -i: case insensitive flag
# Logs: C:\Users\Username\LogFiles\
.\chainsaw.exe search mimikatz -i C:\Users\Username\LogFiles\

# Hunt Operation
# -s: Ruleset to be utilized.
# --mapping: Identify log fields correctly.
# --level: Identify severity of log.
.\chainsaw.exe hunt C:\Users\Username\LogFiles\ -s .\sigma\ --mapping mappings/sigma-event-logs-all.yml --level critical

# Dump Operation
# -o: Output file
.\chainsaw.exe dump C:\Users\Username\LogFiles\ -o C:\Users\Username\dump.csv
```