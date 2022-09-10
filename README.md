# Annotated logging config parent POM v1.0.x
The parent POM which simplifies incorporation annotated-logging library into a project.

## How to use
In order to incorporate `annotated-logging` aspects with use of `annotated-logging-config-pom` into a project and turn 
`@LogBefore` and `@LogAfter` annotations into log statements (weave them into your project's code)
just use at as parent of a target POM file:
```xml
<parent>
    <groupId>com.wnowakcraft</groupId>
    <artifactId>annotated-logging-config-pom</artifactId>
    <version>1.0.3</version>
</parent>
```

## Optional configuration parameters
* **annotated-logging.version** - version of annotated-logging library. **Default**: 1.0.3
* **aspectj-maven-plugin.aspectj-version** - version of AspectJ's aspectjtools library. **Default**: 1.9.5
* **aspectj-maven-plugin.classes-dir** - directory with compiled classes which should be woven.  **Default**: ${project.build.directory}/classes
* **aspectj-maven-plugin.showWaveInfo** - [true/false] defines whether weaving information should be logged. **Default**: false
* **aspectj-maven-plugin.verbose** - [true/false] defines whether detailed logs from aspectj maven plugin should be displayed. **Default**: false
* **aspectj-maven-plugin.version** - version of aspectj maven plugin. **Default**: 1.14.0
* **java.version** - version of Java for compiled bytecode being woven.
  It needs to be consistent with class version of originally compiled classes. **Default**: 11
