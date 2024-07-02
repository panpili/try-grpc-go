# try grpc
A quick start demo for grpc in go

repo: https://github.com/grpc/grpc-go?tab=readme-ov-file

quick start guide: https://grpc.io/docs/languages/go/quickstart/

## Dependency 
```bash
go install google.golang.org/protobuf/cmd/protoc-gen-go@v1.28
go install google.golang.org/grpc/cmd/protoc-gen-go-grpc@v1.2

go get google.golang.org/grpc v1.64.0
go get google.golang.org/protobuf v1.34.2
```

## How to generate pb file
```bash
protoc -I./proto --go_out=pb --go_opt=paths=source_relative \
    --go-grpc_out=pb --go-grpc_opt=paths=source_relative \
    ./proto/*/*.proto
```

## Run
```bash
go run server/*
go run client/*
```