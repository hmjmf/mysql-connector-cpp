cc_library(
    name = "cdk_protocol_mysqlx",
    srcs = glob([
        "*.cc",
    ], exclude = [
        "**/tests/**",
        "**/extra/**"
    ]),
    hdrs = glob([
        "*.h",
        "../../inlcude/**/*.h",
    ], exclude = [
        "**/tests/**",
        "**/extra/**"
    ]),
    includes = [
        "../../inlcude"
    ],
    deps = [
        "//cdk/protocol/mysqlx/pb:cdk_protocol_mysqlx_pb_proto_cc",
    ],
    copts = [
        "-std=c++20",
    ],
    visibility = ["//visibility:public"],
)
