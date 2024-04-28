---
create: 2024-04-28
---
### outside tmux
- tmux new -s <session-name> - create new session with specific name
- tmux a - attach to the session
- tmux ls - sessions list
### inside tmux
#### pane
- <prefix> hjkl - resize panes
- <prefix> m - maximise/minimize pane
- <prefix> | - split vertically
- <prefix> - - split horizontally
- <C-h> <C-j> <C-k> <C-l> - switch between panes
#### configuration
- <prefix> r - refresh tmux configuration
- <prefix> I - install tmux plugins
- <prefix> : - command line
#### session
- <prefix> s - session list
#### window (set of panes)
- <prefix> w - list of windows
- <prefix> c - create new window
- <prefix> <window_name> - switch to window by window name
- <prefix> , - rename window
- <prefix> n - next window
- <prefix> p - previous window
#### copy mode
<prefix> [ - enter the *copy mode*
<C-c> - exit the *copy mode*