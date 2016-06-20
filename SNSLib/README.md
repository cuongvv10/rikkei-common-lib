## This module can be added to Android Studio by:

* 1. Adding the following code to AndroidManifest.xml file under </application> tag:
```gradle
  <meta-data
            android:name="io.fabric.ApiKey"
            android:value="YOUR_API_KEY"/>
```		
  (Sign up Account at https://www.fabric.io and  goto https://fabric.io/kits/android/twitterkit/install to get YOUR_API_KEY)

* 2 Adding Gradle dependency at build.gradle file:
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
	...
   compile 'rikkei.android:SNSLib:1.0'
}
```

## How to use

* 1. Put statement: 
      RkTwitterUtils.init(Context context, String consumerKey , String consumerSecret)
	  to first line of onCreate() method of every Activity

* 2. Put statement: 
      RkTwitterUtils.getInstance().onActivityResult(requestCode, resultCode, data);
      to onActivityResult()  of activity
	  
* 3. Call util functions: 
	  RkTwitterUtils.login(...), RkTwitterUtils.logout(...), RkTwitterUtils.post(...)...

