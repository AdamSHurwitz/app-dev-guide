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
          //do something with it
        }, { 
          throwable -> //do something
        })
    
    Observable.zip(
         //returns Observable
       getPrice(...),
       getPrice(...),
       { gdax, binance ->
          //do something
       }).subscribe({ s -> 
          //do something
       }).unsubscribe()

    private fun getPrice(...) : Observable<Type> {
       return Observable.just(price)
    }
