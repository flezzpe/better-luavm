# better-luavm is a script for matcha that complements the usual luavm documentation and adds many things
better-luavm is still under development and needs a lot of new features and ideas, right now it is just a tesot product to develop luavm in matcha


Example:

```lua
--// loader takes only 1 line of your code and should always go above the provided functions
--// get loader from: https://github.com/flezzpe/better-luavm/blob/main/loader.lua

--// [loader.lua]

create_folder('Example') --// make folder in Matcha folder
```

Simple whitelist system:
```lua
--// [loader.lua]

local userhwid = gethwid()

local hwids = {
	'5VF41D0Y6CCW-DW',
	'FSICZHUJENV1-BW',
	'DIK82ZJGF81-DZ'
}

local is_whitelisted = false

for index = 1, #hwids do
	hwid = hwids[index]

	if hwid == userhwid then
		is_whitelisted = true
	end
end

if not is_whitelisted then
	setclipboard(userhwid)
	printl('Not whitelisted! - hwid copied in clipboard.')
	

	return
end

printl('Whitelisted!')
```

Functions:

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
