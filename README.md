# InfluxDB container for ppc64le

This was a container build of [InfluxDB](https://www.influxdata.com/) for **ppc64le** systems.

**It is no longer maintained**.

These builds use the source code from <https://github.com/influxdata/influxdb>.

At the moment, two versions are available, namely:

- v1.8.0
- v2.0.0-beta.13

For **v1.8.0**, I used the commit tagged `v1.8.0`, and created a custom `Dockerfile`,
available in `Dockerfile-v1.8.0-ppc64le`, which builds the images by:

- Installing build tools as per `Dockerfile_build_ubuntu64` in the source (modified only to change `$GOARCH`)
- Building the code using the `build.py` script in the source
- Copying the necessary files from this builder image to a final image

For **v2.0.0-beta.13** no changes were required - I just built an image using the `Dockerfile` in the source ;-)
