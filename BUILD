load(
    "@rules_rust//rust:defs.bzl",
    "rust_binary",
    "rust_library",
    "rust_test",
)

rust_library(
    name = "transitive",
    srcs = ["transitive.rs"],
    edition = "2018",
)

cc_library(
    name = "direct",
    srcs = ["direct.cc"],
    hdrs = ["direct.h"],
    deps = ["transitive"],
)

rust_binary(
    name = "main",
    srcs = ["main.rs"],
    edition = "2018",
    rustc_flags = [
        "--print",
        "link-args",
    ],
    deps = ["direct"],
)
