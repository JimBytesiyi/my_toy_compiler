# my_toy_compiler

Source code for "My Toy Compiler". Read about how I did on my blog:

http://gnuu.org/2009/09/18/writing-your-own-toy-compiler


## llvm 15 compatibility

## run 
./parser example.txt

## debug

lldb ./parser
breakpoint set --file codegen.cpp --line 80
run example.txt

#### 改动代码让其兼容llvm16
- link时clang报错/usr/bin/ld里找不到-lz 和 -lncurses，在Makefile命令里删除这两个选项即可