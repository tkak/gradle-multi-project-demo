# gradle-multi-project-builds-demo

![CI](https://github.com/tkak/gradle-multi-project-builds-demo/workflows/CI/badge.svg)

Demo for Gradle multi-project builds with cloud native buildpacks

## Build with pack

`BP_GRADLE_BUILT_ARTIFACT` environment variable is needed in case of Gradle multi-project builds.

```
$ pack build greeter --env "BP_GRADLE_BUILT_ARTIFACT=greeter/build/libs/*.[jw]ar" \
    --builder=gcr.io/paketo-buildpacks/builder:base
```
