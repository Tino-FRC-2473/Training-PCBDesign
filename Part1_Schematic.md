# Schematic

The first part of any PCB design is to draw the schematic that describes the electrical circuit for your PCB.

Since this isn't an electrical engineering training, the basic circuit has already be designed for you. However there are some details that still need to be completed that will give you an introduction to reading and navigating a circuit schematic diagram.

# Reading a Schematic

![Schematic overview](images/SchematicOverview.png)

The schematic shows the components that make up an electrical circuit and the connections between them. 

![Schematic component](images/SchematicComponent.png)

In KiCad's default color scheme, the components are drawn in red. You'll see each component has blue labels next to it with a unique identifier like `R101` or `C102` and the component's value or description. 

![Wire junction](images/WireJunction.png)

The wires between the components are drawn in green. Note that when two wires connect to each other, the junction is shown with a green dot. 

![Wire Crossing](images/WireCrossing.png)

If two wires cross without a dot, then the wires do not connect at that point. 

Finally, you'll set at the top and bottom there are connections to an upward pointing arrow labeled `+9V` and a downward pointing triangle labeled `GND`. 

![Ground symbol](images/GNDSymbol.png) ![Power symbol](images/PowerSymbol.png)

These power symbols are used to mark connections to common reference voltages, in this case the positive and negative power connections to the 9V battery. Ground or `GND` is used to denote 0V, which is the point all the other voltages in the circuit are measured from. Note that all symbols of the same voltage are connected together, so the +9V is connected to both the main circuit and the positive terminal of the battery to the right. This helps to avoid drawing lots of wires everywhere we need power and ground, making the schematic easier to read.

# Circuit Components

Now let's go over what components we'll be using in this circuit.

## Resistors

![Resistor symbol](images/ResistorSymbol.png)

Resistors help restrict the flow of electrical current in the circuit. When there is a voltage difference from one side of the resistor to the other, the resistor allows a limited amount of current to flow proportional to how much voltage is applied. Exactly how much current is determined by the resistance of the resistor, measured in Ohms (Ω). The exact formula is $Current = \frac{Voltage}{Resistance}$, so a 1 Ohm resistor will allow 1 Amp of current to flow when 1 Volt of voltage is applied.

In the schematic, resistors are labeled starting with the letter R. Notice that the value of the resistor in Ohms is written underneath the identifier. Since resistor values can get very large, the value is written with SI prefixes. So a 1k resistor has a value of 1 kiloOhm, or 1,000 Ohms. A 1M resistor has a value of 1 MegaOhm, or 1,000 kiloOhms, or 1,000,000 Ohms.

## Capacitors
