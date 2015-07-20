**syntax:**
```
object.Remove("property")
```

`Remove()` method removes defined property.

## Samples ##

```
<!--#include file="JSON_latest.asp"-->
<%
Dim o
Set o = jsObject()

o("name") = "tuğrul"
o("surname") = "topuz"

o.Flush
o.Remove("surname")
o.Flush
%>
```