# Clojure-ns-guide

## CheatSheet

### require

###  use
    - use loads libraries and refers to their namespaces (giving you everything, which is usually/always overkill)
    - use goes the extra step and creates mappings for the stuff in the require'd namespace in the current namespace. That way, rather than doing some.namespace/name you're just referring to it as name. While this is convenient sometimes, it's better to use require or select the individual vars that you want rather than pull in the entire namespace. Otherwise, you could have issues with shadowing (where one var is preferred over another of the same name).
    - If you don't want to use require, but you know what vars you want out of the namespace, you can do this:
```clojure
(ns whatever
(:use [some.namespace :only [vars you want]]))
```
  
### [refer](https://clojuredocs.org/clojure.core/refer) : refers to all public vars of ns, subject to filters. 
    - Use :refer sparingly. It’s good for symbols that have no alphabetic characters, such as >! <! >!! <!! in core.async, or heavily-used macros such those in clojure.test.
    - You can combine :refer and :as in the same :require clause.
     

### as 
    - use loads libraries and refers to their namespaces (giving you everything, which is usually/always overkill)
     example :   
     ```clojure
     (:refer-clojure :exclude [filter remove seq])
     ```
     equivalent to 
     ```clojure
     (refer 'clojure.core :exclude [filter remove])
     ```
     
### :refer-clojure 
   - Same as (refer 'clojure.core <filters>)

### Tips
    - try to only use :require and :use inside of (ns ...). It's much cleaner this way. Don't use and require outside of (ns ..) unless you have a pretty good reason for it.

## Examples 
