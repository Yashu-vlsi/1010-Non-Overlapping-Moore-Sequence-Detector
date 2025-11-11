1010 Non-Overlapping Moore Sequence Detector

*This project implements a non-overlapping Moore finite state machine (FSM) 
that detects the binary sequence “1010” on a serial input a.
*Whenever this sequence appears, the FSM asserts the output signal y = 1.
*It is a non-overlapping detector — meaning that after a valid detection, 
the FSM restarts from the beginning of the sequence before recognizing a new one.

//FSM Coding Style 1 
FSM Coding Style 1 is one of the most commonly used and structured ways of implementing a Finite State Machine (FSM) in Verilog.
It divides the FSM into three main parts, each handling a specific function in the design.
This separation improves readability, synthesis reliability, and debugging clarity.
The first part is the state register block, which is sequential logic. It stores the present state and updates it on every clock edge or when the reset signal is active. 
The second part is the next-state logic block, which is purely combinational. It decides what the next state should be based on the current state and the input conditions. 
The third part is the output logic, which produces the FSM output. In a Moore FSM, the output depends only on the current state.

//FSM Coding Style 2 – Next-State and Output Combined
In Coding Style 2, the FSM design uses two blocks instead of three.
Sequential block for present state register.
Combinational block that handles both next-state logic and output logic together.
