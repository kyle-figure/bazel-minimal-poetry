load("@rules_poetry//python:poetry.bzl", "poetry_update")

poetry_update(
    name = "update_lock",
    lock = "poetry.lock",
    toml = "pyproject.toml",
)

exports_files = ["poetry.lock"]

platform(
    name = "arm64",
    constraint_values = [
        "@platforms//os:linux",
        "@platforms//cpu:arm64",
    ],
)

platform(
    name = "x86_64",
    constraint_values = [
        "@platforms//os:linux",
        "@platforms//cpu:x86_64",
    ],
)

platform(
    name = "win",
    constraint_values = [
        "@platforms//os:windows",
        "@platforms//cpu:x86_64",
    ],
)