+++
title = 'The Tmux Guide I Wish I Had'
date = 2024-07-12T23:32:15-07:00
draft = true
+++

GENERAL:
tmux: start session
exit: leave session

default prefix key: ctrl-b
copy mode: prefix + [
select area to copy: ctrl-v + space

PANES:
contain individual terminal sessions
only one active at a time
vsplit: ctrl-b + %
hsplit: ctrl-b + “
change window: ctrl-b + <up, down, left, right
move pane: ctrl-b + { or }
select pane by number: ctrl-b + q + [PANE_NUMBER]
zoom into pane: ctrl-b + z
make pane a window: ctr-b + !
close pane: ctrl-b + x

WINDOWS
Container of panes
has single active pane
shown at bottom of screen along with active window
new window: ctrl-b + c
switch to WINDOW_NUMBER: ctrl-b + [WINDOW_NUMBER]
rename window: ctrl-b + ,
cycle windows: ctrl-b + n or p
swap windows: ctr-b + :swap-window

SESSIONS
top most layer, collection of 1 or more windows
can have as many as you want open, but generally only attach to one
have a single active window
Able to resume sessions and processes even in th event of connection loss
detach session: ctrl-b + d
list sessions: tmux ls OR ctrl-b + s inside of session
preview windows: ctrl-b + w
attach to most recent session: tmux attach

rename session: tmux rename-session -t [CURRENT_SESSION_NAME] [NEW_SESSION_NAME]
create new session with name: tmux new -s [SESSION_NAME]
kill session: tmux kill-session -t [SESSION_NAME]


CONFIGURATION:
Config file in $HOME/.tmux.conf OR $XDG_CONFIG_HOME/tmux/tmux.conf (essentially ~/.config/tmux/tmux.conf)

source tmux config: ~/config/tmux/tmux.conf

PLUGINS:
tpm (CLONE REPO)

vim-tmux-navigator
tmux-sensible


https://www.youtube.com/watch?v=DzNmUNvnB04
https://www.youtube.com/watch?v=Yl7NFenTgIo
https://tmuxcheatsheet.com/

