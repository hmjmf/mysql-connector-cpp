load("@rules_proto//proto:defs.bzl", "proto_library")

proto_library(
    name = "cdk_protocol_mysqlx_pb_proto_lib",
    srcs = glob([
        "*.proto",
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
