### rsync_hack4_esxi
## How to use rsync on esxi -- which doesn't have this tool

$ sshfs -o allow_other root@xx.xx.xx.xx:/vmfs/volumes/esxi_pool1/<OPTIONA_TARG_DIR>/ /mnt/PATH/TO/LOCAL/MOUNT_SPOT
$ rsync -av /home/<USER>/stuff/* /mnt/PATH/TO/LOCAL/MOUNT_SPOT

Esxi uses a modified form of busybox for its command line and is missing many common GNU/linux tools.  
So, the workaround is to do your work on a linux machine using a mounted drive.  
The basic idea is to use sshfs to mount the esxi target directory on your linux box and then rsync from within the linux box.  
