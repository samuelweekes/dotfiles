# Dotfiles and Config

## Manual steps

Set up OSX hotkeys:
1. Open System Preferences -> Keyboard -> Shortcuts
2. Navigate to 'Mission Control' options
3. Set Ctrl+§ to swap to previous desktop
4. Set Ctrl+tab to swap to next desktop

Install Tmux plugins:
1. Open up a tmux session
2. Install plugins with `prefix + I`

Add Timewarrior hook to Taskwarrior:
1. find / -name on-modify.timewarrior 2>/dev/null
2. cp /path/to/on-modify.timewarrior ~/.task/hooks/
3. chmod +x ~/.task/hooks/on-modify.timewarrior
4. task diagnostics - check active

