- `KAPE` - Kroll Artifact Parser and Extractor.
	- Forensic tool to quickly gather evidence from computers.
- It is highly recommended to use `gKAPE` - the GUI frontend of KAPE.
## Modules
-  KAPE modules are instruction sets on how to process digital artifacts.
	- Modules are written in YAML and stored with the extension `.mkape`
	- All modules are recognized and available under `KAPE/Modules`
	- Any disabled modules are stored in the `!Disabled` folder
## Targets
- KAPE targets are instruction sets on what files and directories to collect upon.
	- Targets are written in YAML and stored with the extension `.tkape`
	- All targets are recognized and available under `KAPE/Targets`
	- Any disabled targets are stored in the `!Disabled` folder
## CLI Commands

```bash
# Obtain data from target source ONLY 
.\kape.exe --tsource C: --tdest C:\temp\tout --tflush --target !SANS_Triage

# Process data from target source ONLY
.\kape.exe --msource C:\temp\tout --mdest C:\temp\mout --mflush --module !EZParser --mef csv --debug

# Obtain and process data from target source
.\kape.exe --tsource C: --tdest C:\temp\tout --tflush --target !SANS_Triage --mdest C:\temp\mout -mflush --module !EZParser --mef csv --debug
```