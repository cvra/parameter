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
        "@ch_cvra_cmp_mem_access//:cmp_mem_access",
        "@ch_cvra_cmp//:cmp",
    ],
)

cc_test(
    name = "parameter-test",
    size = "small",
    srcs = glob([
        "*.h",  # Hack to adapt Bazel's include convention to CVRA's
        "tests/*.cpp",
    ]),
    deps = [
        ":parameter",
        "@ch_cvra_cmp_mem_access//:cmp_mem_access",
        "@ch_cvra_test_runner//:main",
        "@ch_cvra_cmp//:cmp",
    ],
)
