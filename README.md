## MacOS
* Install golang: https://golang.org/dl/
* Install homebrew: https://brew.sh

#### Install packages
```
brew install python zmq
```

## Linux

* Install golang: https://golang.org/dl/
#### Install packages
```apt-get install libssl-dev libzmq5-dev```

---

### Build Sawtooth SDK:
```
go get github.com/golang/mock/gomock
go install github.com/golang/mock/mockgen

go get -u github.com/golang/protobuf/protoc-gen-go

go get github.com/dchote/sawtooth-sdk-go
cd $GOPATH/src/github.com/dchote/sawtooth-sdk-go
go generate
```