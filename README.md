# Custom Command Plugin for Wox 2

A simple and flexible Wox 2 plugin that allows you to define custom shell commands, scripts, or actions via a JSON file. Trigger commands with aliases or keywords directly from Wox!

## 🚀 Features

- Map custom shell commands to Wox keywords
- Support for CMD, PowerShell, and custom executables
- Lightweight and easy to configure
- Supports parameterized inputs

## 📦 Installation

1. Go to the Wox plugin directory:
    - macOS: `~/.wox/wox-user/plugins/`
    - Windows/Linux: 'Your Wox installation directory/plugins/'

2. Go to release page and download the latest version of the plugin

3. Extract the contents of the ZIP file into a new folder named `CustomCommand` in the Wox plugin directory.

4. Restart Wox.

## 🔧 Configuration
1. Open the `Custom Command Settings` in Wox
   (Plugins/Installed Plugins/Custom Command/Settings)
2. Edit the field (it's a JSON text field) 
3. Press Enter to save the changes (no need to restart Wox)
4. You'll see if it works directly in Wox, just type the shortcut name and if it appears, it works!

### Example Configuration
```json
[
  {
    "shortcut": "Gitlab",
    "script": "open 'https://gitlab.com/search?scope=merge_requests&search=$@'",
    "description": "Search merge requests in Gitlab $@"
  },
  {
    "shortcut": "Random",
    "script": "say $((RANDOM % $1))",
    "description": "Generate a random number between 0 and $1"
  }
]
```

You can use `$@` to pass all arguments and `$1`, `$2`, etc. to pass specific arguments. The script can be a shell command, PowerShell command, or a path to an executable.