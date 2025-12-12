*******
- `Sysinternals` - Suite of Windows tools for diagnostics, troubleshooting, and management.
## Process Explorer
- "Task manager on steroids" - more detailed information about processes on system.
## Process Monitor
- Real-time process monitoring tool used to identify what a process is doing on a system level.
## ProcDump
- CLI utility to dump process memory.
	- **Reminder**: In an OS, each process is given its own isolated virtual memory space.

```powershell
# Create a dump 
procdump -c 20 [executable-name] c:\temp
```