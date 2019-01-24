# Cloud Functions

[Resources](#Resources)

[Terminal Commands](#Terminal-Commands)

---

## Resources

[Cloud Functions Intro](https://firebase.google.com/docs/functions/)

[Use cases](https://firebase.google.com/docs/functions/use-cases)

**[Get Started](https://firebase.google.com/docs/functions/get-started)**

**[From Firebase to BigQuery With Firebase Functions](https://blog.questionable.services/article/from-firestore-to-bigquery-firebase-functions/)**

[View logs in Firebase console](https://console.firebase.google.com/project/_/functions/logs?search=&severity=DEBUG)

[Environment configuration](https://firebase.google.com/docs/functions/config-env)

[Handling dependencies](https://firebase.google.com/docs/functions/handle-dependencies)

[Optimizing netowrking](https://firebase.google.com/docs/functions/networking)

[Tips & tricks](https://firebase.google.com/docs/functions/tips)

**YouTube**
- [Learn JavaScript Promises (Pt.1) with HTTP Triggers in Cloud Functions - Firecasts](https://www.youtube.com/watch?v=7IkUgCLr5oA&t)
- [Learn JavaScript Promises (Pt. 2) with a Firestore Trigger in Cloud Functions - Firecasts](https://www.youtube.com/watch?v=652XeeKNHSk&t)
- [Learn JavaScript Promises (Pt 3) for sequential and parallel work in Cloud Functions - Firecasts](https://www.youtube.com/watch?v=d9GrysWH1Lc)

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