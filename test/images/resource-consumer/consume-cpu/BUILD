package(default_visibility = ["//visibility:public"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_binary",
    "go_library",
)

go_binary(
    name = "consume-cpu",
    embed = [":go_default_library"],
)

go_library(
    name = "go_default_library",
    srcs = ["consume_cpu.go"],
    importpath = "k8s.io/kubernetes/test/images/resource-consumer/consume-cpu",
    deps = ["//vendor/github.com/nikhita/systemstat:go_default_library"],
)

filegroup(
    name = "package-srcs",
    srcs = glob(["**"]),
    tags = ["automanaged"],
    visibility = ["//visibility:private"],
)

filegroup(
    name = "all-srcs",
    srcs = [":package-srcs"],
    tags = ["automanaged"],
)
