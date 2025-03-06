# SR latch



# How do computers remember?

Computers can remember various numbers and store them as bits. They can do this by using gates and latches. Latches hold information unless they are changed.
By connecting multiple latches together you can store larger bits of memory 

# What is a SR latch?

One of the most common ways computers store memory is in a SR latch or Set/Reset latch. But to understand how they work we first must decontruct it.

A SR latch is composed of 2 NOR gates in which the output of one is going into the input of the other and the output of the second one is going back into the the first.

This is a truth table on a NOR gate

![nor-gate-truth-table](https://github.com/user-attachments/assets/8723d4c2-ea96-42db-b50c-bb270db5e6c9)

as you can see the output is only 1 when both inputs are 0

keeping this same logic lets look at a SR latch

![zk3PI](https://github.com/user-attachments/assets/6df23dbb-36b1-4dd5-8331-5fd44fa1937e)

as you can observe, both outputs can't be on. They switch back and forth depending on the state of the inputs

We can use this concept to make many different electrical devices such as a vending machine



# vending machine


lets start with 2 buttons: a Vend button and a Coin button.
Lets take the output of the vend button and lets connect it to the input of an AND gate (remember for AND gates both outputs must be 1 to output a 1)

We want our user to insert a coin AND press the Vend button to receive there item.

From the coin button we need to have an SR latch connected in which the output Q is going into the input of the same AND gate
From Q we can connect a LED indicating that we have a coin inserted
Finally we connect the output of the AND gate to an LED indicating that an item has been vended

Now we have a working vending machine circuit but, notice after we vend an item the LEDs stay on.

to fix this we need to reset the SR latch; if you notice we still have one input not connected to the reset side.

We can simply take a wire going from the output of the AND gate and place a buffer before wiring it into the reset of the SR latch


# These are the picture to my SR latch
![Screenshot 2025-02-18 133038](https://github.com/user-attachments/assets/a504a83e-a6e5-48d2-8fea-dd4fadd3ec02)


![IMG_1892](https://github.com/user-attachments/assets/0e3720af-bdb3-4a8a-9fe4-4c1fa942c057)

![IMG_1890](https://github.com/user-attachments/assets/91b1732b-d0d2-41d4-ae76-8f8bcdeb4cb1)

# These are the pictures to the vending machine 

# No button is pressed:
![Vending machine pic 1](https://github.com/user-attachments/assets/95c4c607-a59d-4ee8-a8a4-740d8c3f8da8)


# Coin button is pressed and the machine remembers:
![Vending machine pic 2](https://github.com/user-attachments/assets/8d60d364-bed4-4e35-b857-336cd2489d3b)



# Vend button is pressed and the machine is reset:
![Vending machine pic 3](https://github.com/user-attachments/assets/bfea73f6-4856-4774-85f0-7175b33ce1ef)





