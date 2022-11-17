# CRC32C build in bazel

author: dxyinme

you can use it like this 
```bash
# in workspace
git_repository(
    name = "com_github_dxyinme_crc32c",
    remote = "https://github.com/dxyinme/bazel_crc32c.git",
    branch = "main",
)

# in use
cc_binary(
  name = "crc32c_example",
  srcs = [
    "crc32c_example.cc",
  ],
  deps = [
    "@com_github_dxyinme_crc32c//:crc32c"
  ],
)
```