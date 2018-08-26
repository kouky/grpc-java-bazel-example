# gRPC Java Bazel Example

A working [gRPC](https://grpc.io) example using the [Bazel](https://bazel.build) build system. It's meant as a supplement
to the official [gRPC Java Quick Start Guide](https://grpc.io/docs/quickstart/java.html).


## Before you begin

- JDK: version 8 or higher
- Bazel: [see install instructions](https://docs.bazel.build/versions/master/install.html)

## Clone this repo

```
git clone git@github.com:kouky/grpc-java-bazel-example.git
cd grpc-java-bazel-example
```

## Run gRPC Application 

Compile all the bazel targets

```
bazel build //...
```

Run the server

```
bazel-bin/src/java/org/kouky/helloworld/server/helloworld_server
```

In another terminal, run the client

```
bazel-bin/src/java/org/kouky/helloworld/client/helloworld_client
```

You should see the following output as the client talks to the server.

```
Aug 26, 2018 9:39:49 PM org.kouky.helloworld.client.HelloWorldClient greet
INFO: Will try to greet world ...
Aug 26, 2018 9:39:49 PM org.kouky.helloworld.client.HelloWorldClient greet
INFO: Greeting: Hello world
Aug 26, 2018 9:39:49 PM org.kouky.helloworld.client.HelloWorldClient greet
INFO: Greeting: Hello again world
```

## 3rdParty Dependencies

Third party dependencies are specified in `dependencies.yaml` and generated by [bazel-deps](https://github.com/johnynek/bazel-deps).


To regenerate `3rdparty` dependencies clone the `bazel-deps` repo, change directory into it, and run the following.

```
bazel run //:parse -- generate -r /path/to/grpc-java-bazel-example -s 3rdparty/workspace.bzl -d dependencies.yaml
```
