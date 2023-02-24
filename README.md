README 
====

## Build with cmake

```
javac -h . src/main/java/com/damonyuan/jni/HelloWorldJNI.java
cmake -S . -B build
cmake --build build
```

## Build with g++/clang

```
javac -h . HelloWorldJNI.java
g++ -v -c -fPIC -I${JAVA_HOME}/include -I${JAVA_HOME}/include/darwin com_damonyuan_jni_HelloWorldJNI.cpp -o com_damonyuan_jni_HelloWorldJNI.o
g++ -v -dynamiclib -o libsbmc.dylib com_damonyuan_jni_HelloWorldJNI.o  -lc
```

## Notes

1. in Mac M1, please install the arm version of JDK.