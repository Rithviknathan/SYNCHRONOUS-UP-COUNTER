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

/* write all the steps invloved */

**PROGRAM**

/* Program for flipflops and verify its truth table in quartus using Verilog programming. 
```
module EXP11DE(out,clk,rstn);
input clk,rstn;
output reg [3:0]out;
always @ (posedge clk)
begin
   if(!rstn)
		out<=0;
	else
		out <= out+1;
end
endmodule
```
Developed by: RegisterNumber: 212223100045

**RTL LOGIC UP COUNTER**
<img width="2557" height="1524" alt="Screenshot 2025-10-16 134525" src="https://github.com/user-attachments/assets/dea46ff9-33cb-485c-90f4-c2531abf9cff" />

**TIMING DIAGRAM FOR IP COUNTER**
<img width="2557" height="1525" alt="Screenshot 2025-10-16 134840" src="https://github.com/user-attachments/assets/55a61cd2-e50a-4383-ab99-370b3ae7bfea" />

**TRUTH TABLE**
![WhatsApp Image 2025-10-16 at 13 52 51_d989cb20](https://github.com/user-attachments/assets/73889eb7-6d22-4622-ba9f-635b7d52b616)

**RESULTS**
The implementation of 4 bit synchronous up counter and validate functionality is executed successfully.
