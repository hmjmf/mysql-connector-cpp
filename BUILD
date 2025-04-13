load("@rules_proto//proto:defs.bzl", "proto_library")



# cc_library(
#     name = "mysql-connector-cpp",
#     srcs =[
#         "cmake_build/install/lib64/libmysqlcppconnx-static.a",
#         "cmake_build/install/lib64/libcrypto.dylib",
#         "cmake_build/install/lib64/libssl.dylib",
#         ],
#     hdrs = glob([
#         "cmake_build/install/**/*.h",
#     ]),
#     includes = [
#         "cmake_build/install/include",
#     ],
#     deps = [
#         # "@rapidjson//:rapidjson",
#         # "@openssl//:openssl",
#         # "@com_google_protobuf//:protobuf",
#         # "@lz4//:lz4",
#         # "@zstd//:zstd",
#         # "@zlib//:zlib",
#         # "//cdk/protocol/mysqlx/pb:cdk_protocol_mysqlx_pb_proto_cc",
#     ],
#     copts = [
#         "-std=c++20",
#     ],
#     visibility = ["//visibility:public"],
# )

cc_library(
    name = "mysql-connector-cpp",
    srcs = glob([
        "devapi/*.cc",
        "common/*.cc",
    ], exclude = [
        "**/tests/**",
        "**/extra/**"
    ]),
    hdrs = glob([
        "include/mysqlx/**/*.h",
        "devapi/*.h",
        "common/*.h",
    ], exclude = [
        "**/tests/**",
        "**/extra/**"
    ]),
    includes = [
        "include",
        "include/mysqlx",
        "common",
        "cdk/include"
    ],
    deps = [
        "@rapidjson//:rapidjson",
        "@com_google_protobuf//:protobuf",
        "@lz4//:lz4",
        "@zstd//:zstd",
        "@zlib//:zlib",
        "//cdk:cdk",
    ],
    copts = [
        "-std=c++20",
    ],
    visibility = ["//visibility:public"],
)



# cc_library(
#     name = "cdk",
#     srcs = glob([
#         "core/*.cc",
#         "foundation/*.cc",
#         "mysqlx/*.cc",
#         "parser/*.cc",
#     ], exclude = [
#         "**/tests/**",
#         "**/extra/**"
#     ]),
#     hdrs = glob([
#         "foundation/*.h",
#         "include/**/*.h",
#         "mysqlx/*.h",
#         "parser/*.h",
#     ], exclude = [
#         "**/tests/**",
#         "**/extra/**"
#     ]) + ["include/mysql/cdk/foundation/opaque_impl.i"],
#     includes = [
#         "include",
#         "parser",
#     ],
#     deps = [
#         "@rapidjson//:rapidjson",
#         "@openssl//:openssl",
#         "@com_google_protobuf//:protobuf",
#         "@lz4//:lz4",
#         "@zstd//:zstd",
#         "@zlib//:zlib",
#         "//cdk/protocol/mysqlx/pb:cdk_protocol_mysqlx_pb_proto_cc",
#     ],
#     copts = [
#         "-std=c++20",
#     ],
# )
