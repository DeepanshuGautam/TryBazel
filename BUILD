# Import xcode rules
load("@rules_xcodeproj//xcodeproj:defs.bzl", "top_level_target", "xcodeproj")

# For building the xcode project
xcodeproj(
    name = "xcodeproj",
    project_name = "TryBazel",
    visibility = ["//visibility:public"],
    tags = ["manual"],
    top_level_targets = [
        # Will target only simulator. So, no device in target environments
        top_level_target("//TryBazel:app", target_environments = ["simulator"]),
        "//TryBazelTests:unit-tests",
    ],
)
