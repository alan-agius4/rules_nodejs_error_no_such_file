http_archive(
    name = "build_bazel_rules_nodejs",
    url = "https://github.com/bazelbuild/rules_nodejs/archive/0.12.4.zip",
    strip_prefix = "rules_nodejs-0.12.4",
    sha256 = "c482700e032b4df60425cb9a6f8f28152fb1c4c947a9d61e6132fc59ce332b16",
)

load("@build_bazel_rules_nodejs//:package.bzl", "rules_nodejs_dependencies")
rules_nodejs_dependencies()

load("@build_bazel_rules_nodejs//:defs.bzl", "node_repositories")
node_repositories(
    package_json = ["//:package.json"], 
    preserve_symlinks = True,
    node_version = "10.3.0",
    yarn_version = "1.6.0",
)

load("@build_bazel_rules_nodejs//:defs.bzl", "nodejs_binary", "yarn_install")

yarn_install(
	name = "runtime_deps",
	yarn_lock = "//:yarn.lock",
	package_json = "//:package.json"
)