load("//:java_grpc_library.bzl", "java_grpc_library")

# HelloWorld Targets

proto_library(
    name = "helloworld_proto",
    srcs = ["helloworld.proto"],
)

java_proto_library(
    name = "helloworld_java_proto",
    deps = [":helloworld_proto"],
    visibility = ["//visibility:public"],
)

java_grpc_library(
    name = "helloworld_java_grpc",
    srcs = [":helloworld_proto"],
    deps = [":helloworld_java_proto"],
    visibility = ["//visibility:public"],
)

# RouteGuide Targets

proto_library(
    name = "routeguide_proto",
    srcs = ["routeguide.proto"],
)

java_proto_library(
    name = "routeguide_java_proto",
    deps = [":routeguide_proto"],
    visibility = ["//visibility:public"],
)

java_grpc_library(
    name = "routeguide_java_grpc",
    srcs = [":routeguide_proto"],
    deps = [":routeguide_java_proto"],
    visibility = ["//visibility:public"],
)
