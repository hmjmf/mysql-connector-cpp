cc_library(
    name = "cdk",
    srcs = glob([
        "core/*.cc",
        "foundation/*.cc",
        "mysqlx/*.cc",
        "parser/*.cc",
    ], exclude = [
        "**/tests/**",
        "**/extra/**"
    ]),
    hdrs = glob([
        "foundation/*.h",
        "include/**/*.h",
        "mysqlx/*.h",
        "parser/*.h",
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
        "@openssl//:openssl",
        "@com_google_protobuf//:protobuf",
        "@lz4//:lz4",
        "@zstd//:zstd",
        "@zlib//:zlib",
        "//cdk/protocol/mysqlx:cdk_protocol_mysqlx",
    ],
    copts = [
        "-std=c++20",
    ],
    visibility = ["//visibility:public"],
)
