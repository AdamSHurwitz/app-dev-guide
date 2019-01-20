# Kotlin

[Resources](#Resources)

[Scoping Functions](#Scoping-Functions)

---

## Resources

[Community ](https://kotlinlang.org/community/)

[Documentation](https://kotlinlang.org/docs/reference/android-overview.html)

**Basics**
* [Syntax](https://kotlinlang.org/docs/reference/basic-syntax.html)
* [Getting started with Android and Kotlin](https://kotlinlang.org/docs/tutorials/kotlin-android.html)

**Advanced**
* [Android Frameworks Using Annotation Processing: Dagger, Butterknife, Data Binding, Auto-parcel and DBFlow](https://kotlinlang.org/docs/tutorials/android-frameworks.html)
* [Higher-Order Functions and Lambdas](https://kotlinlang.org/docs/reference/lambdas.html)
* [Anko - Intents, Alert Dialogs, Services, AsyncTasks, Logging](https://blog.jetbrains.com/kotlin/2015/05/advanced-features-of-anko/)

[Android Developers Guide - Sample Apps](https://developer.android.com/samples/?language=kotlin)

**Courses**

[Udacity - Kotlin Bootcamp for Programmers](https://www.udacity.com/course/kotlin-bootcamp-for-programmers--ud9011)

[Kotlin Koans](https://kotlinlang.org/docs/tutorials/koans.html) - [GitHub](https://github.com/Kotlin/kotlin-koans)

[Udemy - Kotlin for Beginners: Learn Programming With Kotlin](https://www.udemy.com/kotlin-course/)

[Treehouse - Kotlin for Java Developers](https://teamtreehouse.com/library/kotlin-for-java-developers)

**Books**

[Kotlin For Android Developers](https://leanpub.com/kotlin-for-android-developers)

## Scoping Functions

**Resources**

[Medium - Mastering Kotlin standard functions: run, with, let, also and apply](https://medium.com/@elye.project/mastering-kotlin-standard-functions-run-with-let-also-and-apply-9cd334b0ef84)

- **run**
- **with**
- **let**
- **also**
- **apply**

![Scoping Functions](images/scoping-functions.png)

_From 'Mastering Kotlin standard functions...' Medium_

`run` 

Encloses code and returns last object in scope.

    run { 
        if (firstTimeView) introView 
        else normalView 
        }.show()
- ie:

      error?.run {
          Log.e(LOG_TAG, "Price Data EventListener Failed.", error)
          return@EventListener
      }

`with`

    with(webview.settings) {
        javaScriptEnabled = true
       databaseEnabled = true
    }

`T.run`

Nullability check can be applied before running code.

    webview.settings?.run {
       javaScriptEnabled = true
       databaseEnabled = true
    }

`T.let`

Emits value.

    stringVariable?.let { optionalVar ->
        println("The length of this String is ${it.length} otherwise optionalVar.length")
    }

`T.apply`

Returns original value. Doesn't require it.

    fun createInstance(args: Bundle) 
        = MyFragment().apply { arguments = args }

    fun createIntent(intentData: String, intentAction: String) =
       Intent().apply { action = intentAction }
               .apply { data = Uri.parse(intentData) }

- ie:

        ContentDialogFragment()
           .newInstance(Bundle().apply { putParcelable(CONTENT_KEY, content) })
           .show(childFragmentManager, null)

`T.also`

Returns original value. Requires it.

    stringVariable?.also {
        println("The length of this String is ${it.length}")
    }

- ie:
    
        childFragmentManager
           .beginTransaction()
           .replace(R.id.dialog_content,
               YouTubeFragment().newInstance(
                  Bundle().also { it.putParcelable(CONTENT_KEY, content) }))
           .commit()