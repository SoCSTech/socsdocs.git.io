# Logging In

Once you've settled here for a little longer, you will have an account created on `seps-app01`. 

## Passwordless Authentication

To help improve security, you will not be able to use your password to log into this server. You will still need to use
your password for `sudo` actions, however. Instead, you will use an SSH key to log in. Your SSH key can be copied using 
the `ssh-id-copy` command like so:
```Bash
ssh-id-copy <your-user>@<seps-app01-addr>
```

If this does not work for you, please provide the colleague completing your enrollment to the server your public ssh key, and they will be able to copy it for you.

## SSH Config File Entry

To help make logging into `seps-app01` easier, we recommend you add the following into your SSH Config file.

The file can be located at `~/.ssh/config` for macOS and Linux installs, or, `C:\Users\<username>\.ssh\config` for Windows! 

```
Host seps-app01
  HostName <seps-app01-addr>
  User <your-user>
```

Once you have that entry in your SSH Config, you can log into `seps-app01` simply by running:
```Bash
ssh seps-app01
```
You will be brought directly into a terminal prompt for the server!