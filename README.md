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

![image](https://github.com/Gokulnaath03/vlsi-exp-4/assets/167178811/9640e914-da6d-4a80-9206-7f88da588964)



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

![image](https://github.com/Gokulnaath03/vlsi-exp-4/assets/167178811/527c46d3-cf4a-439f-97cc-03502880e411)


#JK FLIP FLOP:

![image](https://github.com/Gokulnaath03/vlsi-exp-4/assets/167178811/ad27b7ee-b953-414c-a860-6fc83a58bf29)


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

![image](https://github.com/Gokulnaath03/vlsi-exp-4/assets/167178811/f356b3d7-2ab4-4bac-81ae-33a52efc5fd3)



#T FLIP FLOP:

![image](https://github.com/Gokulnaath03/vlsi-exp-4/assets/167178811/dac32ff4-ed21-4c74-8d5f-a9d260d5f5e5)


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

![image](https://github.com/Gokulnaath03/vlsi-exp-4/assets/167178811/415600c8-e0ce-4a0c-89ec-d8b453463909)


#D FLIP FLOP:


![image](https://github.com/Gokulnaath03/vlsi-exp-4/assets/167178811/e7feae95-5eaa-4ba0-98b9-69d0ab8edfc3)


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

![image](https://github.com/Gokulnaath03/vlsi-exp-4/assets/167178811/2e577452-ad66-4ad2-8f55-e5d8e6b65198)




#RESULT:
 Thus, The Flips Flops Implemented and simulated
successfully. 

