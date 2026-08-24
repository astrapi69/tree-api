## Change log
----------------------

Version 2.2.2-SNAPSHOT
-------------

Version 2.2.1
-------------

ADDED:

- new github-actions workflow publish.yml for publishing to Maven Central via the Central Portal on a RELEASE-* tag push

CHANGED:

- documented the ITree contract, the gen-tree reference implementation and the tree-kit TypeScript sibling in the README

Version 2.2
-------------

CHANGED:

- update to jdk version 21
- migrated publishing to the Sonatype Central Portal (releases over the OSSRH staging API, snapshots to central.sonatype.com) with in-memory GPG signing from GPG_PRIVATE_KEY/GPG_PASSPHRASE or credentials from CENTRAL_USERNAME/CENTRAL_PASSWORD
- updated gradle wrapper to new version 9.7.0
- new gradle plugin org.gradle.toolchains.foojay-resolver-convention in version 1.0.0 for automatic JDK provisioning
- replaced the license-gradle-plugin with the spotless licenseHeaderFile step and added src/main/resources/license-header.txt
- removed the grgit gradle plugin; the tagRelease task now uses a plain git Exec task in gradle/tagging.gradle, so the gradle configuration cache works without workarounds
- enabled the gradle configuration cache
- removed unused test dependencies commons-text, gradle-migration-data, silly-io, file-worker and meanbean
- added Makefile with build, test, release and publish targets
- github-actions workflow: removed obsolete ossrh secrets, updated setup-gradle to v4 and added codecov-action v5

### Gradle Plugins
- **com.diffplug.spotless:com.diffplug.spotless.gradle.plugin**
    - Updated from `7.0.0.BETA2` to `7.0.0.BETA4`

- **io.freefair.lombok:io.freefair.lombok.gradle.plugin**
    - Updated from `8.10` to `8.11`
    - [Repository](https://github.com/freefair/gradle-plugins)

- **nl.littlerobots.version-catalog-update:nl.littlerobots.version-catalog-update.gradle.plugin**
    - Updated from `0.8.4` to `0.8.5`
    - [Repository](https://github.com/littlerobots/version-catalog-update-plugin)

- **org.ajoberstar.grgit:org.ajoberstar.grgit.gradle.plugin**
    - Updated from `5.2.2` to `5.3.0`
    - [Repository](https://github.com/ajoberstar/grgit)

### Libraries
- **io.github.astrapi69:file-worker**
    - Updated from `17.4` to `19.0`
    - [Repository](https://github.com/astrapi69/file-worker)

- **io.github.astrapi69:gradle-migration-data**
    - Updated from `2.4` to `3.0`
    - [Repository](https://github.com/astrapi69/gradle-migration-data)

- **io.github.astrapi69:silly-io**
    - Updated from `3.1` to `3.4`
    - [Repository](https://github.com/astrapi69/silly-io)

- **org.apache.logging.log4j:log4j-core**
    - Updated from `2.17.1` to `3.0.0-beta3`
    - [Repository](https://logging.apache.org/log4j/3.x/)

- **org.junit.jupiter:junit-jupiter**
    - Updated from `5.11.1` to `5.11.3`
    - [Repository](https://junit.org/junit5/)

- **org.junit.platform:junit-platform-launcher**
    - Updated from `1.11.1` to `1.11.3`
    - [Repository](https://junit.org/junit5/)

- **org.projectlombok:lombok**
    - Updated from `1.18.34` to `1.18.36`
    - [Repository](https://projectlombok.org)

## Gradle Release Candidate Update
- **Gradle**
    - Updated from `8.10.2` to `8.11.1`

Version 2.1
-------------

CHANGED:

- update gradle to new version 8.10.2
- update of test dependency junit-jupiter to new minor version 5.11.1
- update of test dependency junit-platform-launcher to new minor version 1.11.1

Version 2
-------------

ADDED:

- new libs.versions.toml file for new automatic catalog versions update

CHANGED:

- rename of module to new name 'io.github.astrapisixtynine.tree.api'
- update to jdk version 17
- update gradle to new version 8.10
- update of lombok version to 1.18.34
- update of gradle-plugin dependency 'spotless-plugin-gradle' to new minor version 7.0.0.BETA2
- update of gradle-plugin dependency 'grgit-gradle' to new minor version 5.2.2

Version 1.5
-------------

ADDED:

- new method 'addChild' to insert a child tree node with a specific given index
- new method 'getChildAt' to get an optional of the child tree node with the given index
- new method 'getChildIndex' to the index from the given child tree node

CHANGED:

- update gradle to new version 8.3

Version 1.4
-------------

ADDED:

- new method 'isAncestor' in interface ITree created that checks if a given tree node is an ancestor of this tree node
- new method 'isDescendant' in interface ITree created that checks if a given tree node is a descendant of this tree node
- new method 'move' in interface ITree created that moves a given tree node to the given new parent tree node

CHANGED:

- update gradle to new version 8.3-rc-4
- update of gradle-plugin dependency 'lombok-plugin' to new minor version 8.2.2
- update of gradle-plugin dependency 'spotless-plugin-gradle' to new minor version 6.20.0
- update of test dependency junit-jupiter-* to new minor version 5.10.0

Version 1.3
-------------

ADDED:

- new method 'isChild' in interface ITree created that checks if a given tree node is the child of this tree node

CHANGED:

- update gradle to new version 8.2-rc-2
- update of lombok version to 1.18.28
- update of gradle-plugin dependency 'spotless-plugin-gradle' to new minor version 6.19.0
- update of gradle-plugin dependency 'grgit-gradle' to new minor version 5.2.0
- javadoc optimized

Version 1.2
-------------

ADDED:

- new method 'hasPreviousSibling' in interface ITree created that checks if a node has a previous sibling
- new method 'hasNextSibling' in interface ITree created that checks if a node has a next sibling

CHANGED:

- javadoc optimized

Version 1.1
-------------

ADDED:

- new export for other modules can use ITree interface

Version 1
-------------

ADDED:

- new CHANGELOG.md file created

Notable links:
[keep a changelog](http://keepachangelog.com/en/1.0.0/) Don’t let your friends dump git logs into changelogs
