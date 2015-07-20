**Syntax:**
```
object.Collection ' [Scripting.Dictionary]
```

`Collection` property returns reference to unwrapped property and value collection.

## Samples ##
### Iterate & Process Primitive Types ###
```
<!--#include file="JSON_latest.asp"-->
<%
Dim m, i
Set m = jsObject()
m("name") = "tuğrul"
m("surname") = "topuz"

For Each i In m.Collection
	Response.Write i & " : " & m(i) & vbCrLf
Next
%>
```
### Iterate & Process jsCore based object ###
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

For Each i In m.Collection
	m(i).Flush
Next
%>
```