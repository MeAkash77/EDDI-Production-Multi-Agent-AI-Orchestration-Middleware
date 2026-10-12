FROM gcr.io/oss-fuzz-base/base-builder-jvm@sha256:ae48328516584d236d0655e20793fe005bfb3d7975fcf3575d05bed3bc684d4b

# No Maven or JDK 25 needed — build.sh compiles only the 3 vendored
# utility classes with javac. JDK version is auto-detected (17 or 21).

COPY . $SRC/project
WORKDIR $SRC/project
COPY .clusterfuzzlite/build.sh $SRC/
