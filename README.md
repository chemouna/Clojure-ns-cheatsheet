# Clojure-ns-guide

## CheatSheet

### require

###  use
    - use loads libraries and refers to their namespaces (giving you everything, which is usually/always overkill)
    
### [refer](https://clojuredocs.org/clojure.core/refer) : refers to all public vars of ns, subject to filters. 
    - Use :refer sparingly. It’s good for symbols that have no alphabetic characters, such as >! <! >!! <!! in core.async, or heavily-used macros such those in clojure.test.
    - You can combine :refer and :as in the same :require clause.
     

### as 
    - use loads libraries and refers to their namespaces (giving you everything, which is usually/always overkill)

## Examples 
