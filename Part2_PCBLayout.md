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

# Component Layout

In the top menu bar, press the "Update PCB from Schematic" button, then click "Update PCB" to ensure the PCB is in sync with the schematic. You'll see all the components have been placed down in the middle of the board. There are also gray lines between the pads showing the connections we'll have to make. If you still have the schematic window open, notice how clicking on a component will also highlight it in the schematic viewer. This can help you keep track of which component is which.

Let's start arranging the components into something more organized. Left click to select a component, and make sure the entire component is highlighted (not just the labels). You can click and drag to simply move the component around. Hit "R" to rotate a component. Start by spacing out the components a bit and rotating them so that we can clearly tell apart the left and right half of the circuit.

# Board Edge

Now let's draw the shape of our PCB. In the right sidebar, select the yellow Edge.Cuts layer. You should see the yellow rounded rectangle shape from the template pop to the front. You can press "H" to hide the other layers and make this more visible. The edge is defined by line segments and curves. You can reposition the existing elements by clicking to highlight, then dragging the endpoints around. In the right sidebar, there are buttons for "Draw Lines" and "Draw Arcs" you can use to add new line segments and arcs. To draw a line, select the draw line tool, then click to start a line. Clicking again will add a line segment. Double clicking or clicking on the starting point will end the line. For arcs, click to define the arc center. Next click to define the radius. Finally move around the center to define the angle of the arc and click to complete the arc.

If you prefer to design your board shape in a different program, you can import an SVG vector shape by selecting File->Import->Graphics. Make sure the select "Edge.Cuts" as the layer, then hit OK. The shape will be imported as a single group which you can drag to the correct position. Make sure to delete any extra line segments first so that there is a single well defined outline for your design.

# Silkscreen Graphics

Once you have your board edge drawn and the components placed where you want them, you can add some decorations on the silkscreen layer. Select the F.Silkscreen layer. You can use the Text tool in the right sidebar to add text objects. You can also import SVG graphics to add more complex designs to the silkscreen layer. Don't forget you can also draw on the B.Silkscreen layer to add designs to the back of your board!

To preview your design, select View->3D Viewer to open a 3D rendering of your board design. This is a good way to check your component placements and verify that your graphics are drawn correctly.