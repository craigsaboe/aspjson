**syntax:**
```
object.Kind ' [Number]
```

`Kind` property contains `JSON_OBJECT` or `JSON_ARRAY` values only.

If initialize an object with `jsObject()` method, that contains `JSON_OBJECT` const's value. If initialize an object with `jsArray()` method, that contains `JSON_ARRAY` const's value.

## Samples ##
Convert to jsObject from jsArray fastly.
```
<!--#include file="JSON_latest.asp"-->
<%
Dim n
Set n = jsObject()

n("is1") = "cin"
n("is2") = "ali"
n("is3") = 55

n.Flush
n.Kind = JSON_ARRAY
n.Flush

%>
```