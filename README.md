由于种种原因(不能确定是否完全由我的环境不同导致)，原仓库的版本本人无法使用，故做了一些修改以使其能在我的环境下运行。

补充：原仓库版本bytes和str混用，导致部分功能在python3下用不了，我这边改成了python3能用的，至于python2下还能不能用不作测试。

# pstdio

A GDB plug-in that can set stdio of the program you debug.

# Notice
See issue [#1](https://github.com/Ovi3/pstdio/issues/1)

# Installation
```
git clone https://github.com/Ovi3/pstdio.git ~/pstdio
echo "source ~/pstdio/pstdio.py" >> ~/.gdbinit
```

# Usage

First open GDB, And type 'pstdio help' to see the help text.

Example:
1. When you debug the program, and the program will call the '`<read@plt>` to read data from stdio.
2. And if you wanna enter the data, like '\x02\x03\x04\x05', just type:
```
pstdio data /x \\x02\\x03\\x04\\x05
```
3. Then execute the 'call `<read@plt>`', the data you enter will be input.
4. Or you can type 'psdtio file /path/to/data'. In this case, data of the file will be input.
