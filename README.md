The bash script, named `script`, needs to append the following line to the configuration file `os-release`

```
DOCUMENTATION_URL="<DOC_URL>"
```

where <DOC_URL> is the default URL given in the script, or one provided as the first argument.

For example, if `script` is given the argument `https://help.ubuntu.com/22.04/ubuntu-help/index.html`, then it must append the line


```
DOCUMENTATION_URL="https://help.ubuntu.com/22.04/ubuntu-help/index.html"
```


If no argument is given, the defaut value in the script of `https://help.ubuntu.com/lts/ubuntu-help/index.html` must be used:

```
DOCUMENTATION_URL="https://help.ubuntu.com/22.04/ubuntu-help/index.html"
```


Here are a couple sample runs:

```
user:/tech-test$ tail -2 os-release 
BUG_REPORT_URL="https://bugs.launchpad.net/ubuntu/"
UBUNTU_CODENAME=jammy

user:/tech-test$ ./script 
user:/tech-test$ tail -3 os-release 
BUG_REPORT_URL="https://bugs.launchpad.net/ubuntu/"
UBUNTU_CODENAME=jammy
DOCUMENTATION_URL="https://help.ubuntu.com/lts/ubuntu-help/index.html"

user:/tech-test$  git checkout os-release # reset os-release, removing appended line
Updated 1 path from the index
user:/tech-test$ tail -2 os-release 
BUG_REPORT_URL="https://bugs.launchpad.net/ubuntu/"
UBUNTU_CODENAME=jammy

user:/tech-test$ ./script https://help.ubuntu.com/22.04/ubuntu-help/index.html
user:/tech-test$ tail -3 os-release 
BUG_REPORT_URL="https://bugs.launchpad.net/ubuntu/"
UBUNTU_CODENAME=jammy
DOCUMENTATION_URL="https://help.ubuntu.com/22.04/ubuntu-help/index.html"
```