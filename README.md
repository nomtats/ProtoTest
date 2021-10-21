This project demonstrates how proto definition can be accidentally included in an AAR.
Execute the following commands to confirm.

./gradlew  mylibrary:build
jar xvf ./mylibrary/build/outputs/aar/mylibrary-debug.aar classes.jar
jar tf classes.jar

This will show that the test.proto is included in the AAR file
