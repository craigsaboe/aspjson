
```
<!--#include file="JSON_latest.asp"-->
<%
Function QueryToJSON(dbc, sql)
	Dim rs, jsa, col
	Set rs = dbc.Execute(sql)
	Set jsa = jsArray()
	While Not (rs.EOF Or rs.BOF)
		Set jsa(Null) = jsObject()
		For Each col In rs.Fields
			jsa(Null)(col.Name) = col.Value
		Next
	rs.MoveNext
	Wend
	Set QueryToJSON = jsa
End Function
%>

QueryToJSON(dbconn, "SELECT name, surname, date FROM members WHERE age < 30").Flush

```