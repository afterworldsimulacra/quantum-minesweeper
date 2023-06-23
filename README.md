### Quantum Minesweeper
for UTS Quantum Hackathon  
(code by Akira Li, Jacky Ly, Joshua Muzik and Salha Alghoraibi)


This project is an 8x8 minesweeper with 10 entangled mines (only 5 of which are definitively dangerous) such that when the player clicks a mine, there is a 50/50 chance of it actually being a mine. However, if a mine did not trigger a game over, then the other mine entangled with it will definitively trigger a game over if hit. Think of it as a *Genshin Impact 50/50* (sorry).

### Minesweeper code explained
insert text here

### Superposition + entanglement
(Akira code explanation) So what I wanted to do was to entangle the 5 pairs of qubits that were associated with specific mine positions such that the probability distributions would be $\frac{\ket{00}}{\sqrt{2}} + \frac{\ket{00}}{\sqrt{2}}$
