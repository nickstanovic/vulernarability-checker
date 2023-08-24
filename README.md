# Vulnerability Checker

This PowerShell script checks for open ports on your machine and assesses them for potential vulnerabilities based on a predefined list of common exploit ports.

## Functionality

1. Lists all established TCP connections on the system.
2. Filters and displays unique ports with their corresponding Process Names, PIDs, and IP Addresses.
3. Highlights ports that are commonly associated with vulnerabilities.

## Commonly Checked Ports

The script specifically checks for the following ports:
- `21`: FTP
- `22`: SSH
- `23`: Telnet
- `25`: SMTP
- `80`: HTTP
- `110`: POP3
- `135`: MS RPC
- `139`: NetBIOS
- `445`: SMB
- `1433`: MS SQL
- `1521`: Oracle SQL
- `3050`: Firebird SQL
- `3306`: MySQL
- `3307`: MySQL (Encrypted Connections)
- `3351`: Pervasive PSQL
- `3389`: RDP
- `5900`: VNC Server (first display)
- `5000`: Sybase SQL Server
- `5432`: PostgreSQL
- `27017`: MongoDB

## Prerequisites

1. You need to have PowerShell installed.
2. It's recommended to run the script as an administrator to see all processes and ports without restrictions.

## Usage

1. Open PowerShell with elevated privileges (Run as Administrator).
2. Navigate to the directory containing the script.
3. Before running the script, you might need to bypass the default execution policy for the current session. You can do this by running:
```powershell
Set-ExecutionPolicy Bypass -Scope Process
```
This sets the execution policy to `Bypass` only for the current PowerShell session.

4. Run the script using the command:
```powershell
.\vulnerability-checker.ps1
```

5. Once you're done, you can close the PowerShell session or reset the execution policy using:
```powershell
Set-ExecutionPolicy Default -Scope Process
```

## Note

- The script is a basic security tool and should be used as a starting point for more comprehensive vulnerability assessments.
- Adjusting the execution policy can expose your system to risks. Always ensure you understand the implications of any commands you run.