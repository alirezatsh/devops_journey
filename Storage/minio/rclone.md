# Rclone - Commands Reference

## Installation and Configuration

### Linux/macOS

```bash

curl https://rclone.org/install.sh | sudo bash
rclone --version
rclone config

```

## Remote Commands

Manage remote connections to cloud storage services.

```bash

rclone listremotes
rclone config show <REMOTE_NAME>
rclone config delete <REMOTE_NAME>
rclone about <REMOTE_NAME>:


```

## Bucket / Storage Commands

Manage buckets or storage directories.

```bash

rclone lsd <REMOTE_NAME>:
rclone ls <REMOTE_NAME>:<bucket-name>
rclone lsl <REMOTE_NAME>:<bucket-name>
rclone mkdir <REMOTE_NAME>:<bucket-name>
rclone rmdir <REMOTE_NAME>:<bucket-name>
rclone purge <REMOTE_NAME>:<bucket-name>

```

## File / Object Commands

Copy, move, sync, or delete files and objects.

```bash

rclone copy <SOURCE> <REMOTE_NAME>:<bucket-name>
rclone move <SOURCE> <REMOTE_NAME>:<bucket-name>
rclone delete <REMOTE_NAME>:<bucket-name>/<file>
rclone deletefile <REMOTE_NAME>:<bucket-name>/<file>
rclone sync <SOURCE> <REMOTE_NAME>:<bucket-name>
rclone lsjson <REMOTE_NAME>:<bucket-name>/<file>
rclone size <REMOTE_NAME>:<bucket-name>

```


## Mount / Serve Commands

Access remote storage locally or via web.

```bash

rclone mount <REMOTE_NAME>:<bucket-name> /mnt/mybucket
rclone serve http <REMOTE_NAME>:<bucket-name> --addr :8080


```

## Crypt / Encryption

Encrypt or decrypt files on remote storage.

```bash

rclone config create <CRYPT_REMOTE_NAME> crypt remote=<REMOTE_NAME>:<bucket-name> password=<PASSWORD> password2=<PASSWORD2>
rclone ls <CRYPT_REMOTE_NAME>:


```


[Rclone Documentation](https://rclone.org/docs/)

