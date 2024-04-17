# Logging In

Once you've settled here for a little longer, you will have an account created on `socs-web01`. 

## Passwordless Authentication

To help improve security, you will not be able to use your password to log into this server. You will still need to use
your password for `sudo` actions, however. Instead, you will use an SSH key to log in. Your SSH key can be copied using 
the `ssh-id-copy` command like so:
```Bash
ssh-id-copy <your-user>@<socs-web01-addr>
```

## SSH Config File Entry

To help make logging into `socs-web01` easier, we recommend you add the following into your SSH Config file.

The file can be located at `~/.ssh/config` for macOS and Linux installs, or, `<username>/.ssh/config` for Windows! 

```
Host socs-web01
  HostName <socs-web01-addr>
  User <your-user>
```

Once you have that entry in your SSH Config, you can log into `socs-web01` simply by running:
```Bash
ssh socs-web01
```
You will be brought directly into a terminal prompt for the server!