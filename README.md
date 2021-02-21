# android-support
A jar for all android-support related libraries (AndroidX included)

# Build
```bash
./gradlew :mylibrary:assemble
cd mylibrary/build/outputs/aar/
extract ./mylibrary-debug.aar
cd ./mylibrary-debug
mkdir support && cd support
find ../libs | xargs -i jar xvf {}
jar xvf ../classes.jar
jar cvf ../support.jar *
cd .. && ll ./support.jar
```
