package(
    default_visibility = [
        ":friends",
    ],
    licenses = ["notice"],  # Apache 2.0
)

package_group(
    name = "friends",
    includes = ["//third_party/mlir:subpackages"],
    packages = [
        "//tensorflow/compiler/mlir/...",
        "//tensorflow/compiler/mlir/lite/...",
    ],
)

cc_library(
    name = "hlo_xla_quantization_passes",
    srcs = [
        "op_quant_spec.inc",
        "propagate.cc",
    ],
    hdrs = [
        "passes.h",
    ],
    deps = [
        "//tensorflow/compiler/mlir/lite/quantization:quantization_config",
        "//tensorflow/compiler/mlir/lite/quantization:quantization_lib",
        "@com_google_absl//absl/memory",
        "@llvm-project//llvm:support",
        "@llvm-project//mlir:IR",
        "@llvm-project//mlir:Pass",
        "@llvm-project//mlir:QuantOps",
    ],
    alwayslink = 1,
)
