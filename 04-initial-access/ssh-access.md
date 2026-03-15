# SSH Access

After mounting the NFS share, the private key was retrieved from:

```
/mnt/kenobi/tmp/id_rsa
```

Fix file permissions:

```bash
chmod 600 id_rsa
```

Login using SSH key:

```bash
ssh -i id_rsa kenobi@TARGET_IP
```
