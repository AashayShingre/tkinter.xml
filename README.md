**

# Tkinter.XML
XML made for making tkinter applications. Help easy layout and modular design.


Example usage:
**my-tkml.xml**

    <Window  formName = "My First TKML"  layout="pack">
	    <Menu>
		    <MenuOption>Pink</MenuOption>
			<MenuOption>Blue</MenuOption>
		    <MenuOption>Red</MenuOption>
			<Menu  name="Dark">
			    <MenuOption>Black</MenuOption>
			    <MenuOption>Grey</MenuOption>
			    <MenuOption>Dark Metal</MenuOption>
		    </Menu>
	    </Menu>
	    <Label>Hello World!</Label>
	    <Label imageSrc="C:\Users\lenovo\Pictures\Wallpapers\AbandonedVillageChina.jpg"  compound="center"  imageHeight="50"  imageWidth="200" fg="yellow"  bg="black">
		    Welcome Tkinter.XML!!
	    </Label>
	    <Button>Test btn</Button>
    </Window>

**my-tkml.py**

    from tkinterxml import TKML
    from sys import argv
    
    tkmlfile = argv[1]
    a = TKML(tkmlfile)
    builtWindow = a.getBuiltWindow()
    
    button_tags = a.getTag('Button') ##returns a list of all tkinter button instances
    button_tags[0]['text'] =  "Press"
    
    builtWindow.mainloop()
