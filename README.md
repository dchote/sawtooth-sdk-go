*Build go sdk*

* Install libssl-dev package
* Install libzmq5-dev package

* Install golang packages & build:
```
go get github.com/golang/mock/gomock
go install github.com/golang/mock/mockgen

go get -u github.com/golang/protobuf/protoc-gen-go

go get github.com/dchote/sawtooth-sdk-go
cd $GOPATH/src/github.com/dchote/sawtooth-sdk-go
go generate
```
Docker instructions
```
cd sawtooth-sdk-go
docker build . -t sawtooth-sdk-go
docker run -v $(pwd):/project/sawtooth-sdk-go sawtooth-sdk-go
```

Go generate will build the protos / mocks and place them in the protobuf or mocks directory respectively.
