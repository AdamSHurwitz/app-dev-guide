# Google Cloud Platform

[Java/Kotlin App](#Java-/-Kotlin-App)

[Terminal Commands](#Terminal-Commands)

---

## Java / Kotlin App

Build Gradle App

1. [Getting started with Gradle](https://www.jetbrains.com/help/idea/getting-started-with-gradle.html)
2. [Make call using Retrofit](https://futurestud.io/tutorials/retrofit-2-beyond-android-retrofit-for-java-projects)
3. Save data into Firebase
   - [Installation & Setup for REST API](https://firebase.google.com/docs/database/rest/start)

**Scheduling**
- [TimerTask](https://stackoverflow.com/questions/22163662/how-to-create-a-java-cron-job)
- [Scheduling Tasks With Cron for Java](https://cloud.google.com/appengine/docs/standard/java/config/cron)
- [Scheduling Jobs With cron.yaml](https://cloud.google.com/appengine/docs/flexible/java/scheduling-jobs-with-cron-yaml)

## Terminal Commands

**SDK**

|View||
|---|---|
|`gcloud topic configurations`| About configurations.
|`gcloud config list`|	List properties in active configuration.
|`gcloud config configurations describe [NAME]`|	List properties in specific configuration.
|`gcloud config configurations list`|	List all configurations.

|Edit||
|---|---|
|`gcloud auth application-default login`|	Authenticate
|`gcloud config configurations create [NAME]`| Create configuration. (need to activate after creation)
|`gcloud config configurations activate [NAME]`| Activate / switch between projects.
|`gcloud config set project [PROJECT_ID]`| Set project.
|`gcloud config set account [EMAIL@DOMAIN.COM]`| Set account.
|`gcloud config configurations delete [NAME]`| Delete configuration.
|`gradle appengineRun`| Run standard application
|`gradle appengineStop`| Stop standard application
|`gradle jettyRun`| Run flexible application

**Deployed**

|View||
|---|---|
|`gcloud app versions list`|List deployed versions.
|`gcloud app logs tail -s default`|See app logs.

|Edit||
|---|---|
|`gradle appengineDeploy`|Deploy
|`gcloud app browse`|Launches app. (local: http://localhost:8080/ or hosted: https://projectName.appspot.com/). Useful for debugging.
|`gcloud app versions stop VERSIONS appVersion`|Stop deployed version.
|`gcloud app services delete service`|Delete service.