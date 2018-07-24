# Title

Hi all. Thank you to be here.

My name is Javier Aceituno and I'm a Software Engineer at Ontruck

I'm sure that you are thinking... What is this talk about?

Ok, when I'm coding I use two principal tools.
In one hand I use an editor to read/write and modify the code and in the other hand I always need a terminal to execute django tasks like makemigrations, create a commit and push it to GitHub, run a new docker container and for example execute tests of my application.

I usually give talks about code in living sessions and, in/at? the end of the talk, I always receive the same question ...
What are the tools that you are using? and the answer is always the same... is vim... and tmux ... and people said ... really? Do you have colors in vim? Can you split windows inside the terminal? How do you do?

For that reason I have prepared this talk, to show you the tools that I use every day for coding and make me more
productive.

So let's start ...

How many of you use Vim? ... and ... of those, how many use tmux?

Ok ...

So this talk is about how you can integrate Vim with Tmux and an introduction of HTTPie.

You can follow the presentation in the first github repository and the second one is my Vim and Tmux configuration.


# Vim

Vim or Vi improved is a powerfull text editor from 1991 that works using the command-line interface.
It comes with an awesome documentation, really easy to use, a great community behind and it's really extensible, customizable and portable, Vim runs under Windows, Macintosh and almost all flavours of UNIX


# Modes

Vim uses 4 different modes and by default, when you open a file, you use the NORMAL mode …

This modes is used to navigate inside the file like search a string, move 5 lines below, go to the end of the file and so on...

Besides all this, you have the INSERT mode to introduce new text, VISUAL MODE to select text and COMMAND mode to execute functions like write and quit.


# Navigation

Like any editor in Vim you can navigate inside a file, but instead of using the mouse and arrows, you use the keys h, j, k, l in NORMAL mode.

You can also use the arrow keys but Vim has been built thinking on that special keys. At the beginning you don't feel confortable using that keys but in the end, you understand that is really powerful because you have your fingers in the middle of the keyboard when you are doing the most common task … reading code.

Also you can move forward and backward to move between words

> Example 8 times `w` or `8w`

To go to number ten you should move 8 words so you have to press `w` 8 times. In Vim the idea is to press the fewer keys as possible so instead of press 8 times forward, we can multiple the movement by 8 to do the same action.

> Example using `f`

But we can do it better using *find in the current line* so we can go directly to number 1.

This multiplier works with all movements so I can move 5 lines up or down, but are you saying that you have to count the lines? 

> Example open OnTruck project

Yes, in that case, but you can configure Vim to show you the number of lines that you have up or down from your current position.

Apart from that, you can do several movements like go to the begining and to the end of the current line, current file or move to an specific line.


# Actions

You can change to INSERT mode you only have to press `i` (insert) key to write.

> Example doing all actions in the list

The actions in Vim are always executed from NORMAL mode and some examples are insert at the end of the line, insert a new line below or above, change text, copy & paste, delete lines, undo and redo, autocomplete, etcetera.

But for me, the most important action is *repeat your last command* with key `.` (dot).

> Example `.` (dot)

So imagine that you want to import models as `m`. In that case you go up insert as `m` and go to the models words to change to `m`. To do that, you change the word models with `m`. And to repeat that acion you can go to the rest of models words and press on `.`.


# Search

Other thing that we use a lot developing is search text.

You can search a word in the current file.

> Example using `/`

Or you can search the word that you have inside your current position

> Example using `*`

And how can we search and replace?

> Example `*` + `.`

Imagine that we want to do the same action as before renaming models with m. We can do it with a regular expression, but I prefer to do it with the combination of *search the word in current position* plus *repeat your last command*.


# Selection

Now is the time to use a different mode, VISUAL model. Visual mode is used to select text and, once you have the text selected you can make different actions.

> Example delete INCIDENT_ACTIONS content

For example if we want to remove INCIDENT_ACTIONS tuple we can select that text and execute the action delete.

And Vim also comes with block selection. That means that we can make actions in multiple lines at the same time.

> Example block selection to add a prefix

To set a prefix to this constants we go to the beginning of the word, enter in block selection mode and say *insert* word `INCIDENT`. So when you finish pressing `ESC` the action is repeated in previous selection.


# Splits and Tabs

Like any other editor Vim you can have multiple files in your screen. 

> Example with split and vsplit

You can use panels or tabs dependends if you want to see the files at the same time or not.


# Functions

Ok ... we have navigated into files, modify some text but ... How can I save the changes?

Vim comes with lots of built-in functions like save the file, quit, edit a file, etcetera. To execute a function you have to do it from COMMAND mode that is pressing `:`.

> Example :write

For example if we want to save the changes that we have made we enter in COMMAND mode and execute the function *write* or *w* that is the same.

To know how functions work you can execute the function help and in that case *:help write*.


# Plugins

Here I have put the list of plugins that I'm using.

> Open OnTruck code and explain each of them.


# Tmux

Ok, now that we know a little about Vim, is the time to do the rest of action that we usually do in a normal day like:
- Commit changes to github
- Build and up the docker container of your applications
- Or create a simple Django migration

To do that we need a simple tool that is a terminal, but ... Can I use the same terminal that I'm using for Vim? YES. To do that there a lot of tools like iterm that let you create tabs and splits, but today I would like to talk you about Tmux.

tmux is a client-server terminal multiplexer that lets you switch
between several programs in one terminal.

> Example execute tmux

To execute it, you only have to run `tmux` in your terminal. Like Vim, Tmux use `.tmux.conf` file to configure Tmux. I invite you to see the tmux.conf file that I have in my dotfiles repository to see the configuration that I'm going to use here today.


# Windows

> Example create windows

I will start creating two windows, one for the slides and the other to open OnTruck project.
In the first window I'll open the slides using vimdeck and in the other vim.

> Example move between windows

We can move between windows directly using the number of the window or seeing the list of windows that I have.

> Example rename the tab

Once that we can our windows created I change the name of the windows to be more verbose and know where I am.


# Panels

Instead of use only windows, I like to use windows with different panels

> Example panels: vim + docker + shell + terminal

so in the window with the OnTruck project I usually have vim, one panel with the docker container, one panel with a python shell and one more with a simple terminal inside the project to commit changes or execute django commands.

This panels configuration lets you make all your common action in only one window. For example we can be coding and:

> Example move to shell

If you need to execute somethign in Python in the context of your app you only need to go to the shell panel

> Example ipdb + postman POST /driver + docker container

Or imagine that you are debugging with `ipdb`, you can use the docker container tab to do this

and always seeing the code you are working with.

Somethimes the size of your panels is not enough and you can resize it or some useful operation is to maximaze the panel where you are working.

> Example maximaze docker panel

For example if I want to have all the screen to debug I move to the docker container panel and maximaze.

> Example move panels number

You can move between panels using the panels number, but I prefer to move between them like vim.

> Example move vim-tmux

To do that you can install a Vim plugin calls `vim-tmux-navigator` and map the keys you use to the move between panels in tmux.conf file. This plugins integrate vim and tmux panels so you can move between vim and tmux panels using the same way.


# Navigation

You can navigate in a tmux panel exactly as in vim, but of course, not with all vim functionality.

> Example error in POST driver

Imagine that we are coding and testing our application and we have an exception. So the first thing to do is navigate to see the trace of your program and second open the file where the failure resides.


# Sync

One amazing functionality of tmux is the panels syncronization. You can execute the same in different panels at the same time.

> Example machine1 + machine2 edit file

For example this is really useful when you want check the status of a service in different machines or change the code of a file in diferrent machines at same time, but remember you shouldn't do this at production ;).


# Pair Prog

And my favourite tmux feature is the posibility to work with your coworker in pair programming. Before, to run tmux, I have executed tmux without arguments. When you do that, you are creating a tmux session and attach to it.

> Example tmux detached mode

Instead of that we can create a named session in detached mode and after that you can connect to it.

With tmux two (or more) different users can connect to the same session.

> Example attach + open vim + attach new session

Using this, we can create a named session in a development environment, connect via ssh, attach to the named session and the magic starts to happen.


# HTTPie

Before, when we were testing our application, we have used Postman to make the request. We have lots of clients like Postman but now that I have an awesome environment running in tmux should be great to use something to make request directly through the terminal. And yes we have an amazing tool call CURL.

Ok so lets try to connect our API using CURL.

First of all we have to create an access token, and after that we need to use it to get results from our API, in that case we want to retrieve the routes that we have openned in Spain.

> Example with the curl

Ok, we can do it but ... I have to write a lot and curl in not designed for humans ... so for that reason HTTPie was born.

HTTPie is a command line HTTP client to make interaction with web services as human-friendly as possible. It comes with lot of features like JSON highlighting and sessions and powerful defaults to use JSON APIs.

So lets go to transform that horrible CURLs to simple httpie requests...

> Example transforming request to create an access_token

First of all we have to change the command, now instead of curl, http is used. HTTPie has been built to use it with JSON APIs by default so we can remove Accept and ContentType headers. And instead to send the json in a string format we can send it as simple arguments

The first thing that we notice is that the response body comes with a highlighting and JSON format.

But we can do it better because in HTTPie schema and host by default are `http` and `localhost` so ...

> Example refactoring http request to create an access_token removing `http` and `localhost`

> Example http request to create an access_token with a file

And now we can take the access token and use it to retrieve the openned routes for Spain.

> Example transforming request to retrieve routes

Like before here we can remove http, localhost and all headers related with JSON, but what happens with our custom authorization header? Ok, we can send it like in curl.

> Example refactoring http request to retrieve routes with --session


# Tips

To finalize with I would like to give you some tips ...

For Vim:
- Learn to speak Vim (see resources)
- Create your own configuration
- Search and try plugins, but ...
- Install those you are going to use
- Keep calm and be patient

For Tmux:
- Change tmux leader to `c-a` mapping `caps lock` key to `control`
- Configure your own tmux in `~/.tmux.conf`
- Use and configure [vim-tmux-navigator](https://github.com/christoomey/vim-tmux-navigator)


# Resources

The first two books are awesome. The first one explain you the basis of Vim and the second one gives you more that one hundred tips.

In the other hand, spf13-vim is a github repository with lots of plugins and a really good approach to configure your vimrc file.

I only have read this book about tmux and it's a really good. It gives you all the knowledge that you need to use tmux and how you can configure step by step.


# Conclusion

And that's all.

(TODO)


# Thanks

Thank you all and remember ... OnTruck is hiring so if you are looking for a new job in sunny Madrid go to our stand to meet us.
