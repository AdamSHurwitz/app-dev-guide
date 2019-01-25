# Cloud Functions

[Resources](#Resources)

[Structure](#Structure)

[Terminal Commands](#Terminal-Commands)

---

## Resources

[Cloud Functions Intro](https://firebase.google.com/docs/functions/)

[Use cases](https://firebase.google.com/docs/functions/use-cases)

**[Get Started](https://firebase.google.com/docs/functions/get-started)**

[View logs in Firebase console](https://console.firebase.google.com/project/_/functions/logs?search=&severity=DEBUG)

[Environment configuration](https://firebase.google.com/docs/functions/config-env)

[Handling dependencies](https://firebase.google.com/docs/functions/handle-dependencies)

[Optimizing netowrking](https://firebase.google.com/docs/functions/networking)

[Tips & tricks](https://firebase.google.com/docs/functions/tips)

**YouTube**
- [Learn JavaScript Promises (Pt.1) with HTTP Triggers in Cloud Functions - Firecasts](https://www.youtube.com/watch?v=7IkUgCLr5oA&t)
- [Learn JavaScript Promises (Pt. 2) with a Firestore Trigger in Cloud Functions - Firecasts](https://www.youtube.com/watch?v=652XeeKNHSk&t)
- [Learn JavaScript Promises (Pt 3) for sequential and parallel work in Cloud Functions - Firecasts](https://www.youtube.com/watch?v=d9GrysWH1Lc)

**Other Use Cases**
- [How to Schedule (Cron) Jobs with Cloud Functions for Firebase](https://firebase.googleblog.com/2017/03/how-to-schedule-cron-jobs-with-cloud.html)
- [From Firebase to BigQuery With Firebase Functions](https://blog.questionable.services/article/from-firestore-to-bigquery-firebase-functions/)

**Samples**
- [Codelab](https://codelabs.developers.google.com/codelabs/firebase-cloud-functions/#0)
- [FirebaseExtended/user-data-protection](https://github.com/FirebaseExtended/user-data-protection)
- [firebase/functions-samples](https://github.com/firebase/functions-samples)
   - [bigquery-import](https://github.com/firebase/functions-samples/tree/master/bigquery-import) 
   - [coupon-on-purchase](https://github.com/firebase/functions-samples/tree/master/coupon-on-purchase)
   - [fcm-notifications](https://github.com/firebase/functions-samples/tree/master/fcm-notifications)
   - [child-count](https://github.com/firebase/functions-samples/tree/master/child-count)


## Structure

Dependencies: package.json

Sample endpoint: https://us-central1-cloud-functions-sample-496b1.cloudfunctions.net/addMessage?text=yourTextInput

## Terminal Commands
Used for Security Rules and Cloud Functions

Setup and Install: [Firebase CLI Reference](https://firebase.google.com/docs/cli/)

|Command|Use
|:---|:---|
| `firebase login`| 
| `firebase init`| Initializes cloud functions project
| `firebase use`| View list of defined aliases under firebaserc file
| `firebase use --add` | Add project id / alias to environment
| `firebase deploy --only functions` | Deploys all functions
| `firebase deploy --only functions:addMessage, functions:secondMethod, functions:thirdMessage` | Deploys specific function(s)
| `firebase functions:delete myFunction` | Delete function in all regions
| `firebase functions:delete myFunction --region us-east-1` |  Delete a specified function running in a specific region
|  `firebase functions:delete myFunction myOtherFunction` | Delete more than one function
|  `firebase functions:delete groupA` | Delete a specified functions group
|   `firebase functions:delete myFunction --force` | Bypass the confirmation prompt
| `firebase functions:log` | View logs (or use console)
| `firebase functions:log --only <FUNCTION_NAME>` | View log for specific funciton