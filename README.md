## Use Go

```
$ git submodule add https://github.com/uniladin/uniladin_proto.git proto

$ go install google.golang.org/protobuf/cmd/protoc-gen-go@latest

$ go install google.golang.org/grpc/cmd/protoc-gen-go-grpc@latest

$ export PATH="$PATH:$(go env GOPATH)/bin"

$ mkdir proto/pb

$ protoc \
    --go_out=proto/pb \
    --go-grpc_out=proto/pb \
    proto/common/ping.proto
```