# Camunda-Gradle Spring Boot demo
> Include swagger

## Execution
> Run `CamundaSwaggerApplication.java`
> 
> Shorten command line: `none` or `@argfile(Java 9+)`

## Execute jar
> Run gradle script `bootJar` or `assemble`
> 
> Run `java -jar camunda-swagger-0.0.1-SNAPSHOT.jar`

## Not working
> Gradle RUN will not find static files of camunda
>
> Shorten command line: `JAR manifest`

### Why it's not working?
Follow `ProcessEnginesFilter` one of camunda's classes
``` java
this.pluginPackageFormat = "{ name: '%s-plugin-%s', " +
      "location: '%s%s/api/%s/plugin/%s/static/app', main: 'plugin.js' }";
```

### Go to
> Camunda UI `http://localhost:8888/` (admin/admin)
>
> Swagger UI `http://localhost:8888/swagger-ui/`