java_library(
    name = "routeguide_util",
    srcs = glob(["*.java"]),
    visibility = [
        "//src/main/java/org/kouky/routeguide/client:__pkg__",
        "//src/main/java/org/kouky/routeguide/server:__pkg__",
    ],
    deps = [
        "//3rdparty/jvm/com/google/protobuf:protobuf_java_util",
        "//src/main/proto:routeguide_java_proto",
    ],
    resources = [
        "route_guide_db.json"
    ],
)
