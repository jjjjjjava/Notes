[toc]

## makefile的规则

```
target ... : prerequisites ...
    recipe
    ...
    ...
```

- target（目标文件）

  可以是一个object file（目标文件），也可以是一个可执行文件，还可以是一个标签（label）。对于标签这种特性，在后续的“伪目标”章节中会有叙述。

- prerequisites(依赖项)

  生成该target所依赖的文件和/或target。

- recipe

  该target要执行的命令（任意的shell命令）。



> 处理的规则：如果任何一个依赖项的时间戳比目标文件的时间戳新，那么就调用recipe中的Command，处理依赖项以生成目标文件。