# Kape Commands

It is highly recommended to use gKAPE - the GUI frontend of KAPE.

```bash
# Obtain data from target source ONLY 
.\kape.exe --tsource C: --tdest C:\temp\tout --tflush --target !SANS_Triage

# Process data from target source ONLY
.\kape.exe --msource C:\temp\tout --mdest C:\temp\mout --mflush --module !EZParser --mef csv --debug

# Obtain and process data from target source
.\kape.exe --tsource C: --tdest C:\temp\tout --tflush --target !SANS_Triage --mdest C:\temp\mout -mflush --module !EZParser --mef csv --debug
```