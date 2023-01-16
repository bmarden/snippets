# Useful VIM snippets

## `g commands`

```vim
" Remove all blank lines
:g/^$/d

" Remove all blank lines that have whitespace
:g/^\s*$/d
```

```vim
" Converting snake_case to TitleCase in vim

" Replace first character and characters after _ with uppercase
:s/\".\|_./\U&/g
" Remove _
:s/_//g
```
