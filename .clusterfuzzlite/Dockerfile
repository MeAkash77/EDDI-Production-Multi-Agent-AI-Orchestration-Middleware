FROM gcr.io/oss-fuzz-base/base-builder-jvm@sha256:0108adb0c100ba1868f1ac857ce3d2ba0da15cdde16f1b20b985a81696fb85df

# No Maven or JDK 25 needed — build.sh compiles only the 3 vendored
# utility classes with javac. JDK version is auto-detected (17 or 21).

COPY . $SRC/project
WORKDIR $SRC/project
COPY .clusterfuzzlite/build.sh $SRC/
