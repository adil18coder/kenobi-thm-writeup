# NFS Enumeration

RPC services were discovered on port 111.

Enumerate NFS mounts:

```bash
nmap -p 111 --script=nfs-showmount TARGET_IP
```

Discovered mount:

```
/var
```

Mount the share locally:

```bash
mkdir /mnt/kenobi
mount TARGET_IP:/var /mnt/kenobi
```
