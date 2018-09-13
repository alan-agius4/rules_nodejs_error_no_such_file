load("@build_bazel_rules_nodejs//:defs.bzl", "nodejs_binary", "nodejs_test")

nodejs_binary(
	name = "rollup",
	node_modules = "@runtime_deps//:node_modules",
	entry_point = "rollup/bin/rollup",
	testonly = 1,
	visibility = ["//visibility:private"],
)

nodejs_test(
	name = "rollup_test",
	node_modules = "@runtime_deps//:node_modules",
	entry_point = "rollup/bin/rollup",
	templated_args = ["^\(json\|schema\|something\)$"],
	visibility = ["//visibility:private"],
)
