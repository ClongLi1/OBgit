// Get all folders                                                                                              
<%  
Tp.App.Vault.GetAllLoadedFiles ()  
  .filter (x => x instanceof tp. Obsidian. TFolder)  
  .map (x => x.name)  
%>  

// Update frontmatter of existing file  
<%*  
Const file = tp. File. Find_tfile ("path/to/file");  
Await tp.App.FileManager.ProcessFrontMatter (file, (frontmatter) => {  
  Frontmatter["key"] = "value";  
});
%>  
