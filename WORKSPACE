load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

http_archive(
    name = "build_bazel_rules_nodejs",
    sha256 = "8f5f192ba02319254aaf2cdcca00ec12eaafeb979a80a1e946773c520ae0a2c9",
    urls = ["https://github.com/bazelbuild/rules_nodejs/releases/download/3.7.0/rules_nodejs-3.7.0.tar.gz"],
)


load("@build_bazel_rules_nodejs//:index.bzl", "npm_install", "node_repositories")

# node_repositories(
#     node_version = "16.0.0",
#     package_json = ["//:package.json"],
# )

npm_install(
    name = "npm",
    # Opt out of directory artifacts, we rely on ts_library which needs
    # to see labels for all third-party files.
    exports_directories_only = True,
    package_json = "//:package.json",
    package_lock_json  = "//:package-lock.json",
)
