# Firestore

## Terminal Commands
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

|[Firestore Security Rules](firestore-security-rules.md)|
|---|