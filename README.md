## NAME:SHYAM SUJIN U
## REG NO.212223040201

# EXP 07-JKFLIPFLOP-USING-IF-ELSE

**AIM:** 

To implement  JK flipflop using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**JK Flip-Flop**

JK flip-flop is the modified version of SR flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of JK flip-flop is shown in the following figure.

![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/a649c30b-232b-4558-b188-fd6c09845180)


This circuit has two inputs J & K and two outputs Qtt & Qtt’. The operation of JK flip-flop is similar to SR flip-flop. Here, we considered the inputs of SR flip-flop as S = J Qtt’ and R = KQtt in order to utilize the modified SR flip-flop for 4 combinations of inputs. The following table shows the state table of JK flip-flop.

![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/c4360742-e8a8-4937-b089-c46c0433f9a3)

 
Here, Qtt & Qt+1t+1 are present state & next state respectively. So, JK flip-flop can be used for one of these four functions such as Hold, Reset, Set & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of JK flip-flop. Present Inputs Present State Next State
 
![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/6c275261-a6d5-4c37-a3a7-1e88ca11c4cd)

By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. Three variable K-Map for next state, Qt+1t+1 is shown in the following figure.
 
![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/5174f41b-0ce0-4329-a372-6d1943ea6673)

The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is Q(t+1)=JQ(t)′+K′Q(t)Q(t+1)=JQ(t)′+K′Q(t)

**Procedure**
STEP 1:Type the program in Quartus software.
STEP 2:Compile and run the program.
STEP 3:Generate the RTL schematic and save the logic diagram.
STEP 4:Create nodes for inputs and outputs to generate the timing diagram.
STEP 5:For different input combinations generate the timing diagram
**PROGRAM**
```
/*Program for logic gates and verify its truth table in quartus using Verilog programming.

module jkflipflop(q, qb,j,k,clock,reset);
    input j,k,clock,reset;
    output reg q, qb;
	 
always @ (posedge (clock))

    begin 
        if (!reset)
            begin
               q <= q;
               qb <=qb;
            end   
        
else
   begin
	   if(j==0 && k==0)
		   begin
			q<=q;
			qb<=qb;
			end
		else if(j!=k)
		   begin
			q<=j;
			qb<=k;
			end
		else if(j==1 && k==1)
		    begin
			 q<=~q;
			 qb<=~qb;
			 end
	end
end	
endmodule

Developed by:SHYAM SUJIN U
RegisterNumber:212223040201
```
*/

**RTL LOGIC FOR FLIPFLOPS**
![image](https://github.com/Shyamsujin/JKFLIPFLOP-USING-IF-ELSE/assets/144870449/404fdab3-ee86-4c5b-994c-f1135f988bb5)

**TIMING DIGRAMS FOR FLIP FLOPS**
![image](https://github.com/Shyamsujin/JKFLIPFLOP-USING-IF-ELSE/assets/144870449/cc3c8844-cfc4-474d-9413-f7c9c9f0768c)

**Result:**
The output of JKFLIPFLOP-USING-IF-ELSE has been executed successfully.

