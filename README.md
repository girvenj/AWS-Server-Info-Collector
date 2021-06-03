# AWS-Server-Info-Collector

A PowerShell script that collects Microsoft Windows and SQL Server information.  Additionally it also collects information on possible incompatibilities between a customer’s Microsoft SQL Server and Amazon RDS SQL.  Providing customers awareness on possible migration blocker to Amazon RDS SQL.  

This code **is as is**. It is not officially supported by Amazon AWS nor is Amazon AWS libel for any misuse of the code.  While the event it could cause an issue is unlikely.  It should be tested and reviewed prior to running in a production environment. 

# Examples:

**Run against local server**
`.\Invoke-SQLInfoReport.ps1 -ServerName 'Localhost' -ReportPath 'C:\Temp'`

**Run against multiple servers**
`.\Invoke-SQLInfoReport.ps1 -ServerName 'Server1', 'Server2' -ReportPath 'C:\Temp'`

**Load servers from a csv list**
`.\Invoke-SQLInfoReport.ps1 -ServerName (Get-Content -Path 'C:\Temp\Servers.csv') -ReportPath 'C:\Temp'`
