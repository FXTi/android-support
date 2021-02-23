# android-support
A jar for all android-support related libraries (AndroidX included)

In root of repo, there' re support.jar & support-stub.jar. They' re product of this repo and mkstub. Just use them! : )

# Build
```bash
./gradlew :mylibrary:assemble
cd mylibrary/build/outputs/aar/
extract ./mylibrary-debug.aar
cd ./mylibrary-debug
mkdir support && cd support
find ../libs | xargs -i jar xvf {}
jar xvf ../classes.jar
rm -rf com/pwn/myapplication
jar cvf ../support.jar *
cd .. && ll ./support.jar
```
