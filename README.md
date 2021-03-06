# About json_processing script

This is python script which can be used as console user interface program or python module to perform some usefull manipulation with JSON data.

# Features
Goal is to handle several usefull things for text JSON representaion which can be considered as hierarchical representaion of data:

[1] extract some variable from JSON object by path

[2] extract some variable from JSON object by path and evaluated arbitarily Python expression on this variable. To reference to variable use "value" in your expression

[3] delete some variable from JSON object by path

[4] set some variable to specific value if previously variable was contained within JSON object

[5] set some variable to specific value if previously variable was not contained within JSON object

# Input
There are 3 format of input data.

*Format-1:* By default mode input is reading from stdin as it's a textfile in format:

`<USER_DEFINED_KEY> <TAB> <JSON_REPRESENTATION> <LF>`

`<USER_DEFINED_KEY> <TAB> <JSON_REPRESENTATION> <LF>`

`...`
  

`<TAB>` -- is tab symbol

`<LF>` -- is line feeding, a.k.a new line.

So before use this script you should convert text representation of JSON object into representation which doesn't include line feeding.

*Format-2:* You can specify input filename by `-i` or `--input` parameter.  Format of input is the same as in Format-1.

*Format-3:* You can specify input filename by `-ink` or `--input_no_key` parameter. In this mode text there is no key information and content of all file represent single json object.

# Output

You can optionally specify output filename by `-o` or `--output` parameter. If you will not do it by default output will be dumped to standart output text stream.
Output contains `key` per json object if input was in format-1 or format-2. 
Output contains `file:input filname` if input was in format-3. 

`<USER_DEFINED_KEY> <TAB> <JSON_REPRESENTATION> <LF>`

`<USER_DEFINED_KEY> <TAB> <JSON_REPRESENTATION> <LF>`

`...`
  

`<TAB>` -- is tab symbol

`<LF>` -- is line feeding, a.k.a new line.

# Reference to Source code and repository

[1] Repository with script https://github.com/burlachenkok/json_processing

[2] Script itself: https://github.com/burlachenkok/json_processing/blob/master/json_processing.py
I tested this application with Python 2.7*. 


# Author
Konstantin Burlachenko (burlachenkok@gmail.com)

# Various links

[1] Example of usage https://github.com/burlachenkok/json_processing/blob/master/example/demo.sh

[2] Orirginal data, prepared data for example and demo.sh text output: https://github.com/burlachenkok/json_processing/blob/master/example



### Copyright (c) 2018, Konstantin Burlachenko (burlachenkok@gmail.com).  All rights reserved.
