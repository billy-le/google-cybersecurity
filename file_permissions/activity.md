## Project description

The lab required the user "research2" to have the correct file permissions in their home directory. Some directory and files did not have the correct permissions so the task was to update them to correctly reflect what was needed.

## Check file and directory details

Ensure we are in the user's current working directory, `pwd`. This gave us back: `/home/researcher2`. We need to be in the `projects` directory so we use `cd projects` to navigate into the subdirectory.

Use the commands `ls -la` to check all permissions for folder and files including hidden files and directories.

```bash
total 32
drwxr-xr-x 3 researcher2 research_team 4096 Nov  1 18:04 .
drwxr-xr-x 3 researcher2 research_team 4096 Nov  1 18:38 ..
-rw--w---- 1 researcher2 research_team   46 Nov  1 18:04 .project_x.txt
drwx--x--- 2 researcher2 research_team 4096 Nov  1 18:04 drafts
-rw-rw-rw- 1 researcher2 research_team   46 Nov  1 18:04 project_k.txt
-rw-r----- 1 researcher2 research_team   46 Nov  1 18:04 project_m.txt
-rw-rw-r-- 1 researcher2 research_team   46 Nov  1 18:04 project_r.txt
-rw-rw-r-- 1 researcher2 research_team   46 Nov  1 18:04 project_t.txt
```

## Describe the permissions string

Using the example, `drwxrwxrwx`, we can break down the permissions for a certain directory or file.

The first character, `d` indicates this is a directory. It it was a `-`, that would mean we are looking at the permissions for a file.

The next three characters, is `rwx`, and repeats again twice. Since we see three of them in sequence, this means that the user, group, and other permission types have read, write, and executing permissions.

If any of these permissions has a `-` like `r-x`, that means the permission is set to readable and executable but not write access.

## Change file permissions

To change a file permission, the command to use is `chmod`. `chmod` takes two arguments, the first being the permissions to modify, and the second is the directory or file to update.

In this case, we want to change the permissions for the file `project_k.txt` to remove write access for the group and other.

To do this, we use `chmod g-w,o-w project_k.txt`.

To confirm our changes, we use `ls -l project_k.txt` which gives us:

```bash
-rw-r--r-- 1 researcher2 research_team   46 Nov  1 18:04 project_k.txt

```

## Change file permissions on a hidden file

To list hidden files and their permission, we use the `a` flag along with the `ls` command.

`ls -a` gives us:

```bash
-rw--w---- 1 researcher2 research_team   46 Nov  1 18:04 .project_x.txt

```

## Change directory permissions

The hidden file should only be accessed by the user so we use `chmod u-w .project_x.txt`

## Summary

As a security analyst, it's important to set the correct permissions for directories and files in a network. I learned about using the `ls -la` command to show all files and directories including hidden ones and using the `chmod` command to update the permissions.
