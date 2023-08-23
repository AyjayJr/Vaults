Misc vim commands I've needed

### Create file in current directory

:e is edit
% refers to current document
:h refers to current documents path - filename
:w to save

```
:e %:h/filename
:w
```

Alternatively,

put in .vimrc to auto change to current directory

```
:set autochdir
```

then just,

```
:e filename
:w
```
