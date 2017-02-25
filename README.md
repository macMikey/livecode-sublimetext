livecode-sublimetext
==============
LiveCode Package for Sublime Text

# What does this package do?

The package adds syntax highlighting for LiveCode files. It is intended for editing script only stacks. The package includes a number of snippets that provide auto-completion when creating new handlers, if-then statements, try/catch blocks, etc.

Auto-complete is also provided for all keywords, properties, functions, and commands.

# Notifying LiveCode of script only stack updates

To send requests to a specified server and port whenever LiveCode files are saved, create a Sublime Text project for your folder tree.  Once you have done that, edit the  `.sublime-project` file.  Here is an example.
You will need to modify "MyProject" and possibly the port number that you are using.

```
{
	"folders":
	[
		{
			"folder_exclude_patterns":
			[
				"_builds"
			],
			"path": ".",
			"name": "MyProject",
		}
	],
	"livecode":
	{
  		"notify_on_save": true,
  		"notify_server":
  		{
    		"host": "localhost",
    		"port": 61373,
    		"debug": false
  		}
	}
}

```

# Screencasts

- [Configuring Sublime Text User Settings when Working with LiveCode](https://www.youtube.com/watch?v=RkhrHdah0zY)
- [Connecting a Sublime Text project to a Levure appllication running in the LiveCode IDE](https://www.youtube.com/watch?v=gkVo35Tb3ck)

# Plugin installation
Please use [Package Control][pc] to install the linter plugin. This will ensure that the plugin will be updated when new versions are available. If you want to install from source so you can modify the source code, you probably know what you are doing so we won’t cover that here.

To install via Package Control, do the following:

1. Within Sublime Text, bring up the [Command Palette][cmd] and type `install`. Among the commands you should see `Package Control: Install Package`. If that command is not highlighted, use the keyboard or mouse to select it. There will be a pause of a few seconds while Package Control fetches the list of available plugins.

2. When the plugin list appears, type `livecode`. Among the entries you should see `LiveCode`. If that entry is not highlighted, use the keyboard or mouse to select it.

[pc]: https://sublime.wbond.net/installation
[cmd]: http://docs.sublimetext.info/en/sublime-text-3/extensibility/command_palette.html
