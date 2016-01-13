# Description
Docker image with all the commonly used tools to build Java applications on Jenkins slaves.

# Supported tags and respective `Dockerfile` links
- [`latest` (_latest/Dockerfile_)](https://github.com/HearstAT/docker-hhi-build-tools/tree/master/Dockerfile)
- [`JDK6-MVN2.2.1` (_JDK6-MVN2.2.1/Dockerfile_)](https://github.com/HearstAT/docker-hhi-build-tools/tree/master/JDK6/MVN2.2.1/Dockerfile)
- [`JDK6-MVN3.0.4` (_JDK6-MVN3.0.4/Dockerfile_)](https://github.com/HearstAT/docker-hhi-build-tools/tree/master/JDK6/MVN3.0.4/Dockerfile)
- [`JDK7-MVN2.2.1` (_JDK7-MVN2.2.1/Dockerfile_)](https://github.com/HearstAT/docker-hhi-build-tools/tree/master/JDK7/MVN2.2.1/Dockerfile)
- [`JDK7-MVN3.0.4` (_JDK7-MVN3.0.4/Dockerfile_)](https://github.com/HearstAT/docker-hhi-build-tools/tree/master/JDK7/MVN3.0.4/Dockerfile)
- [`JDK8-MVN2.2.1` (_0JDK8-MVN2.2.1/Dockerfile_)](https://github.com/HearstAT/docker-hhi-build-tools/tree/master/JDK8/MVN2.2.1/Dockerfile)
- [`JDK8-MVN3.0.4` (_JDK8-MVN3.0.4/Dockerfile_)](https://github.com/HearstAT/docker-hhi-build-tools/tree/master/JDK8/MVN3.0.4/Dockerfile)

# How to use this Docker image
This Docker image is intended to be used with the [Jenkins Docker Plugin](https://wiki.jenkins-ci.org/display/JENKINS/Docker+Plugin). It can be utilized via the SSH connector or JNLP.

## SSH Connect
- Username: jenkins
- Password: jenkins

## JNLP
To run this Docker container

```
docker run hearsthi/jenkins-build-tools -url http://jenkins-server:port <secret> <slave name>
```

optional environment variables:
- `JENKINS_URL`: url for the Jenkins server, can be used as a replacement to `-url` option, or to set alternate jenkins URL
- `JENKINS_TUNNEL`: (`HOST:PORT`) connect to this slave host and port instead of Jenkins server, assuming this one do route TCP traffic to Jenkins master. Useful when when Jenkins runs behind a load balancer, reverse proxy, etc.

# Docker image details
- OS: Ubuntu 15.04
- Jenkins slave.jar (aka remoting.jar)
  - All Tags = 2.9

# Docker image details
- OS: Ubuntu 15.04
- Common tools: unzip, wget, curl, git
- Make (latest)
  - All Tags = 4.0-8.1

- gcc (latest)
  - All Tags = 4.9.2-10ubuntu13

- Java: JDK 6|7|8 (Depending on tag or dockerfile)
- Ruby/Ruby-Dev
  - All Tags = 2.3

- Python
  - All Tags = 2.7

- Maven located in `/usr/share/maven/`
  - Tagged Versions
    - Latest = 3.3.9
    - JDK(6|7|8)-MVN2.2.1 = 2.2.1
    - JDK(6|7|8)-MVN3.0.4 = 3.0.4

- Web Browser tests: XVFB
  - All Tags = 2:1.17.1-0ubuntu3.1

- Firefox at `/usr/bin/firefox`
  - All Tags = 43.0.4

- Selenium at `/opt/selenium/selenium-server-standalone.jar`
  - All Tags = 2.48.2

- Cucumber
  - All Tags = 2.2.0

- MySQL Client (latest)
  - All Tags = 5.6.27

# About this repository
This repository is available on [github.com/HearstAT/docker-hhi-build-tools/](https://github.com/HearstAT/docker-hhi-build-tools), and the automated build is on the [Docker Hub](https://hub.docker.com/r/hearsthi/jenkins-build-tools/).

## Supported Docker versions
This image has been tested with Docker version:
- 1.9.1
- 1.9.0

# User Feedback
## Issues
If you have any problems with or questions about this image, please submit a [GitHub issue](https://github.com/HearstAT/docker-hhi-build-tools/issues).

# License
The cloudbees/java-build-tools image is licensed under the [Apache License, Version 2.0](https://www.apache.org/licenses/LICENSE-2.0), and this repository is too:

```
Copyright 2015 CloudBees, Inc


Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```
