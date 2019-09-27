# cobra-demo
cobra 命令行框架的Demo

# steps

## install cobra

```bash
go get -u github.com/spf13/cobra/cobra
```

## init project

```bash
# mkdir 
mkdir -p cobra-demo && cd cobra-demo

# init project
cobra init --pkg-name github.com/huweihuang/cobra-demo
```

project tree

```
./
├── LICENSE
├── cmd
│   ├── root.go
└── main.go
```

## add command

```bash
cobra add serve
cobra add config
cobra add create -p 'configCmd' # 在父命令config命令下创建子命令create,若没有指定-p,默认的父命令为rootCmd。
```

project tree

```
./
├── LICENSE
├── cmd
│   ├── config.go  # rootCmd的子命令 
│   ├── create.go  # config的子命令
│   ├── root.go    # 默认父命令
│   └── server.go  # rootCmd的子命令
└── main.go
```

## Complete code logic

Complete specific code logic
