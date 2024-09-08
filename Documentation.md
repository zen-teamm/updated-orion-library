# Updated Orion Library - Documentation
This documentation is for the stable release of Orion Library. This is fully written by Mannuhd.

-- <[[ UPDATE LOGS ]]> --
------------------------------
- Added an open button when closing the GUI | Huge thanks to Axton for helping me.
- Made the GUI Draggable for Mobile devices
-------------------------
## Creating the Library
```lua
local OrionLib = loadstring(game:HttpGet(('https://raw.githubusercontent.com/zen-teamm/updated-orion-library/main/library.txt')))()
```

## Creating a Window
```lua
local Window = OrionLib:MakeWindow({Name = "Title of the library", HidePremium = false, SaveConfig = false, ConfigFolder = "OrionTest"})
```

### Additional Options:
* SaveConfig = true / Saves automatically the config. Not reccomanded.
* IntroEnabled = true / Shows the Intro
* IntroText = "Put your text here" / Changes the intro text

### Code to boot additional options:
* local Window = OrionLib:MakeWindow({Name = "Title of the library", HidePremium = false, SaveConfig = true, ConfigFolder = "OrionTest"}) / Save config 
* local Window = OrionLib:MakeWindow({Name = "Title of the library", HidePremium = false, SaveConfig = false, ConfigFolder = "OrionTest", IntroEnabled = true}) / Enables Intro

* local Window = OrionLib:MakeWindow({Name = "Title of the library", HidePremium = false, SaveConfig = false, ConfigFolder = "OrionTest", IntroEnabled = true, IntroText = "Put whatever you want"}) / IntroEnabled + IntroText

-------
Notes:
* If you dont put IntroText and only put IntroEnabled it will show Orion Library as text.

* You can also put SaveConfig whil you use Intro.
-------
## Creating a Tab
```lua
local Tab = Window:MakeTab({
	Name = "Tab 1", -- Tab Name
	Icon = "rbxassetid://4483345998", -- Asset ID
	PremiumOnly = false -- Outdated
})
```
## Creating a Button
```lua
Tab:AddButton({
	Name = "Button!", -- Button name
	Callback = function()
      		print("button pressed") -- What happens when you press the button
  	end    
})
```

## Creating a Section
```lua
local Section = Tab:AddSection({
	Name = "Section" -- Section Name
})
```
## Creating a Toggle
