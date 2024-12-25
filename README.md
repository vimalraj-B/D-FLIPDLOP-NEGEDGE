# D-FLIPDLOP-NEGEDGE

**AIM:**

To implement  D flipflop using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**D Flip-Flop**

D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.

![image](https://github.com/naavaneetha/D-FLIPDLOP-NEGEDGE/assets/154305477/48c81fe8-bc3f-40e7-95e2-519fc155ad51)

This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable. The following table shows the state table of D flip-flop.

![image](https://github.com/naavaneetha/D-FLIPDLOP-NEGEDGE/assets/154305477/e5f3fda7-68ec-4a3a-a0a4-cf6f9cc4ab55)

Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as Qt+1t+1 = D

![image](https://github.com/naavaneetha/D-FLIPDLOP-NEGEDGE/assets/154305477/8592c0d8-2917-4142-91b9-d6c30dd891d2)

Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.

**Procedure**

```

 1).Type the program in Quartus software.
 2).Compile and run the program.
 3).Generate the RTL schematic and save the logic diagram.
 4).Create nodes for inputs and outputs to generate the timing diagram.
 5).For different input combinations generate the timing diagram

```
**PROGRAM**

```
module d(d, clk, rst, q);
  input d, clk, rst;
  output reg q;

  always @(negedge clk or posedge rst) begin
    if (rst)
      q <= 0; // Reset the flip-flop
    else
      q <= d; // D input is passed to Q on the negative clock edge
  end
endmodule


```

![D](https://github.com/user-attachments/assets/bb6a135b-80fc-4442-b939-3cd1cd1b8b7e)



```

Developed by:B.VIMALRAJ
RegisterNumber:24900283.

```


**RTL LOGIC FOR FLIPFLOPS**

```
D FLIP FLOP:
```
![D (2)](https://github.com/user-attachments/assets/4b6a6310-b7d5-4f8a-b8a4-1b0d50116e52)

**TIMING DIGRAMS FOR FLIP FLOPS**

```
D FLIP FLOP:
```
![Screenshot 2024-12-25 211648](https://github.com/user-attachments/assets/6bb2a69a-b4c8-4880-b85f-92edb4e2c2ba)




**RESULTS**

```
Thus the D Flip Flop expression is verified using Quartus software.

```
