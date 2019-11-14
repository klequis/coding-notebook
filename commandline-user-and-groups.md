# commandline-user-and-groups


**List all groups on machine**

```console
sudo getent group
```
**Add user to group**

```console
sudo adduser [username] [groupname]
```

**Add a group**

```console
sudo addgroup [groupname]
```

**See groups user is member of**

```console
groups username
// or
id username
```

**Delete a group**

```console
sudo delgroup [groupname]
```


## Reference
- https://vitux.com/add-and-manage-user-accounts-in-ubuntu-18-04-lts/
