# Dotfiles and Config

## Manual steps

Set up OSX hotkeys:
1. Open System Preferences -> Keyboard -> Shortcuts
2. Navigate to 'Mission Control' options
3. Set Ctrl+§ to swap to previous desktop
4. Set Ctrl+tab to swap to next desktop
5. Remove Ctrl+arrow keys (used for TMUX resize)

Install Tmux plugins:
1. Open up a tmux session
2. Install plugins with `prefix + I`

Add Timewarrior hook to Taskwarrior:
1. find / -name on-modify.timewarrior 2>/dev/null
2. cp /path/to/on-modify.timewarrior ~/.task/hooks/
3. chmod +x ~/.task/hooks/on-modify.timewarrior
4. task diagnostics - check active

Setup bat themes:
1. Run `bat cache --build` to build the theme cache

Setup PHP Debugger:
1. Install Xdebug with pecl
2. Call php --ini to get the loaded config file
3. Add the below snippet:

```
  xdebug.mode = debug
  xdebug.start_with_request = yes
  xdebug.client_host = 127.0.0.1
  xdebug.client_port = 9003
  ; Useful for debugging issues
  ; Squelch annoying log messages on every php command if debugger isn't running, uncomment me if having issues...
  ; xdebug.log_level = 5
  ; xdebug.log = ""
  ```
4. Add a .vscode/launch.json in any project you want to debug. This will get picked up by the default nvim-dap config provided by LazyVim.
```

```
