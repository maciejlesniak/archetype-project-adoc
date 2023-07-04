#set($hash1 = '#')
#set($hash2 = '##')
#set($hash3 = '###')
#set($hash4 = '####')
${hash1} $groupId:$artifactId:$version

[//]: # (Project description starts here)

${hash2} Repository layout
// todo titles do not appear in generated mvn project

* `/nginx` - http server configuration
* `Dockerfile` - creates working Nginx-based http server image with copied html files from `/target/html` (default port is 8080)
* `src/asciidoc/system` - standard system error pages for 404 and 50x errors 
* `src/asciidoc/images` - standard images direcotry

${hash2} Usage

${hash3} AsciiDoc compilation using Maven

To create html5 documents
```shell
mvn clean asciidoctor:process-asciidoc@html5
```

To get rid of local `html` files that may resides in source directores `/src/asciidoc/**`
```shell
mvn clean:clean@clean-sources
```

${hash3} Serving compiled files using Nginx and Docker

Create a docekr image followed by running that image locally:
```shell
docekr build . -t doc:latest
docker run -p 8080:8080 doc:latest
```

${hash2} Dependencies and resources

In terms of AsciiDoc compilation and management, the project depends on `org.asciidoctor:asciidoctor-maven-plugin`. more information about the plugin usage, you could find in [official asciidoctor plugin page](https://docs.asciidoctor.org/maven-tools/latest/plugin/introduction/).


