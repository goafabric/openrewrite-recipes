# Description
- Openrewrite Recipe mainly for Gradle Projects
- For a short Video see: https://youtu.be/HiiOVnhPx3I?si=h9etNakRzUDJON1N
- Upgrades for 
  - Spring Boot 4.0.0
  - Spring Batch
  - Adherent Starters for both implementation and test 
  - Kotlin Null Safety Fixes (starting point)
- Configures for maximum backwords compatibility (e.g. Jackson)
- ApplicationBaseRuntimeHints features Native Runtime Hints currently missing in Spring Boot 4.0 Stack
 
# Concerning Gradle Projects
- Can be simply added to your projects by
  - Adding rewrite.yml
  - Adding Openrewrite Plugin to build.gradle(.kts)
  - Adding rewrite section with Recipes to build.gradle(.kts)
  - Executing ./gradlew rewriteRun

# Concerning Maven Projects
- Though not yet designed for Maven, this recipe can be adopted
- For an example see pom.xml
- Sections in rewrite.yml need to me changed from "org.openrewrite.gradle" to "org.openrewrite.maven"
- Execute mvn rewrite:run

# Known Limitations
- Projects should be on Spring Boot 3.5 already

- Openrewrite execution is currently not compatible with Java25
  - https://github.com/openrewrite/rewrite/issues/6132

- Openrewrite execution is currently only partly compatible with Kotlin 2.x Projects
  - https://github.com/openrewrite/rewrite/issues/6007

# Links
Spring Boot Upgrade Guide
- https://github.com/spring-projects/spring-boot/wiki/Spring-Boot-4.0-Migration-Guide

Official Openrewrite Docs
- https://docs.openrewrite.org/