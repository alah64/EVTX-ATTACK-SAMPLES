if your winlogbeat exists in c:\winlogbeat folder need to configure it and then setup default dashboards and ... by these commands:
```
cd c:\winlogbeat
./winlogbeat.exe setup -e
```

if you are running winlogbeat as a service you do not need to stop it.

then copy this project files into C:\EVTX-ATTACK-SAMPLES folder
after that need to change winlogbeat_example.yml in that folder or make another file in that folder by winlogbeat.yml name.
then run powershell as administrator and run below commands in it:

```
del C:\EVTX-ATTACK-SAMPLES\winlogbeat\*
cd C:\EVTX-ATTACK-SAMPLES\
.\Winlogbeat-Bulk-Read.ps1 -Exe c:\winlogbeat\winlogbeat.exe -Source "..\EVTX-ATTACK-SAMPLES\"
```
