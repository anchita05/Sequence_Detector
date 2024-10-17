A sequence detector is an example of Finite State Machine (FSM) where the hardware is expected to detect a fixed pattern in the input binary bits.

Moore State Machine:

    In Moore machine, output only depends on the present state. 
    It is independent of current input.

    1. Non-Overlapping Moore State Machine:  
        In this type of sequence detector does not allow overlap, but resets itself to the start state when the sequence has been detected.
        For example:
        After the initial sequence 1101 has been detected, the detector with no overlap resets and starts searching for the initial 1 of the next sequence.
    2. Overlapping Moore State Machine:  
        In this type of sequence detector allows overlap, the final bits of one sequence can be the start of another sequence.
        For example: There will be a 1101 sequence detector. It raises an output of 1 when the last 4 binary bits received are 1101.

Mealy State Machine: 
    
    In mealy machine, output depends on the present state and current input. 

    1. Non-Overlapping Mealy State Machine 
        In a non-overlapping sequence detector, the last bit of one sequence does not become the first bit of the next sequence.    
        For example: 
            Input :0110101011001 
            Output:0000100010000

    2. Overlapping Mealy State Machine 
        In an overlapping sequence detector, the last bit of one sequence becomes the first bit of the next sequence.
        For example: 
            Input :0110101011001 
            Output:0000101010000
