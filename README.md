tmux-broadcast
==============

Broadcast commands from one pane in tmux

A simple shell-script alternative to `tmux synchronize-pane` allowing broadcasting 
commands to selected panes.

Poor man's manpage
------------------
```
NAME
    tmux-broadcast - send commands to selected panes in tmux

SYNOPSIS
    tmux-broadcast [OPTION]... [PANE]...

EXAMPLES
    tmux-broadcast -s 'file.sh' -v 1 2 3

        Save commands to 'file.sh'; Increase verbosity; Broadcast to panes 1, 2, 3.

DESCRIPTION
    Broadcast commands from one pane to any panes (in current window by default).

    Pane numbers known as PANE are the indices of a pane in a window obtained using
    `tmux display-panes`.

    Mandatory arguments to long options are mandatory for short options too.

    -s, --save=PATH
        write commands entered to the given path

AUTHOR
    Written by Julien Limoges.

COPYRIGHT
    The MIT License (MIT)
    Copyright (c) 2014 Julien Limoges. 
    
    Permission is hereby granted, free of charge, to any person obtaining a copy
    of this software and associated documentation files (the "Software"), to deal
    in the Software without restriction, including without limitation the rights
    to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
    copies of the Software, and to permit persons to whom the Software is
    furnished to do so, subject to the following conditions:
    
    The above copyright notice and this permission notice shall be included in all
    copies or substantial portions of the Software.
    
    THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
    IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
    FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
    AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
    LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
    OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
    SOFTWARE.
```

NOTES
-----
If you move panes, they will stay linked.
If you close panes, an error from tmux will notify you of a dead pane.

