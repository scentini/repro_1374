load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

http_archive(
    name = "rules_rust",
    sha256 = "73580f341f251f2fc633b73cdf74910f4da64d06a44c063cbf5c01b1de753ec1",
    urls = [
        "https://mirror.bazel.build/github.com/bazelbuild/rules_rust/releases/download/0.5.0/rules_rust-v0.5.0.tar.gz",
        "https://github.com/bazelbuild/rules_rust/releases/download/0.5.0/rules_rust-v0.5.0.tar.gz",
    ],
)

#local_repository(
#    name = "rules_rust",
#    path = "../rules_rust",
#)

load("@rules_rust//rust:repositories.bzl", "rules_rust_dependencies", "rust_register_toolchains")


rules_rust_dependencies()

rust_register_toolchains(edition = "2021")
