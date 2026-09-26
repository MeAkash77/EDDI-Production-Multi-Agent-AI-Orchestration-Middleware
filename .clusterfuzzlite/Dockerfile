FROM gcr.io/oss-fuzz-base/base-builder-jvm@sha256:20bd545f939f24cf521852d1bbcdbe4e24231d3e2c1278ce846c751bc70768d7

# No Maven or JDK 25 needed — build.sh compiles only the 3 vendored
# utility classes with javac. JDK version is auto-detected (17 or 21).

COPY . $SRC/project
WORKDIR $SRC/project
COPY .clusterfuzzlite/build.sh $SRC/
