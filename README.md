# gate_level_schematics

# Exhibit 0
Fibonacci-sequence generator implemented in [Logisim](http://www.cburch.com/logisim/ "Logisim").

## Implementation
* Schematized with discrete built-in logic gates only

* Sequential logic with custom D flip-flop storage

* Naive generation using the recursion: F_{n}=F_{n-1}+F_{n-2}

* Seed values hardwired to F_{0}=F_{1}=1

* Custom hexadecimal seven-segment display

## Specifications
* 32 D flip-flops forming two 16-bit registers

* Four hexadecimal seven-segment displays

* Clocked at 2 Hz for demonstration purposes, capped at 4.1 KHz 

* Full displayed sequence: 2 -> 3 -> 5 -> 8 -> 13 -> 21 -> 34 -> 55 -> 89 -> 144 -> 233 -> 377 -> 610 -> 987 -> 1597 -> 2584 -> 4181 -> 6765 -> 10946 -> 17711 -> 28657 -> 46368 -> Overflow

## Operation
1. Simulate -> Reset Simulation (Ctrl+R)

2. Toggle on CLK_ENABLE

3. Pulse RESET

4. Simulate -> Ticks Enabled (Ctrl+K) OR manually clock via Simulate -> Tick Once (Ctrl+T)


# Exhibit 1
Hamming distance calculator implemented in [Logisim](http://www.cburch.com/logisim/ "Logisim").

![](/test/hamming.gif)

## Implementation
* Schematized with discrete built-in logic gates only

* Sequential logic with custom D flip-flop storage

* Custom hexadecimal seven-segment display

* Two 16-bit numbers are compared bit-by-bit. The Hamming distance between them--the number of positions at which the numbers differ--is stored in memory and output to a hexadecimal display.

## Specifications
* Bit-by-bit scanner driven by T flip-flop counter

* Four-bit adder tracks distance

* Result stored in four-bit register/accumulator

* One hexadecimal seven-segment display

* Clocked at 16 Hz for demonstration purposes, capped at 4.1 KHz 

## Operation
1. Simulate -> Reset Simulation (Ctrl+R)

2. Toggle CALC to reset memory elements

3. Simulate -> Ticks Enabled (Ctrl+K)

4. Enter binary inputs

5. Toggle CALC again

6. The hexadecimal output to the seven-segment display is the Hamming distance. If the display shows 0xF and the TOTAL? indicator light is on, the display has overflowed. The correct Hamming distance should be taken to be 0x10, or 16.
