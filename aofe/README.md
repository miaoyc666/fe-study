# fe-study
learning notes of FE


### QA
#### 1.npm run 的原理是什么？
A: npm run 是 npm 提供的一个命令，用于执行 package.json 文件中定义的 scripts 脚本。它的原理是读取 package.json 文件中的 scripts 字段，然后执行其中的命令。  
具体来说，当执行 npm run script-name 命令时，npm 会在当前目录下查找 package.json 文件，然后读取其中的 scripts 字段，找到与 script-name 相对应的命令，最后执行该命令。  
在执行命令时，npm 会在当前目录下查找该命令的可执行文件，如果找不到则会在系统的 PATH 环境变量中查找。如果找到多个可执行文件，则会按照 PATH 中的顺序依次执行。  
总的来说，npm run 的原理就是读取 package.json 文件中定义的 scripts 脚本，然后执行其中的命令。
