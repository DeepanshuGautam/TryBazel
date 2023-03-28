# Import apple rules
load("@build_bazel_rules_apple//apple:ios.bzl", "ios_application")

# Import swift rules
load("@build_bazel_rules_swift//swift:swift.bzl", "swift_library")

# Build swift files
swift_library(
	name = "app-swift-files",
	srcs = glob(["*.swift"]), # You can put all swift files under `Sources` directory
    visibility = ["//visibility:public"],
    module_name = "TryBazel"
)

# Create target to run the app
ios_application(
    name = "app",
    # Passing swift library as deps
    deps = [":app-swift-files"],
    bundle_id = "com.deepanshugautam.TryBazel",
    families = [
        "iphone",
        "ipad"
    ],
    infoplists = ["Info.plist"],
    resources = glob(["Assets.xcassets/**"]),
    minimum_os_version = "14.0",
    visibility = ["//visibility:public"]
)
