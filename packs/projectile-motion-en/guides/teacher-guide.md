# Projectile motion — teacher guide

Three lessons of about 40 minutes: falling, launching, the pendulum. No equipment: the simulations run in the browser and the exercises are Python cells on the slides.

## The simulations

- Lessons 1 and 2 use a 2D physics world. Press **Play**; **Step** advances one frame; **Reset** puts the bodies back. Students with their own device get their own copy and may change the values the slide lists (gravity, a speed, the bounce).
- Lesson 3's bob follows the pendulum formula, so it swings as soon as the slide is shown.

## Grading

- Each exercise is checked after every run; hidden checks are graded on your computer during a class.
- Answers are rounded to two decimals with round(x, 2), so the checks compare exact values.
- Solution slides are teacher-only.

## Common mistakes

- Degrees where radians are wanted: math.sin takes radians (lesson 2).
- Forgetting round(…, 2), so the check sees 2.0192… instead of 2.02.
- Squaring the wrong thing in the pendulum formula (lesson 3).
