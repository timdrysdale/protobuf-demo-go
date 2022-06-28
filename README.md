# protobuf-demo-go
A demo of protobuf in go


[tutorial](https://developers.google.com/protocol-buffers/docs/gotutorial)

[emacs mode](https://melpa.org/#/protobuf-mode) after installation, invoke with `M-x protobuf-mode`

Note that protobuf compiler installation required changing the permissions on the include folder to match other include folders 

```
# copy the google folder from the install tar to /usr/local/include first
cd /usr/local/include
sudo chmod -R a+r google
sudo chmod -R a+x google #r permissions alone were not sufficient
```

Compilation command
```
protoc --go_out=./ ./addressbook.proto
```

In the example command which writes to and from a phonebook on disk (not included here so far), there is a pretty printed version of the protobuf, which comes from the `writePerson` function [here](https://github.com/protocolbuffers/protobuf/blob/ca17dad213824de92d61fa2c452b84b6567e74a8/examples/go/cmd/list_people/list_people.go#L14)



