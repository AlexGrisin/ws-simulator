# Execute

## Start wiremock server (No Docker)

```
curl -O https://repo1.maven.org/maven2/com/github/tomakehurst/wiremock-standalone/2.26.3/wiremock-standalone-2.26.3.jar
java -jar wiremock-standalone-2.26.3.jar --global-response-templating --root-dir=stubs --port 9999
```

## Start wiremock server (With Docker)

- Docker build
```
docker build -t ws-simulator . 
```

- Docker run
```
docker run -it --rm -p 9999:8080 ws-simulator
```

- More info: https://hub.docker.com/r/rodolpheche/wiremock/

# Options

## Command line options

- Render all response definitions using Handlebars templates.
```
--global-response-templating
```
- Disable the request journal, which records incoming requests for later verification
```
--no-request-journal
```
- Turn on verbose logging to stdout
```
--verbose
```
- More info: http://new.wiremock.org/docs/running-standalone