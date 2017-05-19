# OpenUri
adapt the file provider permission for android 7.0  

* no need to worry about the manifest.xml

* just 2 lines of java code

* no need to care about the specific path, all path is permission granted temporary, so you can use the file object as usual

  ​

# usage

```
Uri uri = OpenUri.fromFile(context,file);

OpenUri.addPermissionRW(intent);
//or only read by addPermissionR
```

then you can use the intent as usual:

```
 intent.setDataAndType(uri, "image/*");
  ...
```






# gradle:

Step 1. Add the JitPack repository to your build file

Add it in your root build.gradle at the end of repositories:

```
allprojects {
    repositories {
        maven { url "https://jitpack.io" }
    }
}
```

Step 2. Add the dependency

```java
dependencies {
        compile 'com.github.hss01248:OpenUri:Latest release'
}
```
Latest release: https://github.com/hss01248/OpenUri/releases