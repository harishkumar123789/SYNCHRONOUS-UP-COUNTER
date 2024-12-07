### SYNCHRONOUS-UP-COUNTER

**AIM:**

To implement 4 bit synchronous up counter and validate functionality.

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**4 bit synchronous UP Counter**

If we enable each J-K flip-flop to toggle based on whether or not all preceding flip-flop outputs (Q) are “high,” we can obtain the same counting sequence as the asynchronous circuit without the ripple effect, since each flip-flop in this circuit will be clocked at exactly the same time:

![image](https://github.com/naavaneetha/SYNCHRONOUS-UP-COUNTER/assets/154305477/d5db3fa0-e413-404c-b80e-b2f39d82e7e8)


![image](https://github.com/naavaneetha/SYNCHRONOUS-UP-COUNTER/assets/154305477/52cb61eb-d04b-442d-810c-31185a68410b)

Each flip-flop in this circuit will be clocked at exactly the same time.
The result is a four-bit synchronous “up” counter. Each of the higher-order flip-flops are made ready to toggle (both J and K inputs “high”) if the Q outputs of all previous flip-flops are “high.”
Otherwise, the J and K inputs for that flip-flop will both be “low,” placing it into the “latch” mode where it will maintain its present output state at the next clock pulse.
Since the first (LSB) flip-flop needs to toggle at every clock pulse, its J and K inputs are connected to Vcc or Vdd, where they will be “high” all the time.
The next flip-flop need only “recognize” that the first flip-flop’s Q output is high to be made ready to toggle, so no AND gate is needed.
However, the remaining flip-flops should be made ready to toggle only when all lower-order output bits are “high,” thus the need for AND gates.

**Procedure**
1. Type the program in Quartus software.
2. Compile and run the program.
3. Generate the RTL schematic and save the logic diagram.
4. Create nodes for inputs and outputs to generate the timing diagram.
5. For different input combinations generate the timing diagram.

/* write all the steps invloved */

**PROGRAM**
```
Developed by HARISH KUMAR S 
Register no: 24010415
**UP Counter**
module ex11(out,clk,rstn);
input clk,rstn;
output reg [3:0]out;
always @(posedge clk)
begin
   if (!rstn)
	    out<=0;
	else
	    out<=out+1;
end
endmodule
**DOWN COUNTER**
module unit11(out,clk,rstn);
input clk,rstn;
output reg [3:0]out;
always @(posedge clk)
begin
   if (!rstn)
	    out<=0;
	else
	    out<=out-1;
end
endmodule
```
**RTL LOGIC UP COUNTER**
![Screenshot 2024-12-07 113547](https://github.com/user-attachments/assets/c5940d5f-d6ab-4ee1-b985-0a1155d769c0)
![Screenshot 2024-12-07 114942](https://github.com/user-attachments/assets/9ef8b08f-e8e3-4d1d-a087-23eaa06e1176)


**TIMING DIAGRAM FOR IP COUNTER**
![Screenshot 2024-12-07 114419](https://github.com/user-attachments/assets/afb72ce6-fc2e-44c3-86c4-f5097d5a3723)

![WhatsApp Image 2024-12-07 at 12 03 53_597b47ad](https://github.com/user-attachments/assets/cfff9a73-0844-42af-a3c5-9f51583f79ad)


**STATE TABLE**

![WhatsApp Image 2024-12-07 at 12 00 00_c9714afd](https://github.com/user-attachments/assets/25145b3a-973c-4037-86b0-af37d0d8250f)


**RESULTS**
Thus the  4 bit synchronous up counter and down counter are verified and the logic diagrams are designed the truth tables are verified .
