# Back-up Software

## Rsync

## Systemback (https://launchpad.net/systemback)
- Linux

- VMware
- Hyper-V

## Veeam Agent for Microsoft Windows FREE (https://www.veeam.com/windows-endpoint-server-backup-free.html)

- Windows cliënts

## Acronis True Image

- Windows cliënts
- Linux system image

## Trilio (https://www.trilio.io/?fbclid=IwAR2xHNAhmYWJjhYLbOGmZ0yqvdtMkqTTpqO1ydrmouibUfj_p2HakZvkdS4)

- Openstack
- RHV

## Bacula Disaster recovery 

- https://blog.bacula.org/whitepapers/CommunityInstallationGuide.pdf
- https://www.digitalocean.com/community/tutorial_series/how-to-use-bacula-on-centos-7

## Systemback (https://launchpad.net/systemback)
- Linux
  
## Rsync (https://linux.die.net/man/1/rsync)

- Linux
- Windows
- MacOS

## Rclone (https://rclone.org/)

https://www.linuxuprising.com/2020/05/how-to-encrypt-cloud-storage-files-with.html

https://medium.com/@sharkeyio/the-best-tool-youre-not-using-15ba2d238515

- Linux
- Windows
- MacOS

## Syncthing (https://syncthing.net/)

- Linux
- Windows
- MacOS

# Data Rescue

## DDRescue

"The basic operation of ddrescue is fully automatic. That is, you don't have to wait for an error, stop the program, restart it from a new position, etc/"

"Ddrescue does not write zeros to the output when it finds bad sectors in the input, and does not truncate the output file if not asked to. So, every time you run it on the same output file, it tries to fill in the gaps without wiping out the data already rescued."

"Automatic merging of backups: If you have two or more damaged copies of a file, cdrom, etc, and run ddrescue on all of them, one at a time, with the same output file, you will probably obtain a complete and error-free file. This is so because the probability of having the same area damaged in all copies is low (if the errors are randomly located). Using the mapfile, only the needed blocks are read from the second and successive copies. "

https://launchpad.net/~hamishmb/+archive/ubuntu/myppa

```
sudo add-apt-repository ppa:hamishmb/myppa
sudo apt-get update
sudo apt install ddrescue-gui
```
