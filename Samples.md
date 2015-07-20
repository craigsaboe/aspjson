# Self Primitive Datatypes #
### numbers ###
```
<!--#include file="JSON_latest.asp"-->
<%
Response.Write toJSON(1989)
%>
```
### strings ###
```
<!--#include file="JSON_latest.asp"-->
<%
Response.Write toJSON("やあ")
%>
```
### date & times ###
```
<!--#include file="JSON_latest.asp"-->
<%
Response.Write toJSON(Now())
%>
```
### single dimension arrays ###
```
<!--#include file="JSON_latest.asp"-->
<%
Response.Write toJSON(Array("a","l","i"))
%>
```
### multi dimension arrays ###
```
<!--#include file="JSON_latest.asp"-->
<%
Dim x(1,1,1)
x(0,0,0) = "threedot"
x(0,0,1) = 2

Set x(0,1,0) = jsObject()
x(0,1,0)("nickname") = "threedot"
x(0,1,0)("age") = 19

x(0,1,1) = 6
x(1,0,0) = Array(Date(), 19, "threedot", True)
x(1,0,1) = False
x(1,1,0) = 10
x(1,1,1) = "やあ"

Response.Write toJSON(x)
%>
```