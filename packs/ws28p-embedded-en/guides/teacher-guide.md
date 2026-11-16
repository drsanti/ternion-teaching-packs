# Embedded basics with the ws28p — teacher guide

Three lessons of about 40 minutes: sense–think–act, buttons and bouncing, signals and sampling. A robotos ws28p board and a USB cable per student or pair is ideal; without one, every lesson runs on the simulated board and every check still passes.

## Before the course

- Connecting a real board needs Chrome or Edge (Web Serial).
- Open each lesson once and press Run on an exercise, so the Python runtime is downloaded.

## The board checks

- Each lesson's second slide connects the board for the rest of the lesson.
- A check runs for its number of seconds after Start and reports each condition; the simulated board passes them all (its PWR button pulses every 4 s, its tilt wanders slowly).

## Grading

- Exercises are checked after every run; hidden checks are graded on your computer during a class. Solution slides are teacher-only.

## Common mistakes

- Forgetting to subtract lo when mapping (exercise 1).
- Counting every 1 instead of each 0 → 1 change (exercise 3).
- Slicing one too many or too few (exercise 5).
