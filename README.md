# optimizationbenchmarking/evaluator-runtime

[![Image Layers and Size](https://imagelayers.io/badge/optimizationbenchmarking/evaluator-runtime:latest.svg)](https://imagelayers.io/?images=optimizationbenchmarking%2Fevaluator-runtime:latest)
[![Docker Pulls](https://img.shields.io/docker/pulls/optimizationbenchmarking/evaluator-runtime.svg)](https://hub.docker.com/r/optimizationbenchmarking/evaluator-runtime/)
[![Docker Stars](https://img.shields.io/docker/stars/optimizationbenchmarking/evaluator-runtime.svg)](https://hub.docker.com/r/optimizationbenchmarking/evaluator-runtime/)

The current version of this image is 0.8.5.

## Components

This is the runtime environment for the optimizationBenchmarking evaluator. It extends [`debian:8.4`](https://hub.docker.com/r/library/debian/tags/8.4/) with the necessary tools in the right configuration, including:

- [`Java 8 OpenJDK`](http://openjdk.java.net/projects/jdk8/)
- [`TeX Live`](http://www.tug.org/texlive/)
- [`ghostscript`](http://ghostscript.com/)
- [`R`](https://www.r-project.org/)

For [`R`](https://www.r-project.org/) we automatically pre-install libraries which may be needed by our software, namely

- [`apcluster`](https://cran.r-project.org/web/packages/apcluster/index.html)
- [`cluster`](https://cran.r-project.org/web/packages/cluster/index.html)
- [`fpc`](https://cran.r-project.org/web/packages/fpc/index.html)
- [`mclust`](https://cran.r-project.org/web/packages/mclust/index.html)
- [`NbClust`](https://cran.r-project.org/web/packages/NbClust/NbClust.pdf)
- [`stats`](http://stat.ethz.ch/R-manual/R-patched/library/stats/html/stats-package.html)
- [`vegan`](https://cran.r-project.org/web/packages/vegan/index.html)

We pin the versions of `R` to `3.3.*` and `ghostscript` to `9.06*`, while we expect that version changes of Tex Live and Java will not lead to any issues.

## Usage

You can run this image by using:

    docker run --rm -t -i optimizationbenchmarking/evaluator-runtime:<VERSION>
	
to look around in the image.