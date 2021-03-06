# Developing
# in a black
# hole

[http://github.com/javiacei/developing-in-a-black-hole](http://github.com/javiacei/developing_in_a_black_hole)
[http://github.com/javiacei/dotfiles](http://github.com/javiacei/dotfiles)


# Vim

Vim, Vi IMproved, is a power open-source text editor

- Awesome documentation (:help)
- Huge community
- Extensible, customizable and portable


# Modes

- Normal `esc`
- Visual `v`
- Insert `i`
- Command-line `:!`


# Navigation

- Movement keys: `h`, `j`, `k`, `l`
- Forward, back: `w`, `b`
- Move multiplier `<number><movement>`
- Go to the beginning of current line `0` and to the end `$`
- Go to the beginning of the file `gg` and to the end `G`
- Go to line `:<linea>`

```python
# Example
from django.db import models

class Vehicle(models.Model):
  mma = models.DecimalField(max_digits=10, decimal_places=2, null=True)
  length = models.DecimalField(max_digits=10, decimal_places=2, null=True)
  model = models.CharField(max_length=200, null=True, blank=True)
```


# Actions

- Insert at the end of the current line `A`
- Add a new line below `o` and above `O`
- Change text `c + <movement>`
- Copy `y + <movement>` and paste `p`
- Delete `d + <movement>`
- Undo `u` and redo `c-r`
- Autocomplete `c-n`
- Repeat the last executed command `.`

```python
# Example
from django.db import models

class Vehicle(models.Model):
  mma = models.DecimalField(max_digits=10, decimal_places=2, null=True)
  length = models.DecimalField(max_digits=10, decimal_places=2, null=True)
  model = models.CharField(max_length=200, null=True, blank=True)
```


# Search

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


# Selection

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


# Macros

- Create a new macro `q + <macro register>`
- Apply macro `@ + <macro>`

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


# Functions

- Execute vim functions with `:`
- `:write`, :w, `:quit` ,`:q`, `:edit`, `:e`
- Execute command line `:!`


# Panels, Tabs

- Horizontal `:split` `:sp` and vertical `:vsplit` `:vsp` panels
- Tabs `:tabe`. Navigate with `gt` and `Gt`


# Plugins
- vundle
- nerdtree
- ctrlp
- ack
- vim-tmux-navigator
- vim-snippets
- vim-flake8
- vim-numbertoggle


# Tips

- Learn to speak Vim (see resources)
- Create your own configuration
- Search and try plugins, but ...
- Install those you are going to use
- Keep calm and be patient


# Resources

- [Learning the vi and Vim Editors](http://shop.oreilly.com/product/9780596529833.do)
- [Practical Vim](https://pragprog.com/book/dnvim2/practical-vim-second-edition)
- [spf13-vim](https://github.com/spf13/spf13-vim)


# Tmux

tmux is a client-server terminal multiplexer that lets you switch
between several programs in one terminal.


# Windows

- Create windows `<leader> + c`
- Rename windows `<leader> + ,`
- Navigate between windows `<leader> + w`, `<leader> + number`


# Panels

- Create horizontal `<leader> + -` and vertical `<leader> + |` panels
- Resize panel `<leader> + L` and `<leader> + H`
- Remove panel `<leader> + x`
- Zoom panel `<leader> + z`
- Navigation `<leader> + q` and like vim using `vim-tmux-navigator`


# Navigation

- Enter in navigation mode `<leader> + [`
- Same vim commands to navigate
- Search `/` and navigate between searches `n` y `N`


# Sync

- Panels syncronization `<leader> + :` and set property `:setw synchronize-panes`


# Pair Prog

- Create a named session in detached mode `tmux new-session -s pair -d`
- Connect to a named session `tmux attach-session -t pair`


# Tips

- Change tmux leader to `c-a` mapping `caps lock` key to `control`
- Configure your own tmux in `~/.tmux.conf`
- Use and configure [vim-tmux-navigator](https://github.com/christoomey/vim-tmux-navigator)


# Resources

- [tmux: Productive Mouse-Free Development](https://pragprog.com/book/bhtmux/tmux)


# HTTPie

Command line HTTP client to make interaction with web services 
as human-friendly as possible

- Command `http` to make requests
- JSON highlighting
- Provide query params `==`
- JSON by default `=`, `:=`, `@=`
- Set headers `Header:Value`
- Sessions


# Using curl

Using curl ...

curl -X POST <url>
    -H "Accept: application/json" \
    -H "Content-type: application/json" \
    -d '{"grant_type":"password","client_id":"<client_id>","username":"<username>","password":"<password>"}' \

curl <url>
    -H "Accept: application/json" \
    -H "Content-type: application/json" \
    -H "Authorization: Bearer <token>" \


# Using httpie

http POST <url> grant_type=password client_id=<client_id> username=<username> password=<password>
http <url> "authorization: Bearer <token>" (and with --session=<name> to save the session)


# jq

jq is a command line JSON processor

- Simple syntax
- JSON highlighting
- Lots of pipe filters


# Demo

jq '(.results | limit(3;.[]) | [.origin, .destination] | join(" -> "))'


# Thanks!

Francisco Javier Aceituno
fco.javier.aceituno@gmail.com
[http://github.com/javiacei](http://github.com/javiacei)

Software Engineer in OnTruck

We will move 1.000.000 trucks with python, join us!
jobs@ontruck.com
