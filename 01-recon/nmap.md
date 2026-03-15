# Nmap Scan

Initial scan to identify open ports and services.

```bash
nmap -sV -sC TARGET_IP
```

## Open Ports

| Port | Service |
| ---- | ------- |
| 21   | FTP     |
| 22   | SSH     |
| 111  | RPC     |
| 139  | SMB     |
| 445  | SMB     |

These services will be further enumerated.
