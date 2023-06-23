### Quantum Minesweeper
for UTS Quantum Hackathon  
(code by Akira Li, Jacky Ly, Joshua Muzik and Salha Alghoraibi)

**edit: WE WON SECOND!

This project is an 8x8 minesweeper with 10 entangled mines (only 5 of which are definitively dangerous) such that when the player clicks a mine, there is a 50/50 chance of it actually being a mine. However, if a mine did not trigger a game over, then the other mine entangled with it will definitively trigger a game over if hit. Think of it as a *Genshin Impact 50/50* (sorry).

### Minesweeper code + mine generation explained
Mine generation is done by creating a quantum circuit with 1 qubit. Then applying a Hadamard gate to create a superposition.

### A mathematical explanation of the superposition + entanglement of mines
(Akira code explanation)  So what I wanted to do was to entangle 10 qubits grouped into 5 pairs that were associated with specific mine positions such that the probability distributions would be $\frac{\ket{01}}{\sqrt{2}} + \frac{\ket{10}}{\sqrt{2}}$ for each pair. Essentially, what this would mean is that there would be a 50% chance of each mine collapsing into the classical state of 0 or 1 when measured, but if it's not triggered, then the mine entangled with it will definitively be.

So how to do this? Bell state 3 (all my homies love bell state 3).
For each pair of qubit, apply the Hadamard gate to the first qubit, and the NOT gate to the second, and then CNOT the two qubits to entangle them (using the first qubit as a control, second qubit as a target). Repeat 5x. This leads to the quantum state (bell state 3) $\frac{\ket{01}+\ket{10}}{\sqrt{2}}$ which is represents the exact 50/50 probability distribution of each possibility needed. 

gg finished :D
