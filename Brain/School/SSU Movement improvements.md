# Sliding fix

Ok so I removed crouch entirely and the slide feels pretty ok I believe.

I first need to make sure the sliding on slopes works well which I think it does.

Then I have to figure out why you get that little minijump after the slide.
- Could have something to do with some of the values on the player movement script
- Could have something to do with the jump cooldown timer
- Could have something to do with the player collider being small during
	- make it so that jump first makes the player full size

Ok those are all potential things to look at.

---
# Falling bug

There's a bug where when you are falling for a certain amount of time or distance your momentum suddenly drops to around 5 from 10.

What could be making this happen?

