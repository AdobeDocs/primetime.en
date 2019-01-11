---
description: null
seo-description: null
seo-title: License Embedder command-line usage
title: License Embedder command-line usage
uuid: 6f2cc195-ffdc-4421-a1ab-1d4e2412a8df
index: y
internal: n
snippet: y
---

# License Embedder command-line usage{#license-embedder-command-line-usage}

```
java -jar AdobeLicenseEmbedder.jar sourcefile destfile [options]
```

* `sourcefile` represents an encrypted file. 
* `destfile` specifies the name of the file in which the encrypted content with the embedded license is saved.

  If you specify a directory, the file is saved in the destination directory. The name of the source file also becomes the name of the file that is saved in the destination directory.

The following table describes the command line options that you can specify: 

## Options:

<table frame="all" colsep="1" rowsep="1" class="+ topic/table adobe-d/table " id="table_hnl_2sy_n4">  
 <thead class="- topic/thead "> 
  <tr rowsep="1" class="- topic/row "> 
   <th colname="1" class="- topic/entry entry"> <p class="- topic/p ">Command Line Option </p> </th> 
   <th colname="2" class="- topic/entry entry"> <p class="- topic/p ">Description </p> </th> 
  </tr> 
 </thead>
 <tbody class="- topic/tbody "> 
  <tr rowsep="1" class="- topic/row "> 
   <td colname="1" class="- topic/entry "> <span class="+ topic/ph pr-d/codeph codeph"> -l license-filename </span> </td> 
   <td colname="2" class="- topic/entry "> Name of the file that includes the license that you want to embed. You can specify multiple <span class="codeph"> -l </span> options to embed multiple licenses. </td> 
  </tr> 
  <tr rowsep="1" class="- topic/row "> 
   <td colname="1" class="- topic/entry "> <span class="+ topic/ph pr-d/codeph codeph"> -m metadata-filename </span> </td> 
   <td colname="2" class="- topic/entry "> Specifies the content metadata for which you can generate a license. This option is required to generate a license. </td> 
  </tr> 
  <tr rowsep="1" class="- topic/row "> 
   <td colname="1" class="- topic/entry "> <span class="codeph"> -noprompt </span> </td> 
   <td colname="2" class="- topic/entry "> Do not ask if the destination file should be overwritten. If the destination file already exists and the <span class="codeph"> -o </span> has not been applied, an error occurs. </td> 
  </tr> 
  <tr rowsep="0" class="- topic/row "> 
   <td colname="1" class="- topic/entry "> <span class="codeph"> -o </span> </td> 
   <td colname="2" class="- topic/entry "> If the destination file already exists, you can overwrite it without being prompted. </td> 
  </tr> 
 </tbody> 
</table>

