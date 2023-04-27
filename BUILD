load("@rules_python//python:defs.bzl", "py_test")
load("@pip//:requirements.bzl", "requirement")
load("@rules_python//python/pip_install:requirements.bzl", "compile_pip_requirements")

filegroup(
    name = "python_requirements",
    srcs = [
        "requirements.lock",
        "requirements.txt",
    ],
    visibility = ["//visibility:public"],
)

compile_pip_requirements(
    name = "pip_requirements",
    timeout = "moderate",
    extra_args = ["--allow-unsafe"],
    requirements_in = "requirements.txt",
    requirements_txt = "requirements.lock",
    tags = ["manual"],
)
py_test(
  name = "main",
  srcs = ["main.py"],
  deps = [requirement("protobuf"), requirement("ray"), requirement("torch"), requirement("torchvision"), requirement("tabulate"), requirement("gymnasium"), requirement("dm-tree"),requirement("scikit-image")],
)
