# JKFLIPFLOP-USING-IF-ELSE

**AIM:** 

To implement  JK flipflop using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**JK Flip-Flop**

JK flip-flop is the modified version of SR flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of JK flip-flop is shown in the following figure.

![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/a649c30b-232b-4558-b188-fd6c09845180)


This circuit has two inputs J & K and two outputs Qtt & Qtt’. The operation of JK flip-flop is similar to SR flip-flop. Here, we considered the inputs of SR flip-flop as S = J Qtt’ and R = KQtt in order to utilize the modified SR flip-flop for 4 combinations of inputs. The following table shows the state table of JK flip-flop.

![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/c4360742-e8a8-4937-b089-c46c0433f9a3)

 
Here, Qtt & Qt+1t+1 are present state & next state respectively. So, JK flip-flop can be used for one of these four functions such as Hold, Reset, Set & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of JK flip-flop. Present Inputs Present State Next State
 
![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/6c275261-a6d5-4c37-a3a7-1e88ca11c4cd)

By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. Three variable K-Map for next state, Qt+1t+1 is shown in the following figure.
 
![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/5174f41b-0ce0-4329-a372-6d1943ea6673)

The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is Q(t+1)=JQ(t)′+K′Q(t)Q(t+1)=JQ(t)′+K′Q(t)

**Procedure**

1.Connect the circuit on the breadboard/kit using the JK flip-flop IC (e.g., 7476/7473/4027).

2.Give the power supply of +5V and ground to the IC.

3.Connect the clock input to the clock generator or pulse switch.

4.Connect inputs J and K to switches so they can be set to 0 or 1.

5.Connect Q and Q̄ outputs to LEDs or indicators to observe the output state.

6.Set J = 0 and K = 0, then apply a clock pulse and note the output Q (should remain unchanged).

7.Set J = 0 and K = 1, apply a clock pulse and observe the output (Q should reset to 0).

8.Set J = 1 and K = 0, apply a clock pulse and observe the output (Q should set to 1).

9.Set J = 1 and K = 1, apply a clock pulse and observe the output toggle (Q becomes complement of previous state).

10.Repeat the above steps to verify the JK flip-flop behavior for multiple clock pulses.

11.Record all observations in a truth table format.
**PROGRAM**
```
module JK_FF( clk,j,k,q,qbar);
    input clk;
    input j;
    input k;
    output reg q;
    output reg qbar;

    
always @(posedge clk) begin
    if (j == 0 && k == 0) begin
        q <= q;
        qbar <= qbar;
    end 
    else if (j == 0 && k == 1) begin
        q <= 0;
        qbar <= 1;
    end 
    else if (j == 1 && k == 0) begin
        q <= 1;
        qbar <= 0;
    end 
    else if (j == 1 && k == 1) begin
        q <= ~q;
        qbar <= ~qbar;
    end
end

endmodule
```

 Developed by:Thuleer R
 RegisterNumber:212225230285
*/

**RTL LOGIC FOR FLIPFLOPS**
<img width="793" height="438" alt="Screenshot 2025-12-15 211933" src="https://github.com/user-attachments/assets/2cd0f66e-1928-4f80-9350-f780dab20f1b" />

**TIMING DIGRAMS FOR FLIP FLOPS**
<img width="1920" height="1080" alt="Screenshot (68)" src="https://github.com/user-attachments/assets/5bb99367-8b05-4ec5-90ff-61f0f9442db9" />

**RESULTS**
