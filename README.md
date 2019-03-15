# agent-java-junit5
[![Build Status](https://travis-ci.org/reportportal/agent-java-junit5.svg?branch=master)](https://travis-ci.org/reportportal/agent-java-junit5)
[ ![Download](https://api.bintray.com/packages/epam/reportportal/agent-java-junit5/images/download.svg) ](https://bintray.com/epam/reportportal/agent-java-junit5/_latestVersion)
[![Join Slack chat!](https://reportportal-slack-auto.herokuapp.com/badge.svg)](https://reportportal-slack-auto.herokuapp.com)
[![stackoverflow](https://img.shields.io/badge/reportportal-stackoverflow-orange.svg?style=flat)](http://stackoverflow.com/questions/tagged/reportportal)
[![UserVoice](https://img.shields.io/badge/uservoice-vote%20ideas-orange.svg?style=flat)](https://rpp.uservoice.com/forums/247117-report-portal)
[![Build with Love](https://img.shields.io/badge/build%20with-❤%EF%B8%8F%E2%80%8D-lightgrey.svg)](http://reportportal.io?style=flat)
---
# ReportPortal [JUnit5](https://junit.org/junit5/) Integration

The repository contains [JUnit5](https://junit.org/junit5/docs/current/user-guide/) Listener for [ReportPortal](http://reportportal.io/) integration.

## Getting Started

1. Create folders **_/META-INF/services_** in **_resources_**
2. Put there a file named **_org.junit.platform.launcher.TestExecutionListener_**
3. Supply a single row **_com.epam.reportportal.junit5.ReportPortalListener_** for default realization

__/META-INF/services/org.junit.platform.launcher.TestExecutionListener__
```xml
com.epam.reportportal.junit5.ReportPortalListener
```

If you desire to configure test *name*, *description* and *tags*:

Extend *ReportPortalListener*, override *getTestItem()* and replace *com.epam.reportportal.junit5.ReportPortalListener*
with fully qualified custom Listener class name in this file.
### Maven

```xml
<repositories>
    <repository>
        <id>bintray</id>
        <url>http://dl.bintray.com/epam/reportportal</url>
    </repository>
    <repository>
        <id>jitpack.io</id>
        <url>https://jitpack.io</url>
    </repository>
</repositories>

<dependency>
   <groupId>com.epam.reportportal</groupId>
   <artifactId>agent-java-junit5</artifactId>
   <version>$LATEST_VERSION</version>
</dependency>
```

### Gradle

```yml
repositories {
    jcenter()
    mavenLocal()
    maven { url "http://dl.bintray.com/epam/reportportal" }
    maven { url "https://jitpack.io" }
}

testCompile 'com.epam.reportportal:agent-java-junit5:$LATEST_VERSION'
```


# Copyright Notice

Licensed under the [Apache 2.0](https://www.apache.org/licenses/LICENSE-2.0) license (see the LICENSE.md file).