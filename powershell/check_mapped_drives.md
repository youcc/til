### Check mapped network drives in Windows 10
```
gwmi -Query 'Select * from Win32_NetworkConnection' | Select-Object LocalName, RemoteName, UserName, ConnectionState | Sort-Object LocalName | ft -auto
```