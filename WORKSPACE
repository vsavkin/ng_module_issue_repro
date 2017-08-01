load("@bazel_tools//tools/build_defs/repo:git.bzl", "git_repository")

git_repository(
    name = "build_bazel_rules_typescript",
    remote = "https://github.com/bazelbuild/rules_typescript.git",
    commit = "75f416d",
)

git_repository(
    name = "build_bazel_rules_angular",
    remote = "https://github.com/alexeagle/rules_angular",
    commit = "ce85fe6",
)

git_repository(
    name = "io_bazel_rules_sass",
    remote = "https://github.com/bazelbuild/rules_sass.git",
    tag = "0.0.2",
)

load("@build_bazel_rules_typescript//:defs.bzl", "node_repositories")
load("@io_bazel_rules_sass//sass:sass.bzl", "sass_repositories")

node_repositories(package_json = "//:package.json")
sass_repositories()