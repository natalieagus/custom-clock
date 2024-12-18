## Custom Clock Project 

A simple project demonstrating the consequence of using other components' output as clk input for a particular component in an attempt to "slow down" the clock. 

Upon running the project, you will see a countdown from 7 to 0 on the 7seg. 

### Observation 

When running the project on simulation, reset works properly. It resets the value displayed on the seven segment back to 7. This is because we use a counter that still utilizes the board's clock. 

When `io_dip[0][0]` is up, reset no longer works on the countdown module. This is because we are using a module which `.clk` signal is supplied by another component. 
