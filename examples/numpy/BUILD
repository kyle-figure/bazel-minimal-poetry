load("@rules_poetry//lib:py_zip.bzl", "py_zip")
load("//tools/poetry:transitions.bzl", "py_binary_arm64", "py_binary_win", "py_binary_x86_64")

py_binary(
    name = "app",
    srcs = ["app.py"],
    deps = [
        "@poetry//:numpy",
    ],
)

py_binary_arm64(
    name = "app_arm64",
    binary = ":app",
)

py_zip(
    name = "deploy_arm64",
    target = ":app_arm64",
)

py_binary_x86_64(
    name = "app_x86_64",
    binary = ":app",
)

py_zip(
    name = "deploy_x86_64",
    target = ":app_x86_64",
)

py_binary_win(
    name = "app_win",
    binary = ":app",
)

py_zip(
    name = "deploy_win",
    target = ":app_win",
)
