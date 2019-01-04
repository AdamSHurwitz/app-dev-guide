# Firestore

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

|[Firestore Security Rules](firestore-security-rules.md)|
|---|

## Query
**Resources**

[Perform simple and compound queries in Cloud Firestore](https://firebase.google.com/docs/firestore/query-data/queries)

|Query|Use
|:---|:---
|`db.collection("cities").whereEqualTo("capital",true).addSnapshotListener()`|Observes snapshot changes of a query getting multiple documents.
|`.whereEqualTo("capital",true).whereLessThan(value).whereGreaterThanOrEqualTo(value)`|[Compound queries](https://firebase.google.com/docs/firestore/query-data/queries#compound_queries) (Can only perform multiple range comparisons on same field.)
|`.orderBy("name")`
|`.orderBy("name", Direction.DESCENDING)`|Can chain **orderBy** multiple layers.
|`.limit(3)`
|`.whereGreaterThan("population",100).orderBy("population")`|Combining **where** and **orderBy** as long as using the same attribute.
|[**Paginate data with query cursors**](https://firebase.google.com/docs/firestore/query-data/query-cursors)
|`.startAt(value).endAt(value)` |Inclusive
|`startAfter(value).endBefore(value)`|Exclusive
|[Use a document snapshot to define the query cursor](https://firebase.google.com/docs/firestore/query-data/query-cursors#use_a_document_snapshot_to_define_the_query_cursor)
|[Paginate a query](https://firebase.google.com/docs/firestore/query-data/query-cursors#paginate_a_query) (based on last visible document)
|[Set multiple cursor conditions](https://firebase.google.com/docs/firestore/query-data/query-cursors#set_multiple_cursor_conditions)