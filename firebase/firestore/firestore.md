# Firestore

[Query](#Query)

[Security Rules](firestore-security-rules.md)

---

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