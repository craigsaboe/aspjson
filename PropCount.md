**syntax:**
```
object.Count ' [Number]
```

`Count` property contains object's items count.

## Samples ##

```
<!--#include file="JSON_latest.asp"-->
<%
Dim o
Set o = jsObject()

o(Null) = "ali"
Response.Write o.Count
o(Null) = 43
Response.Write o.Count

o.Flush
%>
```