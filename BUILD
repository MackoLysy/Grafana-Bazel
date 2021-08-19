load("@build_bazel_rules_nodejs//:index.bzl", "nodejs_binary")
load("@npm//@grafana/toolkit:index.bzl", "grafana_toolkit")

nodejs_binary(
    name = "node_server",
    entry_point = ":test.js",
)

grafana_toolkit(
    name = "build",
    data = [
        "@npm//@grafana",
        # "@npm//@jest",
        # "@npm//rxjs",
        # "@npm//es-abstract",
        # "@npm//lodash"
    ],
    args = ["plugin:build"]
)
