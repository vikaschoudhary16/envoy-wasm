licenses(["notice"])  # Apache 2

# Use a wrapper cc_library with an empty source source file to force
# compilation of other cc_library targets that only list *.a sources.
cc_library(
    name = "all_external",
    srcs = [":empty.cc"],
    defines = ["OPENTRACING_STATIC"],
    deps = [
        "@com_github_datadog_dd_opentracing_cpp//:dd_opentracing_cpp",
        "@com_google_googletest//:gtest",
        "@com_lightstep_tracer_cpp//:lightstep_tracer",
        "@io_opentracing_cpp//:opentracing",
    ],
)

genrule(
    name = "empty_cc",
    outs = ["empty.cc"],
    cmd = "touch \"$(@D)/empty.cc\"",
)
