## Install Java OpenJDK

Check version:

`$ java --version`

If missing:

`$ sudo apt install openjdk-17-jre`

## Increase TCP Connection Limits
To support Java threads, increase the open files limit by configuring soft and hard file handles in /etc/security/limits.conf (via a text editor or a single command string):

```
$ cat <HERE | sudo tee --append /etc/security/limits.conf > /dev/null
  *	soft nofile 32768
  *	hard nofile 32768
  HERE
```

