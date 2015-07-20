**syntax:**
```
object.Clone ' [jsCore]
```
`Clone()` method clones new object from `jsCore` object.

## Samples ##
```
<!--#include file="JSON_latest.asp"-->
<%
Dim o, p

Set o = jsObject()
o("name") = "tuğrul"
o("surname") = "topuz"
o.Flush

Set p = o.Clone
p("name") = "threedot"
p.Flush
%>
```