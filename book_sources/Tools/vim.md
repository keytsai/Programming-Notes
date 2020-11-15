# Vim 操作

![Vim](/images/2020-11-14-13-53-12.png)

Example:

```bash
#! /usr/bin/bash
echo "The script name is        ==> ${0}"
echo "Total parameter number is ==> $#"
[ "$#" -lt 2 ] && echo "Parameter is less than 2." && exit 0
echo "Your whole parameter is   ==> '$@'"
total=$((${1}+${2}))
echo The sum is : ${total}

```