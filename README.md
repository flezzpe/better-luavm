# better-luavm is a script for matcha that complements the usual luavm documentation and adds many things
better-luavm is still under development and needs a lot of new features and ideas, right now it is just a tesot product to develop luavm in matcha


Examples:

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

# Vector3
```lua
Vector3.new(X <number>, Y <number>, Z <number>)
```
Example
```lua
printl(Vector3.new(0, 15, 0).Y) --// Output: 15
```

# Vector3 Get Vectors
return last vector3 value
```lua
Vector3:get_vectors()
```
Example
```lua
Vector3:new(15, 23, 0)

printl(Vector3:get_vectors()) --// Output: 15, 23, 0, but in Matcha [unknown type] [unknown type] [unknown type]
```

# Vector3 Zero
```lua
Vector3:zero()
```
Example
```lua
printl(Vector3:zero()) --// Output: 0, 0, 0
```

# Vector3 One
```lua
Vector3:one()
```
Example
```lua
printl(Vector3:one()) --// Output: 1, 1, 1
```

# Shutdown
```lua
shutdown()
```
Example
```lua
shutdown() --// Shuts down Roblox
```

# Get Bytes
```lua
get_bytes(data <string>)
```
Example
```lua
printl(get_bytes('hello world!')) --// Output: \104\101\108\108\111\32\119\111\114\108\100\33
printl('\104\101\108\108\111\32\119\111\114\108\100\33') --// Output: hello world!
```

# Base64 Encode
```lua
base64_encode(input <string>)
```
Example
```lua
local encoded = base64_encode('hello world!')

printl(encoded) --// Output: aGVsbG8gd29ybGQh
```

# Base64 Decode
```lua
base64_decode(input <string>)
```
Example
```lua
local decoded = base64_decode('aGVsbG8gd29ybGQh')

printl(decoded) --// Output: hello world!
```
