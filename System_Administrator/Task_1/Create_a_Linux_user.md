### Create a Linux User with non Interactive Shell


- The password and username is present in this page https://kodekloudhub.github.io/kodekloud-engineer/docs/projects/nautilus


```shell
# Login to the app02 server from the initial thor - jump server

> $ ssh steve@stapp02

```

``` shell
# Create a user ravi with a non interactive Shell

> $ sudo useradd ravi -s /sbin/nologin
```

#### Note : An interactive and non-interactive shell

An interactive shell interacts with the user. If it's a login shell, any commands in ~/.login are executed, if it's not a login shell (you can spawn interactive subshells) .login is not evaluated.

A non-interactive shell does not interact with the user but works a shell script. Whenever you invoke a shell script, the very first line (the "shebang" #!/bin/bash) spawns a non-interactive subshell. All non-interactive shells are no login shells, thus they do not evaluate .login.

Any shell a user can log into is per definition an interactive shell. If it wasn't (like /bin/false or /bin/nologin) the user couldn't log in.