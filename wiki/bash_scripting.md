---
title: "Scripting in bash"
---

# Scripting in bash 

_ _ _

## Description

Scripting in `bash` is quintessential for anyone who wants to make his Linux experience more enjoyable. 

_ _ _

## Application

_ _ _ 

## Tips

### Debugging with explicit set

**Set -e** - instructs `bash` to exit immediately whenever any command returns non-zero exit status.

**Set -u** - makes the script exit immediately when an undefined variable is being referred to.

**Set -o pipefail** - this setting shows the error code of the failed command in a pipeline (so that it doesn't keep moving along to other commands).

All the sets can be unset and set (e.g. with `set +u` and `set -u`) on-demand within the body of the script. 

### Use less flexible IFS

`Bash` uses IFS set to `$' \n\t` by default, i.e. words are split on newlines, tabs, and spaces. In most cases, however, it is more desirable to set IFS to `$'\n\t`.

### Stop xargs from running if no input is given

Oftentimes we have to use a wonderful utility called `xargs` in our pipes. The problem is that is can keep spawning commands, even if the previous command in the pipe exited with errors. To escape such behaviour, use `xargs -r` which stands for `--no-run-if-empty`. 
_ _ _
## References

