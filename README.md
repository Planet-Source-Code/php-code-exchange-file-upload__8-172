<div align="center">

## File Upload \!\!\!\!\!\!\!


</div>

### Description

Hope this will help! Good luck!
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[PHP Code Exchange](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/php-code-exchange.md)
**Level**          |Intermediate
**User Rating**    |4.6 (60 globes from 13 users)
**Compatibility**  |PHP 3\.0, PHP 4\.0
**Category**       |[Files](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/files__8-2.md)
**World**          |[PHP](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/php.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/php-code-exchange-file-upload__8-172/archive/master.zip)





### Source Code

```
upload.htm :
<html><head><title>PHP's FileUPLOAD</title></head><body>
<form method="post" action="upload.php" enctype="multipart/form-data">
     <input name="userfile[]" type="file">
     <input name="userfile[]" type="file">
     <input name="userfile[]" type="file">
     <input name="userfile[]" type="file">
     <input name="userfile[]" type="file">
     <input name="userfile[]" type="file">
     <input type="submit" value="Upload!!!" >
</form>
upload.php :
<?
  for($i=0;$i<sizeof($userfile);$i++)
  {
   if(!$userfile_size[$i])
     continue;
   $UPLOAD = fopen( $userfile[$i], "r" );
   $contents = fread( $UPLOAD,$userfile_size[$i]);
   fclose( $UPLOAD );
   $SAVEFILE = fopen( "upload//".$userfile_name[$i], "wb" );
   fwrite( $SAVEFILE, $contents,$userfile_size[$i] );
   fclose( $SAVEFILE );
 }
 echo "Server HaD Receive the Upload Files!";
?>
```

