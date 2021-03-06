# How to use Tmux like hacker

After update .tmux.conf
Update config:
tmux source-file ~/.tmux.conf

<bind-key> Control + a 

v split-window -h
b split-window
o Switch to the next pane
q Number Switch to the pane

Our prefix/leader key is Control + a now (just like the screen multiplexer). This sequence must be typed before any tmux shortcut.

Control + a before any command
Control + a then ? to bring up list of keyboard shortcuts
Control + a then <Space> to change pane arrangement
Control + a then o to rotate panes
Control + a then h, j, k, l to move left, down, up, right. Respectively. (vim hjkl)
Control + a then ; to go to last panel

<!-- 
    Window
-->
Beyond your first window:

Control + a then c to create a new window
Control + a then n to next window
Control + a then p to previous window
Control + a then [0-9] move to window number
Control + a then & to kill window
Custom:

Control + a then m to switch to main-horizontal layout with the main window at 60% height.


<!-- ####################################################################### -->

read this https://danielmiessler.com/study/tmux/
see video demo https://www.youtube.com/watch?v=BHhA_ZKjyxo

Ctrl+a <command>

<command>
[phan window}

        Ctrl+a c                               New window
        Ctrl+a , {dau phay}                    Dat ten window
        Ctrl+a l                               go to last-active window 
        Ctrl+a p                               chuyen toi cua so trc
        Ctrl+a n                               chuyen toi cua so sau
        Ctrl+a w                               List window
        Ctrl+d                                 exit current shell/window   
        Ctrl-a &                               Kill the current window
        Ctrl-a window number                   (Move to the specified window number,the default bindings are from 0 -- 9)
        Ctrl-a .                               di chuyen window hien den so moi
        
        :movew<CR>                             move window to the next unused number
        :swap-window -s 3 -t 1                 Swap window 3 cho window 1

[panel]
        Ctrl+a %                               dua panel theo chieu ngang
        Ctrl+a : split-window                  Dua panel theo chieu doc
        Ctrl+a "                               Dua panel theo chieu doc    
        Ctrl-a q                               Show pane numbers (used to switch between panes)
        Ctrl-a o                               Switch to the next pane
        Ctrl-a ?                               List all keybindings
        Ctrl-a {                               (Move the current pane left)
        Ctrl-a }                               (Move the current pane right)
        
        Ctrl-a z                               Zoom in or zoom out panel

[new session]
        tmux new -s session-name               start a new session with Name
        Ctrl+a d                               detach from currently attached session 
        tmux ls                                List session
        tmux attach -t session-name            re-attach a detached session 
        tmux kill-session -t session-name       
        Ctrl+a :kill-session
        Ctrl+a :rename-session <name-session>  Rename session
        tmux kill-server                       To kill all sessions, from the local terminal, we run the following command. 


# add to ~/.tmux.conf
bind | split-window -h
bind - split-window -v

http://www.dayid.org/comp/tm.html
#################################




Split Ubuntu(Gnome) Terminal Screen And Work Like A Professional Using "Tmux" Or "Screen"
http://www.noobslab.com/2014/08/split-ubuntugnome-terminal-screen-and.html
#################################

You can use keybind + key combination to perform actions for Tmux, follow these keys:  
KeyBind + Combination Key   Action Description  
Ctrl+b  %                                   Split the current window vertically into two panes  
Ctrl+b  :split-window                       Horizontally split window or current pane  
Ctrl+b  o                                   Switch to the next pane  
Ctrl+b  c                                   Open new window  
Ctrl+b  l                                   Move to previous window  
Ctrl+b  n                                   Move to next window  
Ctrl+b  p                                   Move to previous window  
Ctrl+b  d                                   Detach current client  
Ctrl+b  x                                   Kill the current pane  
Ctrl+b  &                                   Kill the current window  
Ctrl+b  ,                                   Rename the current window  
Ctrl+b  q                                   Display pane numbers  
Ctrl+b  ?                                   List all keybindings  
Ctrl+b  {                                   Move the current pane to previous  
Ctrl+b  }                                   Move the current pane to next  
Ctrl+b  :break-pane                         Detach pane into its own window  
Ctrl+b  w                                   List all windows  
Ctrl+b  0-9                                 To select window  


Tmux also allows you to resize panes as you like, follow these commands:  
KeyBind + Combination Key                   Action Description  
Ctrl+b  :resize-pane                        Resize current pane down by default  
Ctrl+b  :resize-pane -U                     Upward Resize current pane  
Ctrl+b  :resize-pane -R                     Resize current pane to right  
Ctrl+b  :resize-pane -L                     Resize current pane to left  
Ctrl+b  :resize-pane 40                     Resize current pane down by 40 cells  
Ctrl+b  :resize-pane -L 40                  Resize current pane left by 40 cells  
Ctrl+b  :resize-pane -R 40                  Resize current pane right by 40 cells  
Ctrl+b  :resize-pane -U 40                  Resize current pane upward by 40 cells  
Ctrl+b  :resize-pane -t -L 40               Resize pane with id of 2 left by 40 cells  
Ctrl+b  :resize-pane -t 2 40                Resize pane with id of 2 down by 40 cells  



Screen Terminal Multiplexer
Screen is a full-screen window manager that multiplexes a physical terminal between several processes, typically interactive shells. Each virtual terminal provides the functions of the DEC VT100 terminal and, in addition, several control functions from the ANSI X3.64 (ISO 6429) and ISO 2022 standards (e.g., insert/delete line and support for multiple character sets). There is a scrollback history buffer for each virtual terminal and a copy-and-paste mechanism that allows the user to move text regions between windows. When screen is called, it creates a single window with a shell in it (or the specified command) and then gets out of your way so that you can use the program as you normally would. Then, at any time, you can create new (full-screen) windows with other programs in them (including more shells), kill the current window, view a list of the active windows, turn output logging on and off, copy text between windows, view the scrollback history, switch between windows, etc. All windows run their programs completely independent of each other. Programs continue to run when their window is currently not visible and even when the whole screen session is detached from the users terminal.
GNU Screen can be thought of as a text version of graphical window managers, or as a way of putting virtual terminals into any login session. It is a wrapper that allows multiple text programs to run at the same time, and provides features that allow the user to use the programs within a single interface productively. This enables the following features: persistence, multiple windows, and session sharing. Checkout screen manual.



You can control screen multiplexer with following keys:  
KeyBind + Combination Key       Action Description  
Ctrl+a  | (Vertical Bar)        Split pane vertically  
Ctrl+a  Shift+s                 Split pane horizontally  
Ctrl+a  Shift+q                 Detach current pane  
Ctrl+a  Tab                     To switch between panes  
Ctrl+a  c                       To open pane session or New window  
Ctrl+a  space                   Move to next terminal  
Ctrl+a  backspace               Move to previous terminal  
Ctrl+a  "                       To choose between terminal windows  
Ctrl+a  0-9                     To navigate between terminal windows  
Ctrl+a  :remove                 Remove current pane  
Ctrl+a  Shift+x                 Remove current pane  
Ctrl+a  :only                   Remove all panes except one  
Ctrl+a  \                       To close all panes and exit screen   
Ctrl+a  :resize 40              Resize pane by 40 cells  
Ctrl+a  p                       Move to next process pane  
Ctrl+a  n                       Move to previous process pane

#########################################################################

Tmux Plugin Manager  
more info https://github.com/tmux-plugins/tpm


Installing plugins
Press prefix + I (capital i, as in Install) to fetch the plugin.


Uninstalling plugins
Remove (or comment out) plugin from the list.
Press prefix + alt + u (lowercase u as in uninstall) to remove the plugin.
All the plugins are installed to ~/.config/tmux/plugins/ so alternatively you can find plugin directory there and remove it.


Key bindings

prefix + I
Installs new plugins from GitHub or any other git repository
Refreshes TMUX environment


prefix + U
updates plugin(s)


prefix + alt + u
remove/uninstall plugins not on the plugin list


#########################################################################

# Save and Restore Tmux Environment

To save the Tmux environment, we hit Ctrl + a + Ctrl + s in the Tmux Terminal. If the save was successful, a message of Tmux environment saved! would pop up.


To restore the Tmux environment, we hit Ctrl + a + Ctrl + r in the Tmux Terminal. If the restore was successful, a message of Tmux restore complete! would pop up.


All the sessions, windows, and panels would be saved and restored with Tmux Resurrect. Some of the running commands, such as htop, would be restored as well.
#########################################################################
