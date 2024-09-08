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
```lua
Tab:AddToggle({
	Name = "This is a toggle!", -- Toggle name
	Default = false,
	Callback = function(Value)
		print(Value) -- What happens when you turn on and off the toggle
	end    
})
```

## Creating a Color Picker
```lua
Tab:AddColorpicker({
	Name = "Colorpicker", -- Colorpicker name
	Default = Color3.fromRGB(255, 0, 0), -- Default color
	Callback = function(Value)
		print(Value) -- What happens when you change the color
	end	  
})
```

## Creating a Slider
```lua
Tab:AddSlider({
	Name = "Slider", -- Slider name
	Min = 0, -- Minimum value
	Max = 20, -- Max Value
	Default = 5, -- Default value
	Color = Color3.fromRGB(255,255,255), -- Slider color
	Increment = 1, -- The increment of the value when you drag on the slider
	ValueName = "bananas", -- Value name
	Callback = function(Value)
		print(Value) -- What happens when you change the slider's value
	end    
})
```

## Creating a Label
```lua
Tab:AddLabel("Label")
```

## Creating a Textbox
```lua
Tab:AddTextbox({
	Name = "Textbox", -- Textbox name
	Default = "Orion on top", -- Default box input
	TextDisappear = true, -- If the text disappears after you press enter
	Callback = function(Value)
		print(Value) -- What happens when you type something in the textbox
	end	  
})
```

## Creating a Notification
```lua
OrionLib:MakeNotification({
	Name = "Title!", -- Notif Title
	Content = "Notification content... what will it say??", -- Notif content
	Image = "rbxassetid://4483345998", -- Notif Image
	Time = 5 -- How much long the notif will stay 
})
```

# EXTRA
## Destroying the GUI
```lua
OrionLib:Destroy()
```

# Thanks for using
Thanks for using the Updated Orion Library! It will soon get an update with more features! We only have put the necessary features for now!
