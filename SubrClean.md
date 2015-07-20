**syntax:**
```
object.Clean
```
Remove all contents in jsObject or jsArray.

## Samples ##
```
<!--#include file="JSON_latest.asp"-->
<%
Dim o
Set o = jsArray()

Sub AddUser(name, surname)
        Set o(Null) = jsObject()
        o(Null)("name") = name
        o(Null)("surname") = surname
End Sub

AddUser "tuğrul", "topuz"
AddUser "nasrettin", "hoca"
AddUser "cin", "ali"
o.Flush

o.Clean

AddUser "barış", "manço"
o.Flush
%>
```