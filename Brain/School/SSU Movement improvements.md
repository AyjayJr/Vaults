# Sliding fix

What is wrong with it?
- Feels bad
- overall weird physics

I believe at least one of the problems is that when the player crouches it cuts the height in half. Thus, there is a moment where the player is suspended in the air. The current fix adds a downward force to the player to push him down in connection with the floor.

*Ideas for solution:*
- hmmm not sure what i need, better understanding of the script as a whole first

task #1: read through the movement scripts and watch dave videos for a better understanding of how the crouch and slide work. the goal is to allow the player to preserve momentum in the air and crouch/uncrouch should not kill momentum. 