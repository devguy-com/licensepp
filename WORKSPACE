workspace(name = "licensepp")

load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")
# Building with cmake and make (begin)

http_archive(
    name = "rules_foreign_cc",
    strip_prefix = "rules_foreign_cc-master",
    url = "https://github.com/bazelbuild/rules_foreign_cc/archive/master.zip",
)

load("@rules_foreign_cc//:workspace_definitions.bzl", "rules_foreign_cc_dependencies")

rules_foreign_cc_dependencies()

all_content = """filegroup(name = "all", srcs = glob(["**"]), visibility = ["//visibility:public"])"""
# Building with cmake and make (end)

http_archive(
    name = "rules_cc",
    strip_prefix = "rules_cc-master",
    url = "https://github.com/bazelbuild/rules_cc/archive/master.zip",
)

# dev-guy/cryptopp
http_archive(
    name = "cryptopp",
    build_file_content = all_content,
    strip_prefix = "cryptopp-master",
    url = "https://github.com/devguy-com/cryptopp/archive/master.zip",
)
