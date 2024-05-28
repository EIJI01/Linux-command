# Linux Command

## To install docker and set up Ubuntu distro to version 2

- install docker desktop <br/>
<https://www.docker.com/products/docker-desktop/>

- install WSL and chose distro version that you want

```powershell
wsl --status
wsl -v

$env:WSL_UTF8=1
wsl --help | more

# Save help open in window
wsl --help > wsl.help
explorer.exe .
notepade wsl.help

wsl --list --online 

# For the next command, when prompted
# Use: username for the username 
# Use: password for the password
wsl.exe --install --d Ubuntu-22.04

wsl -l

#Check which version of WSL you are running
wsl -l -v

#To set the default version to WSL 1 or WSL 2 
wsl --set-default-version 2

# Set the default
wsl --set-default Ubuntu-22.04

#Upgrade version from WSL 1 to WSL 2
wsl --set-version Ubuntu-22.04 2
```

## To run WSL on Powershell or Command Line Interface  

```powershell
#go to default distro
wsl

#go to distro another version
wsl ~ -d Ubuntu-22.04
```

## Linux command

### Create folder and File

```powershell
mkdir NewFolder --> folder
touch filename --> file
```

### Remove Folder and File

```powershell
rmdir NewFolder
```

```powershell
whoami
pwd
cd .
cd ~
ls
ls -l
ls -al
ls -al ~/.ssh/
ll
cat Filename.txt
nano Filename.txt
cp Filename.txt ../CopyFile.txt
mv Filename.txt ../MoveFile.txt
echo "hello world"
```

### Permission

### <p style="color:lightgreen;font-weight:bold">drwxr-xr-x or 755</p>

#### <span style="color:red;font-weight:bold">d</span> [ <span style="color:orange;font-weight:bold">r</span><span style="color:yellow;font-weight:bold"> w</span><span style="color:purple;font-weight:bold"> x</span> = 7 | <span style="color:orange;font-weight:bold">r</span><span style="font-weight:bold"> -</span><span style="color:purple;font-weight:bold"> x</span> = 5 | <span style="color:orange;font-weight:bold">r</span><span style="font-weight:bold"> -</span><span style="color:purple;font-weight:bold"> x</span> = 5 ]
{
- <p style="color:red;font-weight:bold">d => directory</p>
- <p style="color:red;font-weight:bold"> - => file</p>
- <p style="color:orange;font-weight:bold">r => read = 4</p>
- <p style="color:yellow;font-weight:bold">w => write = 2</p>
- <p style="color:purple;font-weight:bold">x => execute = 1</p>
- <p style="font-weight:bold">- => none = 0</p>
}

<span style="color:lightgreen;font-weight:bold">u => user or owner</span> || 
<span style="color:lightgreen;font-weight:bold">g => group</span> ||
<span style="color:lightgreen;font-weight:bold">o => everyone</span>

#### Change permission

```powershell
#calculate number from permission
chmod 744 filename.txt

chmod o-w filename.txt
chmod u+w filename.txt
```

### Add User

```powershell
#change to root
sudo su -

#add new user
sudo adduser username

#grant right for user to root permission
sudo visudo # add chanyut ALL=(ALL:ALL) ALL
```

### Change owner file or directory

```powershell
#single file
sudo chown chanyut:chanyut filename.txt

#every inside folder change
sudo chown -R chanyut:chanyut foldername
```
