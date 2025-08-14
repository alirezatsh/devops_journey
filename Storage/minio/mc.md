# MinIO Client (mc) - Commands Reference

## Installation and Configuration

### Linux/macOS

```bash

wget https://dl.min.io/client/mc/release/linux-amd64/mc  
chmod +x mc  
sudo mv mc /usr/local/bin/
mc alias set <ALIAS_NAME> <URL> <ACCESS_KEY> <SECRET_KEY>

```


## Alias Commands

Manage aliases 

```bash

mc alias list  
mc alias remove <ALIAS_NAME> 

```


## Bucket Commands

Manage buckets 

```bash
mc ls <ALIAS_NAME>
mc mb <ALIAS_NAME>/<bucket-name> 
mc rb <ALIAS_NAME>/<bucket-name>
mc policy set <none|download|upload|public> <ALIAS_NAME>/<bucket-name>  
mc anonymous set <public|private|custom> <ALIAS_NAME>/<bucket-name>  

```


## Object Commands

Manage objects

```bash

mc cp <SOURCE> <ALIAS_NAME>/<bucket-name> 
mc mv <SOURCE> <ALIAS_NAME>/<bucket-name> 
mc rm <ALIAS_NAME>/<bucket-name>/<object>
mc mirror <ALIAS_NAME>/<bucket-name>  <ALIAS_NAME2>/<bucket-name2> 
mc mirror --watch <ALIAS_NAME>/<bucket-name> <ALIAS_NAME2>/<bucket-name2>
mc find <ALIAS_NAME>/<bucket-name> --older-than 7d
mc tree <ALIAS_NAME>/<bucket-name>
mc du --recursive <ALIAS_NAME>/<bucket-name>
mc cat <ALIAS_NAME>/<bucket-name>/file.txt
mc stat <ALIAS_NAME>/<bucket-name>/file.txt

```


## User commands

Manage users

```bash

mc admin user add <ALIAS_NAME> <USERNAME> <PASSWORD>
mc admin user remove <ALIAS_NAME> <USERNAME>
mc admin policy set <ALIAS_NAME> <POLICY> --user <USERNAME>

```

## Encryption / Key Management

Manage keys

```bash

mc encrypt set <ALIAS_NAME>/<bucket-name> <KMS_KEY>
mc encrypt unset <ALIAS_NAME>/<bucket-name>

```

## Bucket Versioning & Lifecycle

Manage versions

```bash

mc version enable <ALIAS_NAME>/<bucket-name>
mc version disable <ALIAS_NAME>/<bucket-name>
mc ilm add <ALIAS_NAME>/<bucket-name> <rule.json>
mc ilm remove <ALIAS_NAME>/<bucket-name>

```


## Admin Commands

Manage admin

```bash

mc admin info <ALIAS_NAME>  
mc admin service restart <ALIAS_NAME>  

```

[MinIO Client Documentation](https://docs.min.io/community/minio-object-store/reference/minio-mc.html)
