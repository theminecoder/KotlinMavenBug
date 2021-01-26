# Kotlin + Maven Intellij Import Bug

### Steps to reproduce

1. Create a blank intellij project and add each of the 3 modules to 
   it via File > New > Module From Existing Sources
2. `mvn install` parent
3. Make sure `common` version is `1.0-SNAPSHOT`
4. `mvn install` common
5. Change `common` version to `2.0-SNAPSHOT`
6. Reload maven projects

### Observations

Both maven and IntelliJ can actually build `app` when this situation 
is happening, however IntelliJ code completion and analysis just 
fails to resolve things.
