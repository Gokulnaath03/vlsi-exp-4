# vlsi-exp-4

#AIM: To simulate and synthesis SR, JK, T, D - FLIPFLOP, COUNTER DESIGN
using VIVADO.

#APPARATUS REQUIRED: VIVADO 2023.2

#PROCEDURE:
STEP:1 Start the Vivado, Select and Name the New project.
STEP:2 Select the device family, device, package and speed.
STEP:3 Select new source in the New Project and select Verilog Module
as the Source type.
STEP:4 Type the File Name and Click Next and then finish button. Type
the code and save it.
STEP:5 Select the Behavioural Simulation in the Source Window and
click the check syntax.
STEP:6 Click the simulation to simulate the program and give the inputs
and verify the outputs as per the truth table.


#SR FLIP FLOP:


















#PROGRAM:
end module SRFF(s, r, clk, rst, q);
input s, r, clk, rst;
output reg q;
always@(posedge clk)
begin
if(rst==1)
q=1'b0;
else
begin
case({s, r})
2'b00:q=q;
2'b01:q=1'b0;
2'b10:q=1'b1;
2'b11:q=1'bx;
endcase
end 
endmodule


#OUTPUT:


























#JK FLIP FLOP:





















#PROGRAM:
module JKFF(j, k, clk, rst, q);
input j, k, clk, rst;
output reg q;
always@(posedge clk)
begin
if(rst==1)
q=1'b0;
else
begin
case({j, k})
2'b00:q=q;
2'b01:q=1'b0;
2'b10:q=1'b1;
2'b11:q=~q;
endcase
end
end
endmodule


#OUTPUT:




























#T FLIP FLOP:




















#PROGRAM:
module TFF(clk, rst, t, q);
input t, clk, rst;
output reg q;
always@(posedge clk)
begin
if(rst==1)
q=1'b0;
else
begin
if(t==0)
q=q;
else
q=~q;
end
end
endmodule


#OUTPUT:




























#D FLIP FLOP:






















#PROGRAM:
module DFF(d, q, clk, rst);
input d, clk, rst;
output reg q;
always@(posedge clk)
begin
if(rst==1)
q=1'b0;
else
q=d;
end
 endmodule

 #OUTPUT:































#RESULT:
 Thus, The Flips Flops Implemented and simulated
successfully. 

