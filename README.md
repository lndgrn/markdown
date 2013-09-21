    
IPFile
======
    
Hjälp-funktioner för att arbeta med filsystemet.
    
En *path* anges vanligtvis som "/myFunkeyFolder/myFunkeySubfolder/MyFunkeyFile.file".
    
    
###Create File FileInfoLists
    
    function IDFileInfoListCreateWithFilesAtPath( String aPath ):File.FileInfoList
       {
       
       var myFileInfoList = File.FileInfoList();
       
       File.list( myFileInfoList , File.ListParam.Files , aPath );
       
       return myFileInfoList;
       
       }
    
    
###Create File TextStreams
    
*ReadOnly* och *UTF-8*
    
    function IDTextStreamCreateWithPathAndReadOnlyModeAndUtf8Decoder( String aPath ):File.TextStream
       {
       
       return File.openText( aPath , File.Mode.ReadOnly , "UTF-8" );
       
       }
    
*TruncateOrCreate* och *UTF-8*
    
    function IDTextStreamCreateWithPathAndTruncateOrCreateModeAndUtf8Decoder( String aPath ):File.TextStream
       {
       
       return File.openText( aPath , File.Mode.TruncateOrCreate , "UTF-8" );
       
       }
