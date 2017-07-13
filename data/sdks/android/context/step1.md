```gradle
allprojects {
    repositories {
        maven{ url "https://maven.google.com" }
        maven {
            url  "http://dl.bintray.com/flybits-inc/v3"
        }
        jcenter()
    }
}
```
