# download

This script enables copying through `scp` one or multiple files/directories from a remote machine to your local.

By default, it will copy these files to wherever your `$DOWNLOADS` points to. This variable can be automatically exported by adding the following to your .bashrc file:

```bash
export DOWNLOADS='/mnt/c/Users/marco/Downloads/'
```

## Getting started

To run this command, simply:

```bash
download remote_host /tmp/file.txt
```

```text
marcos@MARCOS-LAPTOP /tmp $ download atenea /tmp/file.txt
↘ Copying file /tmp/file.txt…
✓ All done. Files are in /mnt/c/Users/marco/Downloads/
```

The file will automatically download to your `$DOWNLOADS` directory.

To download multiple files or directories you can run:

```bash
download remote_host /tmp/file1.txt /tmp/file2.txt /tmp/dir1
```

```text
marcos@MARCOS-LAPTOP /tmp $ download atenea /tmp/file.txt /tmp/file1.txt /tmp/file2.txt /tmp/dir1/
↘ Copying file /tmp/file.txt…
↘ Copying file /tmp/file1.txt…
↘ Copying file /tmp/file2.txt…
↘ Copying directory /tmp/dir1/…
✓ All done. Files are in /mnt/c/Users/marco/Downloads/
```

## Autocompletion

For autocompletion to work, copy the file `autocompletion/download` file into `/etc/bash_completion.d/`. This will enable autocompletion when hitting `TAB` both for the remote host machines (the script reads from `~/.ssh/config`) and for the remote files and directories.
