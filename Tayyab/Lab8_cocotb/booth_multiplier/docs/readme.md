# Booth multiplier

Multiplier unit using Booth's multipler algorithem

```
Parameters: NUMBITS     : number of bits (width) of multiplier and multiplicand

Inputs: clk             : clock signal
        reset           : reset signal (active low)
        num_a, num_b    : <NUMBITS> wide multiplier and multiplicand.
                            Must be stable for 1 clock cycle after start signal.
        valid_scr       : valid signal from source signaling availability of inputs (num_a, num_b)
        ready_dst       : ready signal from detination signaling that output (porduct) has been processed

Outputs: ready           : set to 1 when result (product) is available
         product         : <2*NUMBITS> wide result of num_a * num_b
         valid_dst       : valid signal to destination signaling availability of output (product)
         ready_scr       : ready signal to source signaling that inputs (num_a, num_b) has been processed

Supports valid/ready interface.
```
### Reference model
Python reference model is preset in sim/ref_models

### Run tests
Cocotb is used for simulation. The python reference model and testbench are used.

`make`\
Runs cocotb simulation.

`clean`\
Cleans build files.