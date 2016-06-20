## This module can be used in Android Studio by:

* Adding the following code to AndroidManifest.xml file under </application> tag:
```gradle
  <meta-data
            android:name="io.fabric.ApiKey"
            android:value="YOUR_API_KEY"/>
```		(Sign up Account and follow the instructions to get YOUR_API_KEY)
		
		
 * Adding Gradle dependency:
```gradle

buildscript {
  repositories {
    maven { url 'https://maven.fabric.io/public' }
  }

  dependencies {
    // The Fabric Gradle plugin uses an open ended version to react
    // quickly to Android tooling updates
    classpath 'io.fabric.tools:gradle:1.+'
  }
}

apply plugin: 'io.fabric'

repositories {
  maven { url 'https://maven.fabric.io/public' }
}


dependencies {
   compile 'rikkei.android:SNSLib:1.0'
}
```



