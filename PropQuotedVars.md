**syntax:**

```
object.QuotedVars ' [Boolean]
```

JSON string have quoted variables for JSON objects. Various EcmaScript compliant engine have difference specifications, for instance ActionScript fails process for quoted variables.

## Samples ##

```
<!--#include file="JSON_latest.asp"-->
<%
Dim car
Set car = jsObject()

car("model") = 1984
car("color") = "red"
car("name") = "anadol"

car.Flush

car.QuotedVars = False
car.Flush
%>
```