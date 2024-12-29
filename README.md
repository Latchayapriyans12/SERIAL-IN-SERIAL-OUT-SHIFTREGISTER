# SERIAL-IN-SERIAL-OUT-SHIFTREGISTER

**AIM:**

To implement  SISO Shift Register using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**SISO shift Register**

A Serial-In Serial-Out shift register is a sequential logic circuit that allows data to be shifted in and out one bit at a time in a serial manner. It consists of a cascade of flip-flops connected in series, forming a chain. The input data is applied to the first flip-flop in the chain, and as the clock pulses, the data propagates through the flip-flops, ultimately appearing at the output.

The logic circuit provided below demonstrates a serial-in serial-out (SISO) shift register. It comprises four D flip-flops that are interconnected in a sequential manner. These flip-flops operate synchronously with one another, as they all receive the same clock signal.

![image](https://github.com/naavaneetha/SERIAL-IN-SERIAL-OUT-SHIFTREGISTER/assets/154305477/e81c4072-37f9-46c6-8145-566764b74c3a)

Figure 01 4 Bit SISO Register

The synchronous nature of the flip-flops ensures that the shifting of data occurs in a coordinated manner. When the clock signal rises, the input data is sampled and stored in the first flip-flop. On subsequent clock pulses, the stored data propagates through the flip-flops, moving from one flip-flop to the next.
Each D flip-flop in the circuit has a Data (D) input, a Clock (CLK) input, and an output (Q). The D input represents the data to be loaded into the flip-flop, while the CLK input is connected to the common clock signal. The output (Q) of each flip-flop is connected to the D input of the next flip-flop, forming a cascade.

**Procedure**

1 Type the program in Quartus software.

2 Compile and run the program.

3 Generate the RTL schematic and save the logic diagram.

4 Create nodes for inputs and outputs to generate the timing diagram.

5 For different input combinations generate the timing diagram.

**PROGRAM**


```
module siso_10(clk, sin, q);
input clk;
input sin;
output [3:0] q;
reg [3:0] q;
always @(posedge clk)
begin
q[0] <= sin;
q[1] <= q[0];
q[2] <= q[1];
q[3] <= q[2];
end
endmodule
```

Developed by:latchaya priyan.S

RegisterNumber:24900388


![399090167-5d271fea-7abe-47f3-a8e5-e8a1b785dbc9](https://github.com/user-attachments/assets/8e4659cf-7a3b-450c-bb8b-589956577a8a)


**RTL LOGIC FOR SISO Shift Register**

![399090206-8a59eb0e-79a3-4481-bcf0-45b3e9d204bd](https://github.com/user-attachments/assets/80fad6f0-919c-4a57-9128-c7a67598fd36)


**TIMING DIGRAMS FOR SISO Shift Register**

![399090307-df9fe13c-f2db-428e-a6f6-53e2125c4e7d](https://github.com/user-attachments/assets/2195077e-6c44-4bee-8a21-2ffc5729e0c6)


**RESULTS**

Thus the Serial in and Serial out shift Register expression is verified using Quartus software
