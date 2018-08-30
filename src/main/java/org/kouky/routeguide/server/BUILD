java_binary(
    name = "routeguide_server",
    main_class = "org.kouky.routeguide.server.RouteGuideServer",
    visibility = [
        "//visibility:public",
    ],
    runtime_deps = [
        ":routeguide_server_lib",
    ],
)

java_library(
    name = "routeguide_server_lib",
    srcs = glob(["*.java"]),
    deps = [
        "//3rdparty/jvm/io/grpc:grpc_stub",
        "//3rdparty/jvm/io/grpc:grpc_netty",
        "//3rdparty/jvm/io/grpc:grpc_protobuf",
        "//3rdparty/jvm/com/google/protobuf:protobuf_java_util",
        "//src/main/proto:routeguide_java_proto",
        "//src/main/proto:routeguide_java_grpc",
        "//src/main/java/org/kouky/routeguide/util:routeguide_util",
    ],
)
