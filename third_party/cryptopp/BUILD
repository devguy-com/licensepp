# See https://github.com/bazelbuild/rules_foreign_cc

load("@rules_foreign_cc//tools/build_defs:make.bzl", "make")

config_setting(
    name = "darwin_build",
    values = {"cpu": "darwin"},
)

make(
    name = "cryptopp",
    lib_source = "@cryptopp//:all",
    static_libraries =
        ["libcryptopp.a"],
    visibility = ["//visibility:public"],
)
