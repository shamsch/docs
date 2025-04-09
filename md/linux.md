## Linux Torvalds 

Bunch of useful linux commands to know. Tack så mycket Linus. 

## ls
```bash
ls -lah
```
- `-l` long listing format
- `-a` show all files including hidden files
- `-h` human readable format (e.g. 1K, 234M, 2G)

### grep
search a string across text files in a directory
```bash
grep -r "search term" <directory>
```
### find
find a file by name in a directory
```bash
find <directory> -name "*.txt"
```
### curl 
GET request, `-I` only shows the header
```bash
curl -I <url>
```
POST request with JSON data, `-H` set header, `-X` set method
```bash
curl -X POST <url> -H "Content-Type: application/json" -d '{"param1":"value1","param2":"value2"}'
```
### file permission 
```bash
ls -l
> drwxr-xr-x 2 user group 4096 Jan 1 00:00 directory
> -rw-r--r-- 1 user group 4096 Jan 1 00:00 file.txt
```
first character means:
- `d` means directory
- `-` means file
- `l` means symbolic link

next 3 characters means owner permission:
- `r` means read
- `w` means write
- `x` means execute
- `-` means no permission

the subsequent 3 character similarly means group permission and then the next 3 means others permissions

### chmod
read write exectue for owner, group and others
```bash 
chmod 777 <file>
```
other ones better [look up](http://chmod-calculator.com)

### ping
```bash
ping <ip> # ping 1.1.1.1 
```
### pipe and redirect
piping is using one commands output as another commands input
```bash
ls -l | grep "search term"
```
redirecting is using `>` to write output to a file
```bash
ls -l > output.txt
```
or `>>` to append output to a file
```bash
ls -l >> output.txt
```
### ssh
```bash
ssh <user>@<ip>
ssh -i <keyfile> <user>@<ip>
ssh-keygen 
scp <file> <user>@<ip>:<path_in_the_server> # copy file to server
```
### command history
```bash
history # show command history
!<number> # run command with number <number>
!! # run last command
<ctrl> + r # search command history
```
### ps or top or htop
```bash
ps aux | grep <process_name> # show process with name <process_name>
top # show all processes
htop # show all processes with a better UI
```
### kill
you can get the `pid` from last step
```bash
kill <pid> # kill process with pid <pid>
kill -9 <pid> # force kill process with pid <pid>
```
