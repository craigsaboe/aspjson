aspjson is JSON serializer for VBScript based ASP server technology.

It uses VBScript's primitive types except Object and Array types. `jsObject` and `jsArray` classes stand JSON Object and Array dynamically on server side.
These classes derive core functionality from `jsCore`.

aspjson supports nested types for block of buildings, such as `jsObject` instances can contain `Number`s, `String`s, `Null`s, `Array`s and other primitive types, `jsArray` instances can contain these `jsObject` instances or all of the primitive types.

## Hello World! ##
### sample ###
```
<!--#include file="JSON_latest.asp"-->
<%
Dim member
Set member = jsObject()

member("name") = "Tuğrul"
member("surname") = "Topuz"
member("message") = "Hello World"

member.Flush
%>
```
### output ###
```
{"name":"Tu\u011Frul","surname":"Topuz","message":"Hello World"}
```

## SQL Queries ##
### sample ###
```
<!--#include file="JSON_latest.asp"-->
<!--#include file="JSON_UTIL_latest.asp"-->
<%
QueryToJSON(dbconn, "SELECT name, surname FROM members WHERE age < 30").Flush
%>
```
### output ###
```
[
    {
        "name":"ali",
        "surname":"osman"
    },
    {
        "name":"mahmut",
        "surname":"\u00E7\u0131nar"
    }
]
```

## Multi Dimensional Arrays ##
### sample ###
```
<!--#include file="JSON_latest.asp"-->
<%
Dim a(1,1)

a(0,0) = "zero - zero"
a(0,1) = "zero - one"
a(1,0) = "one - zero"
a(1,1) = "one - one"

Response.Write toJSON(a)
%>
```
### output ###
```
[["zero - zero","zero - one"],["one - zero","one - one"]]
```

You can reach [Wiki Pages](http://code.google.com/p/aspjson/w/list) for more information.