# Add Copyright for Vim
fork from [https://github.com/nine2/vim-copyright], modified by newtorn.
vim-copyright is a plug for your file to add/update copyright.

## Installation

Copy the file on your .vim/plug folder.

### Vundle or Plug

```
Bundle "newtorn/vim-copyright"
Plug 'newtorn/vim-copyright'
```

## Usage

add the config to your .vimrc to set your name / email :

```
let g:file_copyright_name = "your name"
let g:file_copyright_email = "your email"
```

add the config to auto add copyright to your file:

Default:
```
let g:file_copyright_auto_filetypes = [
        \ 'sh', 'plx', 'pl', 'pm', 'py', 'python',
        \ 'h', 'hpp', 'c', 'cpp', 'java',
        \ 'ruby', 'rb', 'rake',
        \ 'uml', 'plantuml'
]
```
custom filetype:
```
let g:file_copyright_auto_filetypes = [
        \ 'py', 'python'
]
```

- use `:CopyrightAdd` to add copyright for your file.
- use `:CopyrightUpdate` to update copyright.

you can set comment_prefix map:

```
let g:file_copyright_comment_prefix_map  = {
    \"python": "\#", "py":"\#",
    \"cpp":"/*", "c":"/*", "h":"/*", "hpp":"/*",
    \"go":"/*",
    \"vim":"\"",
    \"sh":"\#", "shell":"\#",
\}

let g:file_copyright_comment_mid_prefix_map = {
    \"python": "\#", "py":"\#",
    \"cpp":"\#", "c":"\#", "h":"\#", "hpp":"\#",
    \"go":"\#",
    \"vim":"\"",
    \"sh":"\#", "shell":"\#",
\}

let g:file_copyright_comment_end_map = {
    \"cpp":"*/", "c":"*/", "h":"*/", "hpp":"*/",
    \"go":"*/",
\
```

or set for filetype(default):

```
    let g:file_copyright_comment_prefix = "\#"
    let g:file_copyright_comment_mid_prefix = "\#"
    let g:file_copyright_comment_end = ""
```


## Copyright

- python file:

```
# ====================================================
#   Copyright (C)2018 All rights reserved.
#
#   Author        : your name
#   Email         : your email
#   File Name     : eg.py
#   Last Modified : 2018-04-06 14:27
#   Description   : 
#
# ====================================================
```

- cpp file:

```
/* ====================================================
#   Copyright (C)2018 All rights reserved.
#
#   Author        : your name
#   Email         : your email
#   File Name     : eg.cpp
#   Last Modified : 2018-04-06 14:27
#   Description   : 
#
# ====================================================*/
```

