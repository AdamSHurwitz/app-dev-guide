# RxKotlin

[Zip Functions](#Zip-Functions)

---

## Zip Functions

**Rx 2**

[.zip() with BiFunction](https://gist.github.com/AdamSHurwitz/7a65feb797301d52d90cafb32a5e5de6)

[.zip() with Function3]()

**Rx 1**

    Observable
       .compose(RxHelpers.IOAndMainThreadSchedulers())
       .doOnCompleted { ... }
       .subscribe({
          // Do something with 'it'.
        }, { 
          throwable -> //do something
        })
    
    Observable.zip(
       // Returns Observable.
       getPrice(...),
       getPrice(...),
       { gdax, binance ->
          // Do something.
       }).subscribe({ s -> 
          // Do something.
       }).unsubscribe()

    private fun getPrice(...) : Observable<Type> {
       return Observable.just(price)
    }
