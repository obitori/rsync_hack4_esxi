### rsync_hack4_esxi
## How to use rsync on esxi -- which doesn't have ths tool

$ sshfs -o allow_other root@xx.xx.xx.xx:/vmfs/volumes/esxi_pool1/<OPTIONA_TARG_DIR>/ /mnt/PATH/TO/LOCAL/MOUNT_SPOT
$ rsync -av /home/<USER>/stuff/* /mnt/PATH/TO/LOCAL/MOUNT_SPOT

