### Ex. No. 6
#### Date: 19.5.23
# Implementation of 4 bit synchronous counters using Verilog HDL
## Aim:
To design and implement the following synchronous counters using Verilog HDL.
1.	UP counter
2.	DOWN counter
## Components Required:
1.	Laptop with Quartus software and modelsim software.
## Theory:
A Synchronous counter is the counter in which the clock input with all the flip-flops uses the same source and produces the output at the same time.
## UP Counter
### State table
![image](https://github.com/rvinifa/Counter/assets/133735746/ede78598-89fd-4aeb-9d82-329e45d05f2a)

### K-map Simplification

   ![image](https://github.com/rvinifa/Counter/assets/133735746/21554263-611b-44a2-8f78-7b2220ef5a05)
   
### Logic Diagram
![image](https://github.com/rvinifa/Counter/assets/133735746/2ab715d3-f6d5-4cf6-8fda-8fa666518c0b)



## DOWN Counter
### State Table
 ![image](https://github.com/rvinifa/Counter/assets/133735746/5be9585c-11aa-47c3-beaf-0dca916750f2)

### K-map simplification
 ![image](https://github.com/rvinifa/Counter/assets/133735746/dde7bc60-3a4f-4fb7-811d-f420cb74bdef)

### Logic Diagram
 ![image](https://github.com/rvinifa/Counter/assets/133735746/64e2d7b7-1646-4ca7-bc6c-c7c10881223c)

## Procedure:
1.	Type the program in Quartus software.
2.	Compile and run the program.
3.	Generate the RTL schematic and save the logic diagram.
4.	Create nodes for inputs and outputs to generate the timing diagram.
5.	For different input combinations, generate the timing diagram.


## Program:
```
Developed By: Mirudhula D
Register No.: 212221230060
```
## UP COUNTER:
```
module exp6a(clk,q1,q2,q3,q4);
input clk;
output reg q1,q2,q3,q4;
always @(posedge clk)
begin
q4=(q1&q2&q3)^q4;
q3=(q1&q2)^q3;
q2=q1^q2;
q1=1^q1;
end
endmodule
```

## DOWN COUNTER:
```
module exp6b(clk,q1,q2,q3,q4);
input clk;
output reg q1,q2,q3,q4;
always @(posedge clk)
begin
q4=((~q3)&(~q2)&(~q1))^q4;
q3=((~q2)&(~q1))^q3;
q2=(~q1)^q2;
q1=1^q1;
end
endmodule
```
## RTL Schematic:
## UP COUNTER:

![image](https://github.com/MIRUDHULA-DHANARAJ/Counter/assets/94828147/15ec39cf-2bf0-4694-8a88-dd4b35d9b91f)

## DOWN COUNTER:

![image](https://github.com/MIRUDHULA-DHANARAJ/Counter/assets/94828147/1a4d507a-8ba5-438b-b050-0418f4700281)

## Timing Diagram:
## UP COUNTER:

![image](https://github.com/MIRUDHULA-DHANARAJ/Counter/assets/94828147/1b88735c-990f-456b-9325-7a71a1fb3dac)


## DOWN COUNTER:

![image](https://github.com/MIRUDHULA-DHANARAJ/Counter/assets/94828147/e3a3f230-346f-49cb-b5d0-2382a3a1835c)



## Result:
Thus the Synchronous UP and DOWN counters using T flipflops are implemented and the state tables are verified.

