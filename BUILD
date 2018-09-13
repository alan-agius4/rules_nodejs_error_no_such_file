load("@build_bazel_rules_nodejs//:defs.bzl", "nodejs_binary")


nodejs_binary(
	name = "rollup",
	node_modules = "@runtime_deps//:node_modules",
	entry_point = "rollup/bin/rollup",
	testonly = 1,
	visibility = ["//visibility:private"],
)