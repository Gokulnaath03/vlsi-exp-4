# EXP 4:

# SIMULATE AND SYNTHESIS SR,JK,T,D-FLIPFLOP,COUNTER DESIGN USING VIVADO.

## AIM:
To simulate and synthesis SR, JK, T, D - FLIPFLOP, COUNTER DESIGN
using VIVADO.

## APPARATUS REQUIRED: VIVADO 2023.2

## PROCEDURE:
STEP:1 Start the Vivado, Select and Name the New project.<br>
STEP:2 Select the device family, device, package and speed.<br>
STEP:3 Select new source in the New Project and select Verilog Module
as the Source type.<br>
STEP:4 Type the File Name and Click Next and then finish button. Type
the code and save it.<br>
STEP:5 Select the Behavioural Simulation in the Source Window and
click the check syntax.<br>
STEP:6 Click the simulation to simulate the program and give the inputs
and verify the outputs as per the truth table.


## SR FLIP FLOP:

![image](https://github.com/Gokulnaath03/vlsi-exp-4/assets/167178811/9640e914-da6d-4a80-9206-7f88da588964)



## PROGRAM:
end module SRFF(s, r, clk, rst, q);<br>
input s, r, clk, rst;<br>
output reg q;<br>
always@(posedge clk)<br>
begin<br>
if(rst==1)<br>
q=1'b0;<br>
else<br>
begin<br>
case({s, r})<br>
2'b00:q=q;<br>
2'b01:q=1'b0;<br>
2'b10:q=1'b1;<br>
2'b11:q=1'bx;<br>
endcase<br>
end <br>
endmodule


## OUTPUT:

![image](https://github.com/Gokulnaath03/vlsi-exp-4/assets/167178811/527c46d3-cf4a-439f-97cc-03502880e411)


## JK FLIP FLOP:

![image](https://github.com/Gokulnaath03/vlsi-exp-4/assets/167178811/ad27b7ee-b953-414c-a860-6fc83a58bf29)


## PROGRAM:
module JKFF(j, k, clk, rst, q);<br>
input j, k, clk, rst;<br>
output reg q;<br>
always@(posedge clk)<br>
begin<br>
if(rst==1)<br>
q=1'b0;<br>
else<br>
begin<br>
case({j, k})<br>
2'b00:q=q;<br>
2'b01:q=1'b0;<br>
2'b10:q=1'b1;<br>
2'b11:q=~q;<br>
endcase<br>
end<br>
end<br>
endmodule


## OUTPUT:

![image](https://github.com/Gokulnaath03/vlsi-exp-4/assets/167178811/f356b3d7-2ab4-4bac-81ae-33a52efc5fd3)



## T FLIP FLOP:

![image](https://github.com/Gokulnaath03/vlsi-exp-4/assets/167178811/dac32ff4-ed21-4c74-8d5f-a9d260d5f5e5)


## PROGRAM:
module TFF(clk, rst, t, q);<br>
input t, clk, rst;<br>
output reg q;<br>
always@(posedge clk)<br>
begin<br>
if(rst==1)<br>
q=1'b0;<br>
else<br>
begin<br>
if(t==0)<br>
q=q;<br>
else<br>
q=~q;<br>
end<br>
end<br>
endmodule


## OUTPUT:

![image](https://github.com/Gokulnaath03/vlsi-exp-4/assets/167178811/415600c8-e0ce-4a0c-89ec-d8b453463909)


## D FLIP FLOP:


![image](https://github.com/Gokulnaath03/vlsi-exp-4/assets/167178811/e7feae95-5eaa-4ba0-98b9-69d0ab8edfc3)


## PROGRAM:
module DFF(d, q, clk, rst);<br>
input d, clk, rst;<br>
output reg q;<br>
always@(posedge clk)<br>
begin<br>
if(rst==1)<br>
q=1'b0;<br>
else<br>
q=d;<br>
end<br>
 endmodule
 

 ## OUTPUT:

![image](https://github.com/Gokulnaath03/vlsi-exp-4/assets/167178811/2e577452-ad66-4ad2-8f55-e5d8e6b65198)

## MOD 10 COUNTER

![image](https://github.com/Gokulnaath03/vlsi-exp-4/assets/167178811/226df16f-07b1-423c-8ff6-c1859ec08242)

## PROGRAM:

module mod_10(clk,rst,out);<br>
input clk,rst;<br>
output reg[3:0]out;<br>
always@(posedge clk)<br>
begin<br>
if(rst==1|out==9)<br>
out=4'b0;<br>
else<br>
out=out+1;<br>
end<br>
endmodule


## OUPUT:

![image](https://github.com/Gokulnaath03/vlsi-exp-4/assets/167178811/49ae3a7d-1a45-4e02-b9f5-0387ba60ad0e)


## UP-DOWN-COUNTER:


![image](https://github.com/Gokulnaath03/vlsi-exp-4/assets/167178811/c1b423d8-1cb2-407d-ae1e-8751469a56b7)


## PROGRAM:


module updown_counter(clk,rst,ud,out);<br>
input clk,rst,ud;<br>
output reg[3:0]out;<br>
always@(posedge clk) begin if(rst==1) out=4'b0; <br>
else if (ud==1) out=out+1;<br>
else<br>
if(ud==0) out=out-1;<br>
end endmodule

## OUTPUT:


![image](https://github.com/Gokulnaath03/vlsi-exp-4/assets/167178811/9d4eeb22-682e-42df-9376-b7135f36ed23)


## RESULT:

 The simulate and synthesis SR, JK, T, D - FLIPFLOP, COUNTER DESIGN using VIVA.
