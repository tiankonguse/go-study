# call module code


对于本地依赖的 module，可以使用 replace 进行替换


```
go mod init example.com/hello

go mod edit -replace example.com/greetings=../02-create-module
> replace example.com/greetings => ../02-create-module

go mod tidy
> go: found example.com/greetings in example.com/greetings v0.0.0-00010101000000-000000000000

go run hello.go
> Hi, Gladys. Welcome!

go build -o hello.out hello.go
```

参考资料: https://go.dev/doc/tutorial/call-module-code  

