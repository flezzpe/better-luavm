# better-luavm is a script for matcha that complements the usual luavm documentation and adds many things
better-luavm is still under development and needs a lot of new features and ideas, right now it is just a tesot product to develop luavm in matcha


Example:
```lua
luavm:__init__()
printl(gethwid())
```

Functions:
# Init
```lua
luavm:__init__(in_debug <boolean>)
```

# Create Folder
```lua
create_folder(folder_path <string>)
```

# Download File (can't download .exe and .dll file's for safety reaseons)
```lua
download(url <string>, output_file <string>)
```

# Get Hwid
```lua
gethwid() --// return <string> value
```

# Is File
```lua
isfile(file_path <string>)
```

# Is Folder
```lua
isfolder(folder_path <string>)
```

# Read File
```lua
readfile(file_path <string>) --// return <string> file data
```

# Create Message (Draw message in Matcha output)
```lua
create_message(message <string>) --// Example output: [Better Lua Virtual Machine v0.1.4] - hello world! 
```
