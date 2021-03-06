# Vim quick ref  
  
### General
  
| Command | Description | 
|---|---|
| . | Repeat last change | 
| 5. | Repeat last change 5 times | 
| @ | Repeat last command line change |
| vim +324 fileName | When launching vim, open to line number 324 |
| vim +/searchTermHere fileName | When launching vim, search for searchTermHere |
| vim +<any : command> fileName | Run any : command when launching vim |

  
### Movement  
  
| Command | Description | 
|---|---|
| H | Jump cursor to top of screen | 
| M | Jump cursor to middle of screen | 
| L | Jump cursor to bottom of screen | 
| Ctrl-o | Jump to previous cursor location | 
| Ctrl-i | Jump back forwards to next cursor location|  
| Ctrl-e | Scroll screen up without moving cursor | 
| Ctrl-y | Scroll screen down without moving cursor | 
| % | Jump to matching bracket or parentheses | 
| t\<x> | Jump to next instance of character `x` |
| T\<x> | Jump to previous instance of character `x` |
  
### Code Editing  
  
| Command | Description | 
|---|---|
| visual > or < | indent block |
| \<leader\>cc | Comment out the current line or text selected in visual mode (NERDCommenter) |
| \<leader\>c\<space\> | Toggles the comment state of the selected line(s). Based on top line (NERDCommenter) |
| \<leader\>cy | Same as \<leader\>cc except that the commented line(s) are yanked first (NERDCommenter) |
| \<leader\>cu | Uncomments the selected line(s) (NERDCommenter) |
| \<leader>w | Remove all whitespace from file. Custom command: `noremap <leader>w :%s/\s\+$//g<CR>` |

Note: default \<leader\> for NERDCommenter is `\` 

### Text Manipulation 

| Command | Description | 
|---|---|
| g~ then a movement | Toggle case "HellO" to "hELLo" | 
| with gU then a movement | Uppercase "HellO" to "HELLO| 
| with gu then a movement | Lowercase "HellO" to "hello| 
| visual select, then ~ | Toggle case "HellO" to "hELLo" | 
| visual select, then U | Uppercase "HellO" to "HELLO | 
| visual select, then u | Lowercase "HellO" to "hello |

### Search  
  
| Command | Description | 
|---|---|
| :%s/foo/bar    | search and replace first match | 
| :%s/foo/bar/g  | global search and replace |
| :%s/foo/bar/gc | global search and replace, prompting for each replace |
| :%s/foo\c/bar/g | global search (case insensitive) and replace. Alternatively use `I` flag at end |
| :%s/foo/&ze/g   | ampersand matches search term - replaces with "fooze" |
| :.,$s/foo/bar/g | search and replace from current line to end of file (. optional) |
| :'<,'>s/foo/bar/g | search and replace in visual selection (including full lines at beginning and end) |
| :,+10s/foo/bar/g | search and replace in next 10 lines |


Note: instead of `/` any non-alphanumeric character other than `\`, `"`or `|` can be used as delimiter 
