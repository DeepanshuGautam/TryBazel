# Import apple rules
load("@build_bazel_rules_apple//apple:ios.bzl", "ios_unit_test")

# Import swift rules
load("@build_bazel_rules_swift//swift:swift.bzl", "swift_library")

# Build swift files
swift_library(
	name = "unit-tests-swift-files",
    srcs = glob(["*.swift"]),
    visibility = ["//visibility:private"],
    # As our tests are testing our app code
    deps = ["//TryBazel:app-swift-files"],
    # Name of the module for the tests
    module_name = "TryBazelTests",
    testonly = True 
)

# Create target to run the unit tests
ios_unit_test(
    name = "unit-tests",
    deps = [":unit-tests-swift-files"],
    minimum_os_version = "15.0",
    # Sets the context, in this case the iOS application
    test_host = "//TryBazel:app",
    platform_type = "ios",
    visibility = ["//visibility:public"]
)
