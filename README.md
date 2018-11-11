# check_zfs
Tool to check status of ZFS pools in FreeBSD.

## Installation
Simply checkout this repository or download [check_zfs](https://raw.githubusercontent.com/peterpakos/check_zfs/master/check_zfs) and link/move the script to `/usr/local/bin/check_zfs`, make sure it's executable:
```
$ sudo curl -o /usr/local/bin/check_zfs "https://raw.githubusercontent.com/peterpakos/check_zfs/master/check_zfs"
$ sudo chmod +x /usr/local/bin/check_zfs
```

## Crontab
To check ZFS pools every minute, add the following line to user's crontab by running `crontab -e`:
```
* * * * * /usr/local/bin/check_zfs >/dev/null 2>&1
```
