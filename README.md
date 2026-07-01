# Tripwire
Adding a TV remote board into your security circuit is actually a clever way to move from a "simple alarm" to a "Wireless Remote Kill-Switch."  A TV remote board is an Infrared (IR) Transmitter. Its job is to blast invisible light pulses. If you add it to the mix, you turn your passive magnetic alarm into an active-controlled security node.

*The "Optical Gate" (Instead of a Magnet)*
You can replace the magnet/mechanical switch entirely with the TV remote board.

The Concept: Infrared light is just another type of switch. If you have an IR Receiver (often found in the monitor or the TV stick), you can build an "Invisible Laser Tripwire."

The Build: Use the TV remote board to point a constant beam of IR light at a receiver mounted across a doorway. As long as the receiver sees the light, the alarm is off. If someone walks through the doorway and breaks the beam, the receiver loses the signal and trips your buzzer circuit.

An "Optical Gate" (or Light Curtain) is a form of non-contact physical security. While a magnetic switch requires the door to physically move a magnet away from a sensor, an optical gate uses a beam of light to create an invisible "tripwire."

Here is how the system functions as a physical security barrier:

1. The Core Components
Emitter (The TV Remote Board): This board is repurposed to act as a constant source of Infrared (IR) light. Because IR light is invisible to the human eye, the "gate" is completely undetectable.

Detector (The IR Receiver): This is typically a small, three-pin component salvaged from your monitor or TV stick. It is designed to "look" for the specific frequency of IR light emitted by the remote board.

The Logic Circuit: A simple transistor-based circuit connects the detector to your buzzer.

2. The Operational Logic
The gate operates in a "Normally Closed" (NC) logical state:

Armed State (Beam Active): The IR emitter is powered, shooting a constant stream of light across the doorway to the receiver. As long as the receiver senses that light, it keeps the buzzer circuit open (the buzzer remains silent).

Triggered State (Beam Broken): If someone walks through the doorway, their body blocks the IR beam. The receiver instantly stops "seeing" the light.

The Alarm: The sudden loss of signal at the receiver causes the transistor to flip its state, immediately closing the circuit and allowing electricity to flow from your 9V battery to the buzzer.

3. Engineering Advantages for Security
Invisible Perimeter: Unlike a magnetic switch that can be seen by an intruder, an optical gate can be mounted inside a door frame or behind molding, making it a "hidden" sensor.

Distance Versatility: A magnet only works if the door is within millimeters of the frame. An optical gate can span an entire hallway or a large garage entryway.

Hard to Bypass: Because the beam is narrow, an intruder would have to know exactly where the light is crossing the room to step over or under it.

4. The "Hack" Challenge
To make this work with your scrap hardware, you need to solve one technical hurdle: Modulation.
TV remote boards are designed to pulse light (to send data), not to shine it steadily. The IR receiver will likely "ignore" a steady light source and only respond to the pulsed signal from a remote.

To fix this, you have two options:

The "Clicker" Trick: Keep the remote button pressed down (or tape it down). The remote will blast the pulsed signal continuously. The receiver will see this constant stream of pulses as a "High" signal, keeping your alarm silent. When someone walks through, they block the pulses, the signal drops, and the alarm trips.

Continuous IR LED: If you can extract just the IR LED from the remote board and power it directly with a resistor and a 3V battery, you get a steady beam. This is much easier for a basic receiver to detect.
