load("@rules_cc//cc:defs.bzl", "cc_binary", "cc_library")
load("//tools:cpplint.bzl", "cpplint")

cc_library(
    name = "stardustmsgexporterlib",
    srcs = ["stardust_msg_exporter.cc"],
    hdrs = ["stardust_msg_exporter.h"],
    deps = [
        "//cyber",
        "//modules/drivers/proto:pointcloud_cc_proto",
        "//modules/drivers/proto:sensor_image_cc_proto",
        "//modules/perception/lidar/common:pcl_util",
        "//modules/perception/onboard/transform_wrapper",
        "@com_google_absl//absl/strings",
        "@opencv",
    ],
)

cc_binary(
    name = "stardust_msg_exporter",
    srcs = ["stardust_msg_exporter_main.cc"],
    deps = [
        ":stardustmsgexporterlib",
        "//modules/drivers/proto:pointcloud_cc_proto",
        "//modules/drivers/proto:sensor_image_cc_proto",
        "@com_google_absl//absl/strings",
    ],
)

cpplint()
