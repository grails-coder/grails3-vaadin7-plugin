# Vaadin 7 plugin for Grails 3.x

This is a fork from the original plugin: vaadin-for-grails/grails3-vaadin7-plugin

At the moment some enhancements to the plugin were made:
* Upgraded to vaadin 7.6.8.

Disclaimer: This is a not fully tested plugin, use it at your own risk, I'm not responsible for that.

The Vaadin 7 plugin integrates the [Vaadin Framework](https://vaadin.com/home) into Grails in an easy way.

## Build the plugin.
Download a copy of the project.
```bash
git clone https://github.com/grails-coder/grails3-vaadin7-plugin.git
```
Now on the downloaded local copy go to the grails3-vaadin7-plugin/vaadin7 folder and issue following commands.
```gradle
cd grails3-vaadin7-plugin/vaadin7
./gradlew clean
./gradlew build
./gradlew publishMavenPublicationToMavenLocal
```
Project is already configured to write to your local repo. If you want to write to a specific location make changes on
publishing > repositories on the build.gradle

## Quickstart
Now on the project you attempt to use the Vaadin make sure to have following configuration on the `build.gradle` file.

```gradle
buildscript {
    repositories {
        mavenLocal()
    }
}
```

Then, add the plugin dependency to your build script.

```gradle
compile 'org.grails.plugins:vaadin7:3.+'
```

Finally execute the grails command `grails vaadin-quickstart com.yourcompany` and run your app.
