**syntax:**
```
object.Pair("property")
object.Pair(Null)
object("property")
object(Null)
```

`Pair()` method manuplates data structure on the jsCore object. If property have a `Null` value then taken an autoproperty. Autoproperties contain an ordered numbers.

## Samples ##
```
<!--#include file="JSON_latest.asp"-->
<%
Dim n
Set n = jsObject()

n.Pair("name") = "tuğrul"
n("surname") = "topuz"
n(Null) = Array(2, 4, 6, 8)
n(Null) = "the end"

n.Flush
%>
```
### Value contains jsCore objects (jsArray, jsObject) or primitive types ###
```
<!--#include file="JSON_latest.asp"-->
<%
Dim m, i
Set m = jsArray()

Sub AddUser(name, surname)
        Set m(Null) = jsObject()
        m(Null)("name") = name
        m(Null)("surname") = surname
End Sub

AddUser "tuğrul", "topuz"
AddUser "nasrettin", "hoca"
AddUser "cin", "ali"

m.Flush
%>
```