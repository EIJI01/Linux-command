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
pwd
whoami
ls
cd .
cat Filename.txt
nano Filename.txt
cp Filename.txt ../CopyFile.txt
mv Filename.txt ../MoveFile.txt
ls -l
ls -al
ll
echo
```

