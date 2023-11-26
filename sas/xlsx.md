### Using LIBNAME XLSX to read and write Excel files. 
- Syntax
```
/* because Excel field names often have spaces */
options validvarname=any;
 
libname xl XLSX '/folders/myfolders/sas_tech_talks_15.xlsx';
 
/* discover member (DATA) names */
proc datasets lib=xl; quit;
 
libname xl CLEAR;
```
Source: 
https://blogs.sas.com/content/sasdummy/2015/05/20/using-libname-xlsx-to-read-and-write-excel-files/