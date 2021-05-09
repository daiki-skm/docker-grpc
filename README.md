# RPC life cycle

I have implemented [RPC life cycle](https://grpc.io/docs/what-is-grpc/core-concepts/#rpc-life-cycle) using docker.

Please run the following command to work inside a container.
```
cd /infrastructure/docker
docker-compose up -d
docker-compose exec go-grpc bash
```

## Unary RPC
It receives one data and returns one data.

```
go run server/main.go
go run client/main.go
```

## Server streaming RPC
Keeps receiving values from the server.

```
go run server/notification.go
go run client/notification.go
```

## Client streaming RPC
Keeps receiving values from the client.

```
go run server/upload.go
go run client/upload.go
```

## Bidirectional streaming RPC
Both sides will continue to receive values.

```
go run server/chat.go
go run client/chat.go
```
