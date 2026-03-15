# SMB Enumeration

List SMB shares:

```bash
smbclient -L //TARGET_IP -N
```

Discovered share:

```
anonymous
```

Connect to the share:

```bash
smbclient //TARGET_IP/anonymous
```

Download files recursively:

```bash
smbget -R smb://TARGET_IP/anonymous
```

Found file:

```
log.txt
```

This file contains information about SSH key generation and ProFTPD configuration.
