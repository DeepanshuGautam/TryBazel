load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

http_archive(
    name = "build_bazel_rules_swift",
    sha256 = "d25a3f11829d321e0afb78b17a06902321c27b83376b31e3481f0869c28e1660",
    url = "https://github.com/bazelbuild/rules_swift/releases/download/1.6.0/rules_swift.1.6.0.tar.gz",
)
load(
    "@build_bazel_rules_swift//swift:repositories.bzl",
    "swift_rules_dependencies",
)

swift_rules_dependencies()

http_archive(
    name = "build_bazel_rules_apple",
    sha256 = "3e2c7ae0ddd181c4053b6491dad1d01ae29011bc322ca87eea45957c76d3a0c3",
    url = "https://github.com/bazelbuild/rules_apple/releases/download/2.1.0/rules_apple.2.1.0.tar.gz",
)

load(
    "@build_bazel_rules_apple//apple:repositories.bzl",
    "apple_rules_dependencies",
)

apple_rules_dependencies()


load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

http_archive(
    name = "rules_xcodeproj",
    sha256 = "7967b372bd1777214ce65c87a82ac0630150b7504b443de0315ea52e45758e0c",
    url = "https://github.com/MobileNativeFoundation/rules_xcodeproj/releases/download/1.3.3/release.tar.gz",
)

load(
    "@rules_xcodeproj//xcodeproj:repositories.bzl",
    "xcodeproj_rules_dependencies",
)

xcodeproj_rules_dependencies()
