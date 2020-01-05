# See https://github.com/bazelbuild/rules_foreign_cc
#
# See https://github.com/amrayn/licensepp

load("@rules_foreign_cc//tools/build_defs:cmake.bzl", "cmake_external")

filegroup(
    name = "srcs",
    srcs = ["CMakeLists.txt"] + glob(["cmake/*", "src/**", "license++/*"]),
    visibility = ["//visibility:public"],
)

cmake_external(
    name = "licensepp",
    cache_entries = {
        "MAKEFLAGS": "-j5",
        "CRYPTOPP_ROOT_DIR": "$EXT_BUILD_DEPS/cryptopp",
    },
    defines = ["NDEBUG"],
    lib_source = ":srcs",
    static_libraries = ["liblicensepp.a"],
    visibility = ["//visibility:public"],
    deps = [
        "//third_party/cryptopp",
    ],
)
