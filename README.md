## NAME: PRADEEP V
## REG NO: 212223240119

# BOOLEAN_FUNCTION_MINIMIZATION

**AIM:**

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy

**Equipment Required:**

Hardware – PCs, Cyclone II , USB flasher

**Software – Quartus prime**

**Theory**

**Logic Diagram**

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

/* Program to implement the given logic function and to verify its operations in quartus using Verilog programming. 
```
module ex01san(a,b,c,d,w,x,y,z,f1,f2);
input a,b,c,d,w,x,y,z;
output f1,f2;
wire adash,bdash,cdash,ddash,ydash,p,q,r,s,t,u;
not(adash,a);
not(bdash,b);
not(cdash,c);
not(ddash,d);
not(ydash,y);
and(p,bdash,ddash);
and(q,adash,b,d);
and(r,a,b,cdash);
or(f1,p,q,r);

and g1(s,ydash,z);
and g2(t,x,y);
and g3(u,w,z);
or g4(f2,s,t,u);
endmodule




```
Developed by: RegisterNumber:*/


**RTL realization**
![316319712-dee09fd9-6b44-40ef-afbf-d6ab2e627d53](https://github.com/velupradeep/BOOLEAN_FUNCTION_MINIMIZATION/assets/150329341/4f6f4a0d-460f-4003-a885-e35887bc9bf6)

**Truth Table**
![316319842-96ebeb42-3093-489e-b6ab-688e9a11d038](https://github.com/velupradeep/BOOLEAN_FUNCTION_MINIMIZATION/assets/150329341/bed21d2e-b4c9-4d03-b535-ae5b553a7b35)


**Timing Diagram**
![316319778-ce67084d-5d29-4a77-b17f-48f38be24498](https://github.com/velupradeep/BOOLEAN_FUNCTION_MINIMIZATION/assets/150329341/5bbf59b4-4c78-4263-89ef-c73c084f324e)



**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

