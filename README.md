<div align="center">

## Forced Download


</div>

### Description

Forces users to have choice of downloading a binary file. This was becomming a problem with Word documents - as they would either open within the browser or open externally. You may need to change the FileName variable.
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Lewis E\. Moten III](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/lewis-e-moten-iii.md)
**Level**          |Beginner
**User Rating**    |4.8 (58 globes from 12 users)
**Compatibility**  |ASP \(Active Server Pages\)
**Category**       |[Controls/ Forms/ Dialogs/ Menus](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/controls-forms-dialogs-menus__4-3.md)
**World**          |[ASP / VbScript](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/asp-vbscript.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/lewis-e-moten-iii-forced-download__4-7351/archive/master.zip)





### Source Code

```
<%
Dim Stream
Dim Contents
Dim FileName
FileName = "History12.doc"
Response.ContentType = "application/octet-stream"
Response.AddHeader "content-disposition", "attachment; filename=" & FileName
Set Stream = server.CreateObject("ADODB.Stream")
Stream.Open
Stream.LoadFromFile Server.MapPath(FileName)
Contents = Stream.ReadText
Response.BinaryWrite Contents
Stream.Close
Set Stream = Nothing
%>
```

