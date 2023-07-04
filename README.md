# AsciiDoc project template Maven archetype

The project incorporates a Maven archetype useful for creating [AsciiDoctor](https://docs.asciidoctor.org) documentation for IT projects

A target project is based on Maven, Docker and Nginx. It creates a complete environment for the development and maintenance of project documentation. An HTML-based web server that exposes documentation using compiled AsciiDoc files dockerized as an Nginx HTTP server. As a result, documentation could be deployed as a full-featured web server in various environments, starting from the local dev, through Kubernetes clusters to end with a broad range of cloud providers.

## Creating a new project based on the archetype

```shell
mvn archetype:generate                           \
  -DarchetypeGroupId=pl.sparkidea.maven          \
  -DarchetypeArtifactId=archetype-project-adoc   \
  -DarchetypeVersion=1.0-SNAPSHOT                \
  -DgroupId=<my.groupid>                         \
  -DartifactId=<my-artifactId>
```

Example:

```shell
mvn archetype:generate                           \
  -DarchetypeGroupId=pl.sparkidea.maven          \
  -DarchetypeArtifactId=archetype-project-adoc   \
  -DarchetypeVersion=1.0-SNAPSHOT                \
  -DgroupId=pl.sparkidea.demo                    \
  -DartifactId=doc-demo
```

## Current gaps

1. Add a project revision based on GIT commit (doc footer instead of `XX` placeholder)
2. Expose project versioning and GIT commit metadata
