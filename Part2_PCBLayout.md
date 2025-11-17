# PCB Layout

The next step is to define the shape of your PCB and the layout of where the components will physically go on the board. Open the PCB editor by hitting the green PCB editor button at the top right of the schematic editor, or by selecting "PCB Editor" from the project window.

# PCB Layers

![PCB cross section](https://jpfile1.oss-accelerate.aliyuncs.com/allpcb/web/image/20250909/6389303466214455969409416.jpg)

A circuit board is made of multiple layers of different materials laminated together into a kind of composite sandwich. In the PCB editor, these layers are shown in the right sidebar.

* Copper layers (Front/Back): The conductive copper layers making the electrical connections in the PCB. You'll see the components come with copper "pads" where they will be soldered to the PCB later. We'll draw "traces" or wires on the copper layers to connect up these pads as defined in the schematic.
* Paste layers: These layers are used to define where solder will be placed by automated soldering machines. Since we'll be soldering these by hand, you don't need to worry about these layers.
* Silkscreen: The silkscreen layers are used to paint markings and designs on the front and back of the PCB. You can see the components come with silkscreen labels to show you what direction to place the component and their identifier so you know which component goes where. The silkscreen layers are where you can really make the PCB look its best by adding graphics, QR codes, and other artwork.
* Mask: This defines the cutouts in the "solder mask" insulation that protects the copper layers. This is where the insulation is exposed on the component pads so that you can solder to the copper underneath. The mask layer is generally pre-defined by the component pads, so you shouldn't need to touch anything here.
* Edge.Cuts: This layer is used to draw the edge of the PCB. The factory will use this line to cut out the final PCB, so this defines the shape and size of your board. This must be a single closed loop.
* Margin, Courtyard: These layers define the space components physically take up on the front and back of the board. This is used to make sure you don't accidentally place components too close to each other.
* Fab: This layer is where you can make notes. The shapes on this layer won't affect the PCB design, so you can use this to draw guide lines or anything else to help with your design. The template includes some dimension lines showing the 100x100mm size limit as well as center lines.
