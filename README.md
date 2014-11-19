tmux-broadcast
==============

Broadcast commands from one pane in tmux

A simple scripted alternative to `tmux synchronize-pane` which is limited in its usage.

Usage
-----
Call the script with the pane indices observed using PREFIX+Q inside tmux.

e.g. (in pane 0) tmux-broadcast 1 2

Will allow you to broadcast keys from pane 0 to pane 1 and 2.

If you move panes, they will stay linked.
If you close panes, an error from tmux will notify you of a dead pane.

Rough edges but usable. Used to investigate a patch for tmux itself.
