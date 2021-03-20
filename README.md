Exercise 6: And now for the tricky bit
======================================

*This exercise should be handed in as a group, as the final project design hand-in before the design review*

From the last two design rounds, you should have a rough plan for how the elevators interact, what the components (modules) for a single elevator are, and how those components interact. From the last two project milestones, you should also have some way to send messages over a network, and the start of a module that can run a single elevator.

For this design hand-in, you should select one module from your design, and provide a detailed design for it. The module you choose should be either a) The module you expect to be the hardest one to create, or b) The module that is currently the least clear part of your design (or rephrased: currently most hand-wavy and vaguely defined).

The reason for choosing "hardest" / "least clear" (instead of "the one it makes most sense to start programming next") is that being stuck with making the hardest part last might require re-designing all the easy parts, and - if you started programming - possibly re-implementing them. 
 
Here are the considerations you should reflect upon:

 - Before designing anything - why did you choose this module?
   - Why do you expect it to be hard, or what is currently unclear?
   - We think the movment module is going to be the most trickey. We have to manage the que in an order make it consitent.
   - If things seem quite clear *now*, mentally time-travel back to when they were not: what was the last piece to fall in place?
 - What does this module do?
 - it controls the movement
   - What are its outputs?
   - floor it is going to. (movment up, down or idle)
   - Both in name (what you call these outputs), and in kind (what their data type is)
   -  datatype int and MD_down MD_up
 - What does this module need, in order to do that?
   - What are its inputs?
   -  What floor the elevator is in. button pushes. timer. 
   - What is its state (local data)? 
   - Again: both in name and in kind
   - Is it (conceptually) necessary to know where the inputs come from?
     - As in: do you need to know this when making this module, or just when integrating it with the rest of the system?
     - no
 - What needs to be done to tie inputs, state, and outputs together?
   - What needs to be done when you receive each input?
     - Or if you are output-oriented: what needs to be done to calculate each output?
     - the queue
   - What are the sub-modules you need?
     - Mostly, these will probably be functions
     - the queue (mabye an own module?), direction, 
     - But maybe, you manage threads/tasks/objects (whatever your module-thing is) hierarchically



 
