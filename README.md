# test.log parser

## Usage

Generates list of individual test to run from `test.log`:

```
$ cat test.log | go run main.go
go test github.com/hashicorp/consul/agent -run TestRexecWriterAB
go test github.com/hashicorp/consul/agent -run TestRexecWriter
go test github.com/hashicorp/consul/agent -run TestCoordinate_Node
go test github.com/hashicorp/consul/watch -run TestAE_Run_QuitMORESPACES
go test github.com/hashicorp/consul/watch -run TestAE_Run_Quit
```

or when you have it in your `PATH` and want to run the test right away:

```
$ cat test.log | testlog | bash
```

```
$ cat test.log | testlog -tags 'consulent consulprem' | bash
```

## Features

Errors are written to STDERR and it supports providing flags with `-flags`.
