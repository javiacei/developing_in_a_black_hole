# Developing
# in a black
# hole


# About me

Francisco Javier Aceituno
fco.javier.aceituno@gmail.com
[Github: @javiacei](http://github.com/javiacei)

Software Engineer en OnTruck


# Contents

- Vim
- Tmux
- HTTPie
- jq


# Vim

Vim, Vi IMproved, is a power open-source text editor

- Awesome documentation (:help)
- Huge community
- Extensible, customizable and portable


# Vim

- Modes
- Navigation
- Actions
- Search
- Selection
- Macros
- Command line
- Functions
- Splits and tabs
- Buffers
- Plugins
- Tips
- Resources


# Vim / Modes

- Normal `esc`
- Visual `v`
- Insert `i`
- Command-line `:`


# Vim / Navigation

- Movement keys: `h`, `j`, `k`, `l`
- Forward, back: `w`, `b`
- Move multiplier `<numero><desplazamiento>`
- Go to the begining of current line `0` and to the end `$`
- Go to the begining of the file `gg` and to the end `G`
- Go to line `:<linea>`


# Vim / Navigation

- Movement keys: `h`, `j`, `k`, `l`
- Forward, back: `w`, `b`
- Move multiplier `<numero><desplazamiento>`
- Go to the begining of current line `0` and to the end `$`
- Go to the begining of the file `gg` and to the end `G`
- Go to line `:<linea>`

```python
# Example
from django.db import models

class Vehicle(models.Model):
  mma = models.DecimalField(max_digits=10, decimal_places=2, null=True)
  length = models.DecimalField(max_digits=10, decimal_places=2, null=True)
  model = models.CharField(max_length=200, null=True, blank=True)
```


# Vim / Actions

- Insert at the end of the current line `A`
- Add a new line below `o` and above `O`
- Change text `c + <desplazamiento>`
- Copy `y + <desplazamiento>`
- Delete `d + <desplazamiento>`
- Paste `p`
- Undo `u` and redo `c-r`
- Repeat the last executed command `.`
- Autocomplete `c-n`


# Vim / Actions

- Insert at the end of the current line `A`
- Add a new line below `o` and above `O`
- Change text `c + <desplazamiento>`
- Copy `y + <desplazamiento>`
- Delete `d + <desplazamiento>`
- Paste `p`
- Undo `u` and redo `c-r`
- Repeat the last executed command `.`
- Autocomplete `c-n`

```python
# Example
from django.db import models

class Vehicle(models.Model):
  mma = models.DecimalField(max_digits=10, decimal_places=2, null=True)
  length = models.DecimalField(max_digits=10, decimal_places=2, null=True)
  model = models.CharField(max_length=200, null=True, blank=True)
```


# Vim / Search

- Search inside current line `f<character>` (forward), `F<character>` (back)
- Search inside current file `/`
- Search selected word `*`
- Search and replace `:%s/<search>/<replace>`


# Vim / Search

- Search inside current line `f<character>` (forward), `F<character>` (back)
- Search inside current file `/`
- Search selected word `*`
- Search and replace `:%s/<search>/<replace>`

```python
# Example
from django.db import models

class Vehicle(models.Model):
  mma = models.DecimalField(max_digits=10, decimal_places=2, null=True)
  length = models.DecimalField(max_digits=10, decimal_places=2, null=True)
  model = models.CharField(max_length=200, null=True, blank=True)
```


# Vim / Selection

- In visual mode `v`
- Block selection `c-v`


# Vim / Selection

- In visual mode `v`
- Block selection `c-v`

```python
# Example
from django.db import models

class Incident(models.Model):
    INCIDENT_ACTIONS = (
        (ASSIGN_DRIVER, 'Assign driver'),
        (UNASSIGN_DRIVER, 'Unassign driver'),
        (UPLOAD_CARGO_MANIFEST, 'Upload cargo manifest'),
        (DELETE_CARGO_MANIFEST, 'Delete cargo manifest'),
    )

    action = models.CharField(max_length=30, choices=INCIDENT_ACTIONS, default=ACTION_OTHER)
```


# Vim / Macros

- Create a new macro `q + <macro register>`;
- Apply macro `<number>@ + <macro>`;


# Vim / Macros

- Create a new macro `q + <macro register>`;
- Apply macro `<number>@ + <macro>`;

```python
# Example
from django.db import models

class Incident(models.Model):
    INCIDENT_ACTIONS = (
        (ASSIGN_DRIVER, 'Assign driver'),
        (UNASSIGN_DRIVER, 'Unassign driver'),
        (UPLOAD_CARGO_MANIFEST, 'Upload cargo manifest'),
        (DELETE_CARGO_MANIFEST, 'Delete cargo manifest'),
    )

    action = models.CharField(max_length=30, choices=INCIDENT_ACTIONS, default=ACTION_OTHER)
```


# Vim / Command line

- Execute vim functions `:`
- Execute command line `:!`


# Vim / Functions

- Execute vim functions with `:`
- `:write`, :w, `:quit` ,`:q`, `:edit`, `:w`


# Vim / Splits and tabs

- Horizontal `:split` `:sp` and vertical `:vsplit` `:vsp` splits
- Tabs `:tabe`. Navigate with `gt` and `Gt`


# Vim / Buffers

- A file loaded into memory for editing
- List buffers `:buffers`
- Select a buffer `:buffer <number>`, `:b <number>`


# Vim / Plugins
- vundle
- nerdtree
- ctrlp
- fugitive
- tabular
- ack
- vim-tmux-navigator
- vim-snippets
- vim-flake8
- vim-molokai


# Vim / Tips

- Learn to speak Vim
- Create your own configuration
- Search and try plugins, but ...
- Install those you are going to use
- Keep calm and be patient


# Vim / Resources

- [Learning the vi and Vim Editors](http://shop.oreilly.com/product/9780596529833.do)
- [Practical Vim](https://pragprog.com/book/dnvim2/practical-vim-second-edition)


# Tmux

tmux is a terminal multiplexer that lets you switch between several
programs in one terminal.


# Tmux

- Windows
- Splits
- Navigation
- Sync
- Pair Programming
- Tips


# Tmux / Windows

- Create windows `<leader> + c`
- Rename windows `<leader> + ,`
- Navigate between windows `<leader> + w`, `<leader> + number`


# Tmux / Splits

- Create horizontal `<leader> + -` and vertical `<leader> + |` splits
- Resize splits `<leader> + L` and `<leader> + H`
- Remove split `<leader> + x`
- Zoom split `<leader> + z`
- Navigation `<leader> + q` and like vim using `vim-tmux-navigator`


# Tmux / Navigation

- Enter in navigation mode `<leader> + [`
- Same vim commands to navigate
- Search `/` and navigate between searches `n` y `N`


# Tmux / Sync

- Splits syncronization `<leader> + ;` and set property `:setw synchronize-panes`


# Tmux / Pair Prog


# Tmux / Tips

- Change tmux leader to `c-a`
- Map `caps lock` key to `control`
- Use and configure [vim-tmux-navigator](https://github.com/christoomey/vim-tmux-navigator)
- Configure your own tmux in `~/.tmux.conf`


# HTTPie

Command line HTTP client to make interaction with web services 
as human-friendly as possible

- Command `http` to make requests
- JSON highlighting
- Provide query params `==`
- JSON by default `=`, `:=`, `@=`
- Set headers `Header:Value`
- Sessions


# jq

jq is a command line JSON processor

- Simple syntax
- Lots of filters
- Pipe filters
