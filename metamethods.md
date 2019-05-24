# Tempest

## Metamethod Additions
REDC happens to add in many useful metamethods for userdata's in lua.
Here is a list of all the metamethods and what they change or do.

```lua
local object = setmetatable(newproxy(), {
  __implicit_cast = function(self, type) end --print(self)
})
```
```lua
local object = setmetatable(newproxy(), {
  __explicit_cast = function(self, type) end --print(string(self))
})
```
```lua
local object = setmetatable(newproxy(), {
  __new = function(...) end --new self()
})
```
```lua
local object = setmetatable(newproxy(), {
  __uhash = function(self) end --#self
})
```
```lua
local object = setmetatable(newproxy(), {
  __umultiply = function(self) end --*self
})
```
```lua
local object = setmetatable(newproxy(), {
  __uminus = function(self) end -- -self
})
```

If any new metamethods are not on here it is most likely due to I usually update this documentation while in school.
So new metamethods could be added at any time.
