# libphonenumber-cljs

[Google's libphonenumber](https://github.com/googlei18n/libphonenumber) packaged for use from clojurescript.

## Usage

Add dependency: `[nberger/libphonenumber-cljs "0.1.0-SNAPSHOT"]`

Use it:

```clojure

(ns foo.core
  (:import [i18n.phonenumbers PhoneNumberUtil]))

(def phone-util (.getInstance PhoneNumberUtil))

(defn valid-phone? [phone]
  (->> (.parse phone-util phone "US")
       (.isPossibleNumber phone-util)))
```

## License

Copyright © 2015 Nicolás Berger

Distributed under the Eclipse Public License either version 1.0 or (at
your option) any later version.
