**syntax:**
```
object.jsString ' [string]
```

`jsString` property returns JSON string.

## Samples ##
```
<!--#include file="JSON_latest.asp"-->
<%
Dim o
Set o = jsArray()
o(Null) = 0
o(Null) = 2
o(Null) = 4
o(Null) = 6
o(Null) = 8

Response.Write "this is JSON: " & o.jsString
%>
```