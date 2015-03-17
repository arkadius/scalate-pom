Scalate Maven POM
=================

Shared parent POM for Scalate Maven projects.

######: Deployment notes:
The Maven `distributionManagement` element is defined for this (and all inheriting projects unless overridden) as:
```xml
  <distributionManagement>
    <snapshotRepository>
      <id>sonatype-oss</id>
      <url>https://oss.sonatype.org/content/repositories/snapshots/</url>
    </snapshotRepository>
    <repository>
      <id>sonatype-oss</id>
      <url>https://oss.sonatype.org/service/local/staging/deploy/maven2/</url>
    </repository>
  </distributionManagement>
```
To deploy a snapshot or release, ensure that your loaded Maven `settings.xml` file contains the following:
```xml
<settings>
  <servers>
    <server>
      <id>sonatype-oss</id>
      <username>your-sonatype-jira-id</username>
      <password>your-sonatype-jira-pwd</password>
    </server>
  </servers>
</settings>
```
