Integration with macos / finder.

https://schembri.me/post/neovim-everywhere-on-macos/

1. Using automator app, create an application with "Run applescript" action and put the following in the script. Save the application in `/Applications`

```
on run {input, parameters}
	set cmd to "nvim"
	if input is not {} then
		set filePath to POSIX path of input
		set cmd to "nvim \"" & filePath & "\""
	end if
	
	tell application "iTerm"
		create window with default profile
		tell the current window
			tell the current session to write text cmd
		end tell
	end tell
end run
```

2. Also using automator, create a "Quick Action" with the following content. 

```
on run {input, parameters}
	set tempfile to do shell script "mktemp -t edit-in-vim"
	
	tell application "iTerm"
		create window with default profile
		tell the current window
			tell the current session
				write text "cat <<EOF > \"" & tempfile & "\""
				write text input
				write text "EOF"
				
				write text "nvim \"" & tempfile & "\""
				
				delay 1
				repeat while name contains "nvim"
					delay 0.1
				end repeat
				
				set content to do shell script "cat \"" & tempfile & "\""
				close
				return content
			end tell
		end tell
	end tell
end run
```

In system preferences -> keyboard shortcuts -> services, assign it a shortcut cmd+option+ctl+v
