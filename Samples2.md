# Definitions #
## object object ##
```
<!--#include file="JSON_latest.asp"-->
<%
Dim o
Set o = jsObject()

o("name") = "tuğ"
o("name") = o("name") & "rul"

o("surname") = "topuz"
o("lucky_numbers") = Array(1,2,6,7,9)
o("sample_date") = #05.10.2003#
o(Null) = "nasrettin hoca"

o.Flush
%>
```
## array object ##
```
<!--#include file="JSON_latest.asp"-->
<%
Dim a
Set a = jsArray()

a(Null) = 2
a(Null) = 4
a(Null) = 6
a(Null) = 8

a.Flush
%>
```
# Conversions #
## jsArray to jsObject ##
```
<!--#include file="JSON_latest.asp"-->
<%
Dim a
Set a = jsArray()

a(Null) = 2
a(Null) = 4
a(Null) = 6
a(Null) = 8

a.Flush

a.Kind = JSON_OBJECT

a.Flush
%>
```
## jsObject to jsArray ##
```
<!--#include file="JSON_latest.asp"-->
<%
Dim o
Set o = jsObject()

o("name") = "tuğ"
o("name") = o("name") & "rul"

o("surname") = "topuz"
o("lucky_numbers") = Array(1,2,6,7,9)
o("sample_date") = #05.10.2003#
o(Null) = "nasrettin hoca"

o.Flush

o.Kind = JSON_ARRAY

o.Flush
%>
```
# Block Structures #
## object sample ##
```
<!--#include file="JSON_latest.asp"-->
<%
Dim o
Set o = jsObject()

Set o("person") = jsObject()
o("person")("name") = "Tuğrul"
o("person")("surname") = "Topuz"

Set o("equipment") = jsObject()
o("equipment")("name") = "keyboard"
o("equipment")("type") = "electronic"
o("equipment")("buy_date") = #06.04.2003#

o.Flush
%>
```
## array sample ##
```
<!--#include file="JSON_latest.asp"-->
<%

Dim a
Set a = jsArray()

Set a(Null) = jsArray()
a(Null)(Null) = 0
a(Null)(Null) = 2
a(Null)(Null) = 4
a(Null)(Null) = 6

Set a(Null) = jsArray()
a(Null)(Null) = 1
a(Null)(Null) = 3
a(Null)(Null) = 5
a(Null)(Null) = 7

a.Flush
%>
```
## mixed sample ##
```
<!--#include file="JSON_latest.asp"-->
<%

Dim a
Set a = jsArray()

Sub AddMember(name, surname, birth)
	Set a(Null) = jsObject()
	a(Null)("name") = name
	a(Null)("surname") = surname
	a(Null)("birth") = birth
End Sub

AddMember("tuğrul", "topuz", #10.09.1989#)
AddMember("cin", "ali", #01.01.1968#)

a.Flush
%>
```