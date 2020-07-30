# GNU Linux System

## Learning

- [Linux Fundamentals](http://linux-training.be/linuxfun.pdf)
- [Introduction to Linux](http://tldp.org/LDP/intro-linux/intro-linux.pdf)
- [Linux 101 Hacks](https://www.thegeekstuff.com/linux-101-hacks-ebook/)

### Outputs & inputs (aka file descriptors)

- `0` - stdin
- `1` - stdout
- `2` - stderr
- `>` - other

> created every time a program needs to interact with files

They are split, user can redirect them to different outputs (other streams, files, sockets).

`2>&1` redirects a standard error to a standard output so they appear together and can be jointly redirected to an output.

> **NOTE** `2>1` redirects a standard error to a file called `1`
> **NOTE** `ls > /dev/null 2>&1` or `unknowncommand > /dev/null 2>&1` means that no outputs are printed on terminal

## Useful commands

1. please read manual (at least description) for each command
1. you can use documentation during the interview
1. if you get `command not found`, try to install it with `brew` or `apt` or any other package manager.

> **NOTE** just explore a command - please do not learn all possible options
> **NOTE** during testing please be careful with using `rm*` commands

### Junior

#### Junior I

##### UNIX File types

- `-` regular file (text file)
- `d` directory
- `s` unix socket (unix sockets are much faster than communication over ip interface)
- `c` character device (terminal)
- `b` block device (like a terminal but receives blocks)
- `f` named pipeline (created by `mkfifo`)
- `l` link

> everything is a file

##### Useful tricks

- `<space>command` - the command will not be saved in history
- `<command> --help | less`

##### Useful tools

- [tmux](https://linux.die.net/man/1/tmux)
- [screen](https://linux.die.net/man/1/screen)
- [ngrok](https://ngrok.com/)
- [bash loops](https://ryanstutorials.net/bash-scripting-tutorial/bash-loops.php)
- [JSON formatter](https://stedolan.github.io/jq/download/)

##### Commands

- [man](https://linux.die.net/man/1/man)
- [alias](https://ss64.com/bash/alias.html)
- [cd](https://ss64.com/bash/cd.html)
- [cp](https://ss64.com/bash/cp.html) / [mv](https://ss64.com/bash/mv.html) / [mkdir](https://ss64.com/bash/mkdir.html)
- [curl](https://linux.die.net/man/1/curl)
- [wget](https://linux.die.net/man/1/wget)

##### Interview

- what is `man`, what is it for and how to use it?
- practical use cases for `alias`
- what kind of paths `cd` can handle?
- `cp Dockerfile{,.dev}` - explain the command
- what is `mv`?
- how to create a nested directories with `mkdir`?
- how to copy files without changing existing ownership permissions?
- what is the difference between `wget` and `curl`?
- how to add a custom header to a curl's requests?
- how to send a `POST` request with curl?
- does the order of a command option matter?

#### Junior II

##### Linux daemons / services

Daemons are background processes in Linux systems. Most of deamons have names that end with the letter `d` e.g. `memcached`, `sshd`. Scripts stored in `/etc/init.d/` or `/etc/rc.d/` directories are used to manage deamons statuses.

##### Setting hostname/domain name of own local server

Edit one of these files (depends on your OS):

- `/etc/hosts` - OSX (some says that it's valid for Debians as well)
- `/ets/hostname` - Debian familly OS

and add

```
127.0.0.1       bard.dev
```

and you can ping `bard.dev` or use the address in a web browser

##### Commands

- [cut](https://linux.die.net/man/1/cut)
- [grep](https://linux.die.net/man/1/grep)
- [head](https://linux.die.net/man/1/head)
- [less](https://linux.die.net/man/1/less) / [more](https://linux.die.net/man/1/more)
- [ls](https://linux.die.net/man/1/ls)
- [ps](https://linux.die.net/man/1/ps)
- [tail](https://linux.die.net/man/1/tail)
- [tree](https://linux.die.net/man/1/tree)
- [wc](https://linux.die.net/man/1/wc)

##### Interview

- how to read first X lines from a file?
- how to read last X lines from a file?
- what is `less`?
- how to print all lines from fileX and fileY without lines "xyz" and "abc"?

fileX:

```
abc
qwe
zxc
```

fileY:

```
123
xyz
HJKL
```

- what is `cut`?
- how to print all files within nested directories?
- what is the difference between `tail` and `less`?
- what can be done with `ps` command?
- how to count files in a directory?

### Independent

#### Independent I

##### SSH

SSH (*secure shell*) is a network protocol for operating network services securely over an unsecured network. It works with client-server architecture and allows to execute commands (through terminal) on a remote servers.
It uses a key or passphrase to auto authorize and authenticate an access to a user on remote server.

> **NOTE**: SSH server allows to use `scp` or `rsync`.

##### Enable SSH server on OSX

- System preferences
- Sharing
- and check `Remote Login` option

##### Enable SSH server on GNU Linux

Just follow steps from [community notes](https://help.ubuntu.com/community/SSH/OpenSSH/Configuring) or install
`sshd` packaged.

###### Public Key and Private Keys

> **NOTE** *please do not share your private keys with anyone*

> **NOTE** you can use your public key for an authentication with foreign server

![pub_vs_pem](https://www.comodo.com/images/support/certs3.jpg)
![sign_with_pem](https://upload.wikimedia.org/wikipedia/commons/1/1e/Public_key_signing.svg)

###### Generate keys

```bash
$ ssh-keygen -t rsa -b 4096 -C "bob@keys.dev"
Generating public/private rsa key pair.
Enter file in which to save the key (/Users/bard/.ssh/id_rsa): bob_key
Enter passphrase (empty for no passphrase):
Enter same passphrase again:
Your identification has been saved in bob_key.
Your public key has been saved in bob_key.pub.
The key fingerprint is:
SHA256:G0bIuTKmbPyOWOkhl+hqswT5/zAuWmqkVLxFbn6HgkU bob@keys.dev
The key's randomart image is:
+---[RSA 4096]----+
|                 |
|     E o         |
|  . + + .        |
| . o = o         |
|o . @ . S        |
|.B B = + +       |
|*.& o o o        |
|+&.* o           |
|O+=o=..          |
+----[SHA256]-----+
$ ls -la
total 1112
drwxr-xr-x  12 bard  admin     384 Sep 14 14:53 .
drwxr-xr-x  13 bard  admin     416 Aug 28 09:33 ..
-rw-------   1 bard  admin    3243 Sep 14 14:53 bob_key
-rw-r--r--   1 bard  admin     738 Sep 14 14:53 bob_key.pub
```

###### Generate a public key based on private key

```bash
$ ssh-keygen -y -f bob_key > bob_key_2.pub
```

##### Streams and operators

- `>`
```
$ ls -la > files.txt`
# saves list of files to a file, and overwrite an existing value or creates a new file
```
- `>`
```
$ ls -la >> files.txt`
# saves list of files to a file, and append to existing value or creates a new file
```
- `<`
```
$ echo 'hello world' > output
$ cat <output
hello world
```
- `<<`
```
$ cat <<EOF
  > hello
  > world
  > EOF
```
- `|` - pipe eg. `ls | head -2` prints first two files
- `&` - move process to background
- `&&` - logical `AND` operator
- `||` - operator `OR` operator
- `!` - logical `NOT` operator

##### Command Editing Shortcuts

- `Ctrl + a` - go to the start of the command line
- `Ctrl + e` - go to the end of the command line
- `Ctrl + k` - delete from cursor to the end of the command line
- `Ctrl + u` - delete from cursor to the start of the command line
- `Ctrl + w` - delete from cursor to start of word (i.e. delete backwards one word)
- `Ctrl + y` - paste word or text that was cut using one of the deletion shortcuts (such as the one above) after the cursor
- `Ctrl + xx` - move between start of command line and current cursor position (and back again)
- `Alt + b` - move backward one word (or go to start of word the cursor is currently on)
- `Alt + f` - move forward one word (or go to end of word the cursor is currently on)
- `Alt + d` - delete to end of word starting at cursor (whole word if cursor is at the beginning of word)
- `Alt + c` - capitalize to end of word starting at cursor (whole word if cursor is at the beginning of word)
- `Alt + u` - make uppercase from cursor to end of word
- `Alt + l` - make lowercase from cursor to end of word
- `Alt + t` - swap current word with previous
- `Ctrl + f` - move forward one character
- `Ctrl + b` - move backward one character
- `Ctrl + d` - delete character under the cursor
- `Ctrl + h` - delete character before the cursor
- `Ctrl + t` - swap character under cursor with the previous one
- `Ctrl + r` - search the history backwards
- `Ctrl + g` - escape from history searching mode
- `Ctrl + p` - previous command in history (i.e. walk back through the command history)
- `Ctrl + n` - next command in history (i.e. walk forward through the command history)
- `Alt + .` - use the last word of the previous command

> **NOTE** under OSX please set your `ALT` key as `ESC+`
> **NOTE** some keybinds might not work due to different implementation of terminal or shell

###### Command Control Shortcuts

- `Ctrl + l` - clear the screen
- `Ctrl + s` - stops the output to the screen (for long running verbose command)
- `Ctrl + q` - allow output to the screen (if previously stopped using command above)
- `Ctrl + c` - terminate the command
- `Ctrl + z` - suspend/stop the command (such command can be restored with `fg`)

> **NOTE** some keybinds might not work due to different implementation of terminal or shell

###### CommandBangBang

- `!!` - run last command
- `!blah` - run the most recent command that starts with ‘blah’ (e.g. !ls)
- `!blah:p` - print out the command that !blah would run (also adds it as the latest command in the command history)
- `!$` - the last word of the previous command (same as Alt + .)

> **NOTE** some command bangs might not work due to different implementation of shell

##### Files ownership

```bash
$ touch file.txt
$ ls -lah | grep file
-rw-r--r--  1 bard bard    0 Jan 16 09:50 file.txt
$ chown root:root file.txt # sets owner to root user and root group
$ sudo chown root:root file.txt # but it requires a root privileges
$ mkdir tmp
$ touch tmp/test1.txt tmp/test2.txt # creates two files in tmp directorys
$ sudo chown -R root:root tmp # sets owner to root:root for all files in tmp directory recursively
```

##### File permissions

```bash
$ touch file.txt
$ mkdir tmp
$ ls -la | grep -E "file|tmp"
-rw-r--r--  1 bard bard    0 Jan 16 09:50 file.txt
drwxr-xr-x  2 bard bard 4096 Jan 16 09:55 tmp
```

| file type | owner | group | others |
|:--------- |:----: |:-----:| ------:|
| `-`       | `rw-` | `r--` | `r--`  |
| `d`       | `rwx` | `r-x` | `r-x`  |

- file type `-` means that is a regular file
- `rw-` - file can be read/written by owner
- `r--` - file can be read group
- `r--` - file can be read other system users
- file type `d` means that is a directory (more file types could be found above
  in section [UNIX file types](#unix-file-types))
- `rwx` - directory can be read/written/executed by owner (by executed it means
  that owner can list files or enter to a directory)
- `r-x` - directory can be read/executed

###### number and character values

- READ (r) = 4
- WRITE (w) = 2
- EXECUTE (x) = 1

``` bash
4 + 2 + 1 => 7 RWX
4 + 1 => 5 RX
1 => 1 WX
```

```bash
$ chmod 751 test.bin # can be executed by every single user, can be read by owner and users from the group, owner has a full control
```

```bash
$ chmod -x test.bin # removes execute permissions
$ chmod +x test.bin # add execute permission to user/group/others
$ chmod u+x test.bin # add execute permission to owner
$ chmod g+x test.bin # add execute permission to group
$ chmod ug+x test.bin # add execute permission to owner and group
$ chmod ugo+x test.bin # add execute permission to owner, group and others (it does the same like +x)
```

##### Commands

- [at](https://linux.die.net/man/1/at)
- [cron](https://ss64.com/bash/cron.html)
- [chmod](https://linux.die.net/man/1/chmod) / [chown](https://linux.die.net/man/1/chown)
- [ssh](https://linux.die.net/man/1/ssh)
- [df](https://linux.die.net/man/1/df)
- [du](https://linux.die.net/man/1/du)
- [jobs](https://ss64.com/bash/jobs.html) / [bg](https://ss64.com/bash/bg.html) / [fg](https://ss64.com/bash/fg.html)
- [file](https://linux.die.net/man/1/file) / [whereis](https://linux.die.net/man/1/whereis) / [type](https://ss64.com/bash/type.html)
- [find](https://linux.die.net/man/1/find)

##### Interview

- what is `at`?
- how would you describe `cron`?
- how would you describe a cron notation?
- how does cron work for two users on one system?
- how to change file permissions and/or ownership recursively?
- how would you describe a notation for changing file permissions?
- how would you describe a notation for changing file ownership?
- how to connect to a server with a specific identity file?
- what is the different between `df` and `du`?
- how to display a more human readable values with `df`/`du`?
- how to move a job to background?
- how to move a job to foreground?
- how to list all jobs with PIDs from the background?
- how to get `mime` information about a file?
- what is the difference between `whereis` and `type`?
- what you can achieve with `find` command?

#### Independent III

- [kill](https://linux.die.net/man/1/kill) / [killall](https://linux.die.net/man/1/killall) / [pkill](https://linux.die.net/man/1/pkill) / [pgrep](https://linux.die.net/man/1/pgrep)
- [ln](https://linux.die.net/man/1/ln) and [more examples](https://www.ostechnix.com/explaining-soft-link-and-hard-link-in-linux-with-examples/)
- [tar](https://linux.die.net/man/1/tar) / [gzip](https://linux.die.net/man/1/gzip)
- [strace](https://linux.die.net/man/1/strace)
- [ack](https://linux.die.net/man/1/ack)
- [awk](https://linux.die.net/man/1/awk)
- [lsof](https://ss64.com/bash/lsof.html)
- [nc](https://linux.die.net/man/1/nc) / [netstat](https://ss64.com/bash/netstat.html)
- [rsync](https://linux.die.net/man/1/rsync)
- [scp](https://linux.die.net/man/1/scp)
- [xargs](https://linux.die.net/man/1/xargs)

##### Interview

- what is difference between `kill` and `killall`?
- what is the default signal for *kill* commands ?
- what is `ln`?
- what can you achieve with `find` command?
- how to create an archive with with `tar` and `gzip`?
- how to extract an archive?
- what you can achieve with `strace` command?
- what is `ack`?
- when would you use `awk`?
- what can you achieve with `lsof` command?
- how can you create a client and server with `nc`?
- what can you achieve with `netstat` command?
- how would you copy file from/to a remote server?
- how would you combine `xargs` with other commands?

## Deprecated / Outdated

### /proc filesystem

- `cmdline` - how the process was launched
- `cwd` - current working directory
- `environ` - runtime variables
- `exec` - executable (symlink)
- `fd` - opened file descriptors
- `limits` - "ulimit" for the process
- `mounts` - how processes sees mounted filesystem

> and many many ... many more different properties

### iptables

iptables is a command line tool that uses policy chains to allow or block network traffic, sample policies:

- IP address block:

```bash
iptables -A INPUT -s 10.0.0.2 -j DROP
iptables -A FORWARD -s 10.0.0.2 -j DROP
iptables -A INPUT -d 10.0.0.2 -j DROP
iptables -A FORWARD -d 10.0.02 -j DROP
```

- MAC address block:

```bash
iptables -A INPUT -m mac --mac-source 00:00:00:00:00:01 -j DROP
iptables -A FORWARD -m mac --mac-source 00:00:00:00:00:01 -j DROP
```

- port forward for an IP address

```bash
iptables -I FORWARD -p tcp -d 10.0.0.2 --dport 5432 -j ACCEPT
iptables -t nat -A PREROUTING -p tcp -i eth0 --dport 5432 -j DNAT --to 10.0.0.2
```

> **NOTE** do not hurt yourself
> - be careful with iptables - you may block income/outcome traffic on your machine what requires a reboot
> - chain polices are not persisted
