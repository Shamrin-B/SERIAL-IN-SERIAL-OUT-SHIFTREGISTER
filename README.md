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
```
1.Type the program in the Quartus software.
2.compile and run the program.
3.geenerate the RTL schematic and save the logical diagram.
4.creat the node for the input and output to generate the timing diagram.
5.for the different input combination generate the timing diagram.
```
**PROGRAM**

/* Program for flipflops and verify its truth table in quartus using Verilog programming.

Developed by:SHAMRIN B.
RegisterNumber:24900144

*/
```
module enp_10(clk,sin,q);
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

**RTL LOGIC FOR SISO Shift Register**

![Screenshot (61)](https://github.com/user-attachments/assets/f16f9e8e-0e5c-4b18-aa43-87806d3497d8)


**TIMING DIGRAMS FOR SISO Shift Register**

![Screenshot (62)](https://github.com/user-attachments/assets/3abe6d63-6224-4e49-85b1-8f98c7f48a06)


**TRUTH TABLE**

![image](https://github.com/user-attachments/assets/522d6a7e-c32f-4da8-b877-3e7c4c9c484b)


**RESULTS**

  SISO Shift Register using verilog and validating their functionality using their functional tables are studied and verified.

