## Introduction:

A finite state machine (FSM) its a abstract mathematical model of a machine that can assume only one state at time of a finite list of possible states.
The FSM can change from one state to another in response to an external input and this change is called transition. The FSM is defined by your list of states, your initial state and the conditions for each transition.

## Description:

Implements the class FiniteStatesMachine that have the following list of states: started, collecting, processing and stopped.

The initial state of the FSM object should be stopped and the class must implements the following methods: getPreviousState, getCurrentState and setCurrentState.
The state transitions must occur accordingly the following table:

Actual state      Input         Next state
stopped           start         started

started           collect       collecting
started           stop          stopped

collecting        process       processing
collecting        stop          stopped

processing        stop          stopped

Also implements the following methods: collectData and processData, that will be used during the states collecting and processing, respectively.

To simulate the data collection, the collectData method must use the class array from NumPy to generate and return a array of size 3x3 containing random numbers between 0 and 9. After finishes the data collection, prints to the user a info message and perform the transition to the processing state.

The processData method must receive the collected data and run the following processing operations: multiply each element by the scalar 5 and calculate the transposed of this result. After this processing stage, prints the final result to the user and perform the transition to the collecting state.

At any time, the user must be allowed to send a input command to the FSM to achieve a state transition accordingly to the previous table.
