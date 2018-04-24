cc_library(
    name = "parameter",
    srcs = glob([
        "*.c",
        "*.h",
    ]),
    hdrs = glob(["*.h"]),
    include_prefix = "parameter",
    visibility = ["//visibility:public"],
    deps = [
        "@ch_cvra_cmp//:cmp",
        "@ch_cvra_cmp_mem_access//:cmp_mem_access",
    ],
)

cc_library(
    name = "parameter_port_mock",
    srcs = ["tests/parameter_port_mock.cpp"],
    visibility = ["//visibility:public"],
    deps = [
        ":parameter",
        "@cpputest//:CppUTest",
    ],
)

cc_test(
    name = "parameter-test",
    size = "small",
    srcs = glob([
        "*.h",  # Hack to adapt Bazel's include convention to CVRA's
        "tests/parameter_port_print_test.cpp",
        "tests/parameter_test.cpp",
        "tests/parameter_types_test.cpp",
    ]),
    deps = [
        ":parameter",
        ":parameter_port_mock",
        "@ch_cvra_cmp//:cmp",
        "@ch_cvra_cmp_mem_access//:cmp_mem_access",
        "@ch_cvra_test_runner//:main",
    ],
)
