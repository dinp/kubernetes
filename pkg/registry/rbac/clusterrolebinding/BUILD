package(default_visibility = ["//visibility:public"])

licenses(["notice"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
)

go_library(
    name = "go_default_library",
    srcs = [
        "doc.go",
        "registry.go",
        "strategy.go",
    ],
    tags = ["automanaged"],
    deps = [
        "//pkg/api:go_default_library",
        "//pkg/apis/rbac:go_default_library",
        "//pkg/apis/rbac/validation:go_default_library",
        "//pkg/genericapiserver/registry/rest:go_default_library",
        "//vendor:k8s.io/apimachinery/pkg/apis/meta/internalversion",
        "//vendor:k8s.io/apimachinery/pkg/apis/meta/v1",
        "//vendor:k8s.io/apimachinery/pkg/fields",
        "//vendor:k8s.io/apimachinery/pkg/labels",
        "//vendor:k8s.io/apimachinery/pkg/runtime",
        "//vendor:k8s.io/apimachinery/pkg/util/validation/field",
        "//vendor:k8s.io/apimachinery/pkg/watch",
        "//vendor:k8s.io/apiserver/pkg/endpoints/request",
        "//vendor:k8s.io/apiserver/pkg/storage",
        "//vendor:k8s.io/apiserver/pkg/storage/names",
    ],
)

filegroup(
    name = "package-srcs",
    srcs = glob(["**"]),
    tags = ["automanaged"],
    visibility = ["//visibility:private"],
)

filegroup(
    name = "all-srcs",
    srcs = [
        ":package-srcs",
        "//pkg/registry/rbac/clusterrolebinding/policybased:all-srcs",
        "//pkg/registry/rbac/clusterrolebinding/storage:all-srcs",
    ],
    tags = ["automanaged"],
)
