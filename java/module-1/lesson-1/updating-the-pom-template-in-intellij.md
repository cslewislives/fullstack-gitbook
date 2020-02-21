---
description: Instructions to update your Pom file template.
---

# Updating the Pom Template In IntelliJ

Please review the attached video in you have not already updated your Pom template in IntelliJ. 

{% hint style="warning" %}
[Video to update the Pom Template](https://www.youtube.com/watch?v=KTfjWJB8X7Y)
{% endhint %}

Written instructions for this same activity are as follows:

1. Open IntelliJ so that it displays the Welcome dialog. 
2. Click the `Configure` menu drop down.
3. Select the `Preferences` \(Mac\) or `Settings` \(Windows\) menu item, this will display the **Preferences for New Projects** dialog.
4. Click on `Editor` in the left-hand pane.
5. Click on `File and Code Templates` in the right-hand pane, Code and File Templates will display in the right-hand pane.
6. There are 4 tabs \(Files, Includes, Code, and Other\). Click on the **Other** tab. This will display a list of "other" file templates.
7. Expand the `Maven` list item.
8. Click on the `Maven Project.xml` list item. This will display the template used to create the pom.xml file for Maven projects.
9. The template code looks like this:

```java
<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0"
         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
    <modelVersion>4.0.0</modelVersion>

#if (${HAS_PARENT})
    <parent>
        <groupId>${PARENT_GROUP_ID}</groupId>
        <artifactId>${PARENT_ARTIFACT_ID}</artifactId>
        <version>${PARENT_VERSION}</version>
#if (${HAS_RELATIVE_PATH})
        <relativePath>${PARENT_RELATIVE_PATH}</relativePath>
#end
    </parent>

#end
    <groupId>${GROUP_ID}</groupId>
    <artifactId>${ARTIFACT_ID}</artifactId>
    <version>${VERSION}</version>

    ${END}    
</project>
```

10. We want to insert the following XML just before the closing `</project>` tag:

```java
    <properties>
        <maven.compiler.source>1.8</maven.compiler.source>
        <maven.compiler.target>1.8</maven.compiler.target>
    </properties>
```

11. The updated template should now look like this:

```java
<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0"
         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
    <modelVersion>4.0.0</modelVersion>

#if (${HAS_PARENT})
    <parent>
        <groupId>${PARENT_GROUP_ID}</groupId>
        <artifactId>${PARENT_ARTIFACT_ID}</artifactId>
        <version>${PARENT_VERSION}</version>
#if (${HAS_RELATIVE_PATH})
        <relativePath>${PARENT_RELATIVE_PATH}</relativePath>
#end
    </parent>

#end
    <groupId>${GROUP_ID}</groupId>
    <artifactId>${ARTIFACT_ID}</artifactId>
    <version>${VERSION}</version>

    ${END}
    <properties>
        <maven.compiler.source>1.8</maven.compiler.source>
        <maven.compiler.target>1.8</maven.compiler.target>
    </properties>
    
</project>
```

12. Click `Apply` and then `OK`. This completes the update.

13. Now test the changes by creating a new Maven project \(following the steps outlined in Hello, World\).

14. The new project should come up displaying the pom.xml file for the project, which should look like this:

```java
<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0"
         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
    <modelVersion>4.0.0</modelVersion>

    <groupId>com.company</groupId>
    <artifactId>maventest</artifactId>
    <version>1.0-SNAPSHOT</version>


    <properties>
        <maven.compiler.source>1.8</maven.compiler.source>
        <maven.compiler.target>1.8</maven.compiler.target>
    </properties>

</project>
```

If it does, you have successfully completed this update. 

