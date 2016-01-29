# DHR Service Registry

Fork of [Digital Service Hub's Service Registry](https://github.com/digitalserviceshub/serviceregistry)

- Adds a new service data description model to service descriptions.
- Extends the existing API with CRUD operations for managing the service data description resources.

# Requirements

- [Maven 3.x](https://maven.apache.org)
- [MongoDb](https://www.mongodb.org)
- [Tomcat 7.0+](https://tomcat.apache.org)

# Building from source

Add build profile(s) to your local maven settings.xml and set parameters according to your environment

```
<profiles>
  <profile>
    <id>development</id>
    <properties>
      <auth.secret>[authentication secret]</auth.secret>
      <db.ip>[mongodb address]</db.ip>
      <db.port>[mongodb port]</db.port>
      <db.name>[mongodb database]</db.name>
      <db.user>[mongodb user name]</db.user>
      <db.pwd>[mongodb user password]</db.pwd>
      <as.ip>[service registry deployment address]</as.ip>
      <as.port>[service registry deployment port]</as.port>
      <mail.smtp.host>[smtp mail server host]</mail.smtp.host>
      <mail.smtp.port>[smtp mail server port</mail.smtp.port>
      <mail.smtp.timeout>[smtp mail service connection timeout]</mail.smtp.timeout>
    </properties>
  </profile>
  <profile>
    <id>testing</id>
    <properties>
      ...
    </properties>
   </profile>
  <profile>
  <profile>
    <id>production</id>
    <properties>
      ...
    </properties>
   </profile>
  <profile>
</profiles>
```

Build project with Maven by issuing following command in shell:

```
mvn clean install -P development
```

This builds the project with development environment profile.

# License

Copyright 2015 VTT Technical Research Centre of Finland Ltd.

Licensed under the [Apache License, Version 2.0](./LICENSE)
