**syntax:**
```
toJSON(variant) ' [string]
```

All primitive datatypes and jsCore object convert to JSON string.

## Samples ##

```
<!--#include file="JSON_latest.asp"-->
<%
Response.Write toJSON("やあ")
%>
```

```
<!--#include file="JSON_latest.asp"-->
<%
Response.Write toJSON("hello")
%>
```

```
<!--#include file="JSON_latest.asp"-->
<%
Response.Write toJSON(Array("cin", "ali", "çarpar", True))
%>
```

```
<!--#include file="JSON_latest.asp"-->
<%
Dim o
Set o = jsObject()
o("name") = "tuğrul"
o("surname") = "topuz"

Response.Write toJSON(o)
%>
```