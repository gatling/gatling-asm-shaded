# gatling-asm-shaded

[ASM](https://asm.ow2.io/) repackaged (shaded) under the `io.gatling.internal.asm` namespace for internal use by Gatling.

## Build

```
mvn clean package
```

## Release

Releases are triggered by pushing a git tag. The tag format **must use 3 version parts** to be picked up correctly by `maven-git-versioning-extension`:

```
git tag v9.10.0
git push origin v9.10.0
```

A tag like `v9.10` (2 parts) will **not** be recognized and the release will fail with version `0.0.0`.

The release workflow signs the artifacts and publishes them to Maven Central automatically.
