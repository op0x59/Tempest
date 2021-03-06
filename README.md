# Tempest

## What this Is
Tempest is a fully functional scripting language that extends off of its precursor, lua.
Tempest uses the Compiler REDC (Red Compiler) to compile red lua and run the language.
Tempest adds many new libraries to the Red Lua language, here is a list.
  - Tempest Forms
  - Assembler
  - Disassembler
  - Memory Library
  - Native Function Interface

## What is REDC
REDC or the Red Compiler is a scripting language compiler that is based on lua. It runs at speeds way faster than regular lua.
REDC adds language extensions like
```lua
--[[
  Example of Inline Functions.
  Could be useful for AOT Obfuscation.
--]]
@inline{} function add(num1, num2)
  return num1 + num2
end

print(add(2, 2))
```
```lua
function assembly_test()
  local ret
  @assembly{}
    mov int64(ret), 1337
  @endassembly{}
  
  return ret;
end

assert(assembly_test() == 1337, "Assembly Test failed!")
```
```lua
@export{as = "test"} function export_test()
  return 0
 end
 
assert(exports["test"] == export_test, "Export Test failed!")
```
there are many other extensions that are like this which will be revealed in due time.

## Who is this Made By
The Tempest Developer Team consists of:
  - 0x59 (https://github.com/op0x59)
  - DOGGO/KowalskiFX (https://github.com/JujharSingh)

## What is the Goal
The goal of tempest is to create a fully functional programming language that can compile itself.
We hope to get to speeds never seen before, as well as extensions that make the programming language really easy to use, while supplying the user with a good api and language to use.
