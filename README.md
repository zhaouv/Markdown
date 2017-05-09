# Markdown interpreter

## Forked Form [duangao](https://github.com/duangao/Markdown)
**changes:**
+ horizen line
+ link
+ support both [LF,CRLF,CR]
+ fix unnatural expression &lt;/li&gt;&lt;/ul&gt;&lt;ul&gt;&lt;li&gt; in unordered list
+ '\n\n' -> '\n\n&lt;br/&gt;&lt;br/&gt;'
+ '&nbsp;&nbsp;\n' -> '&nbsp;&nbsp;\n&lt;br/&gt;'
+ merge blockquote
+ fix bug in img ang table
+ add '&lt;p&gt;&lt;/p&gt;' for text
+ using [github-markdown-css](https://github.com/sindresorhus/github-markdown-css)
+ using [highlight.js](https://github.com/isagalaev/highlight.js)

 *only change for Windows*

------------------------

## Install

### For Linux
+ First you can download it.
+ cd path_to_markdown.py 
+ ln -s full_path_to_markdown.py  /usr/bin/Markdown 
> You may need root. 

+ You can run it by Markdown in any path. 

### For Windows
+ download the markdown_win.py file, which support unicode file IO in windows and handle with the end-of-line character(which is \"r\n" instead of "\n")

> make sure you have put python in path.

+ You can run it by "python path_to_/markdown_win.py  MD_FILE xxx".

## Usage
Markdown source_file [options]

 **options:**
+ -h, --help: 
	show you the help messages
+ -o, --output + [dest_html_file]:
	Set output in specific HTML file
	Default name is "default_output.html"
+ -p, --print + dest_pdf_file:  
	Set output in specific PDF file.

> Warning: If you use this option, you must use -o meanwhile.

+ -P, --Print +dest_pdf_file:
	Generate PDf file only.

## Feature 
+ Six ranks title 
```
    # ---------h1
    ##---------h2
    ###--------h3
    ####-------h4
    #####------h5
    ######-----h6

```
+ horizen line 
```
one of these
1.At least three '-' are needed.
2.'- - -'
3.At least three '*' are needed.
4.'* * *'
```
+ Unordered list
> +,*,- are okay.

+ Ordered list
> Begin with 'number. '

+ Line quote
```
You should put '>' at begin of line.
And this can be nested.
```
+ bold  Italic Delete 
> *italic*
> **bold**
> ~delete~
And you can nest them.

+ Superscript/Subscript
> Superscript: x^[1]
> Subscript:   x/[1]

+ Link and image
```
 [text](url)
 ![image](url)
```

+ Block and Code block
> Block must begin with '```' and end with '```'.
> Code block must begin with '```[language]' and end with '```'.
[Language]: python c++ 

Warning: Token handle with not be execute in block, like bold italic and so on. 

+ Table 

> First line is the table header.
> Second line must be one or more (---|),where '-' can be one or more.
> Extra lines are the body of table.

+ Math formula 
> Inner line formula : begin and end with '$'
> Line formula: begin and with '$$'

Tips: You should connect to Internet. 

## Dependency
+ wkhtmltopdf
	PDF export needs wkhtmlpdf,You can download it from \[wkhtmltopdf](wkhtmltopdf.org)
> For windows,it can work.But you should put the install directory that just like C:\user\xxx\wkhtmlpdf\bin in path.

+ mathjax
	You should connect to Internet to support mathjax working.
+ python3 
	You should use python3 instead of python2, if you must use it in python2,you can replace enum to your own class defination. And remove "from functools import reduce".


