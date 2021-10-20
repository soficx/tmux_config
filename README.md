### Tmux Configuration 
    
    One of the coolest thing about tmux is completely configurable so you can customize the way you interact
    with and the way it looks

----
 When tmux is started, it loads the system configuration file from /etc/tmux.conf Then looks for a user configuration file at ~/.tmux.conf  

    ⚠️ if you've just installed tmux, you 'll need to create the file from scratch  

#### General Settings : 

- Change the prefix C-a instead of C-b
- Change the indexing of windows and pane starting from 1 
- Add scroll history in the buffer
- Enable mouse support
- Ensure window index numbers get reordered on delete 
- Change Copy mode Entry to tab 
- Using vi keys in buffer 
-----
```
Change prefix from 'C-b' to 'C-a'
unbind C-b                  
set-option -g prefix C-a    
bind-key C-a send-prefix
```
Change the indexing of windows and pane starting from 1 rather than 0
```
set -g base-index 1
setw -g pane-base-index 1
```
Add a bit more scroll history in the buffer.
```
set -g history-limit 50000
```
Enable full mouse support 
```
set -g mouse on
```
Ensure window index numbers get reordered on delete.
```
set-option -g renumber-windows on
```
Change the copy mode key
```
unbind [ 
bind-key tab copy-mode
```

Using vi keys in buffer
```
set -g mode-keys vi 
```
