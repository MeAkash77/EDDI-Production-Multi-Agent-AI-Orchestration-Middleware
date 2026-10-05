FROM gcr.io/oss-fuzz-base/base-builder-jvm@sha256:6cd618d0e67c3e58a9071f4cfbaf9ded48f6b8fc984664a571ef994464f42486

# No Maven or JDK 25 needed — build.sh compiles only the 3 vendored
# utility classes with javac. JDK version is auto-detected (17 or 21).

COPY . $SRC/project
WORKDIR $SRC/project
COPY .clusterfuzzlite/build.sh $SRC/
