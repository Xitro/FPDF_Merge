# FPDF_Merge
Tool to merge PDFs created by fpdf 1.6
Project for composer used based on FPDF_Merge by DEMONTE Jean-Baptiste <jbdemonte@gmail.com>

version 1.0

date 2011-02-18


## Why this tool ?
 
All the library tested (fpdi, ...) produce too heavy pdf
because, these are not optimized.
This library parses the pages, get the objects included (font, images)
generate a hash to store only once these objects or reuse previous stored ones.
 
   
## Notes
 
- links are not supported in this version
- all pages are included (because this was what we needed) but update it 
 to create an add(array pages) should be easy 
 

I tried to optimize a lot this tool using X-Debug, let me know if you do best :)
If you get trouble or want to comment, feel free to send me an email.

## Use
 
~~~~
$merge = new FPDF_Merge();
$merge->add('/tmp/pdf-1.pdf');
$merge->add('/tmp/pdf-2.pdf');
$merge->output('/tmp/pdf-merge.pdf'); // or $merge->output(); to open it directly in the browser
~~~~