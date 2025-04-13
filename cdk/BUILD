load("@rules_proto//proto:defs.bzl", "proto_library")

proto_library(
    name = "cdk_protocol_mysqlx_pb_proto_lib",
    srcs = glob([
        "protocol/mysqlx/pb/*.proto",
    ]),
    deps = [
        "@com_google_protobuf//:descriptor_proto",
    ],
    strip_import_prefix = "/cdk/protocol/mysqlx/pb",
)


cc_proto_library(
    name = "cdk_protocol_mysqlx_pb_proto_cc",
    deps = [
        ":cdk_protocol_mysqlx_pb_proto_lib",
    ],
    visibility = ["//visibility:public"],
)



cc_library(
    name = "cdk",
    srcs = glob([
        "core/*.cc",
        "foundation/*.cc",
        "mysqlx/*.cc",
        "parser/*.cc",
        "protocol/mysqlx/*.cc",
    ], exclude = [
        "**/tests/**",
        "**/extra/**"
    ]),
    hdrs = glob([
        "foundation/*.h",
        "include/**/*.h",
        "mysqlx/*.h",
        "parser/*.h",
        "protocol/mysqlx/*.h",
    ], exclude = [
        "**/tests/**",
        "**/extra/**"
    ]) + ["include/mysql/cdk/foundation/opaque_impl.i"],
    includes = [
        "include",
        "parser",
    ],
    deps = [
        "@rapidjson//:rapidjson",
        "@openssl//:ssl",
        "@openssl//:crypto",
        "@com_google_protobuf//:protobuf",
        "@lz4//:lz4",
        "@lz4//:lz4_frame",
        "@zstd//:zstd",
        "@zlib//:zlib",
        ":cdk_protocol_mysqlx_pb_proto_cc",
    ],
    copts = [
        "-std=c++20",
        "-fvisibility=hidden",
    ],
    linkstatic = True, 
    visibility = ["//visibility:public"],
    linkopts = [
        "-lresolv"
    ],
)
