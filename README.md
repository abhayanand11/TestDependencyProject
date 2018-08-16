# TestDependencyProject

The project to demonstrate the creation of Android Archive (.aar)

**<u>Build steps:</u>**

1. Clone the repo
2. Run the gradle command on the cloned project directory './gradlew clean build'



**<u>Artifacts generated:</u>**

- ~\app\build\outputs\aar\app-debug.aar
- ~\app\build\reports\lint-results.html
- ~\app\build\reports\tests\



**<u>Things to notice:</u>**

1. Change build.gradle file for **apply plugin: 'com.android.application'** to **apply plugin: 'com.android.library'**.
2. **applicationId** should be removed as this will interfere with the application id defined in the main project and merge error will occur for AndroidManifest file.
3. Make sure not to set any attribute which can collide or get override by the main project's Manifest file.



**How to use the dependency module created (.aar) in other projects?**

1. Include the module from File>Project Structure>New Module>Import .JAR/.AAR Package
2. Then add the newly included module as the dependency or the app module.
3. Build the project and resolve the AndroidManifest merge error if any.
4. You are good to go :)

