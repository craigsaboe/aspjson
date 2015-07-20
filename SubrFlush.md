**syntax:**
```
object.Flush
```

`Flush` subroutine sends JSON string to standart output.

## Samples ##

```
<!--#include file="JSON_latest.asp"-->
<%
Dim o
Set o = jsObject()
o("build") = "2.0.2"
o.Flush
%>
```