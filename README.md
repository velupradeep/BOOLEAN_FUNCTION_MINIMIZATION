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

module Boolean_min(a,b,c,d,w,x,y,z,f1,f2);
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
Developed by:Pradeep V RegisterNumber:212223240119*/


**RTL realization**
![316248910-f352081d-c087-4f9e-bfbc-1f9953f905cf](https://github.com/velupradeep/BOOLEAN_FUNCTION_MINIMIZATION/assets/150329341/bb1c758d-2359-4b24-821b-f66eae4d1e0d)


**Truth Table**
![316248955-9b8ac838-42f6-4e16-af60-36b3d664d4db](https://github.com/velupradeep/BOOLEAN_FUNCTION_MINIMIZATION/assets/150329341/c1016fce-b517-4d0d-88a4-e3dc9e63c20f)




**Timing Diagram**
![316248973-b497fc93-c6c6-4981-8462-91a226b19e88](https://github.com/velupradeep/BOOLEAN_FUNCTION_MINIMIZATION/assets/150329341/c4bbb22f-a999-47c4-af59-fde614dcc881)




**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

