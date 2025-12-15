# JKFLIPFLOP
# JKFLIPFLOP-USING-IF-ELSE
# AIM:

To implement JK flipflop using verilog and validating their functionality using their functional tables

# SOFTWARE REQUIRED:

Quartus prime

# THEORY

JK Flip-Flop

JK flip-flop is the modified version of SR flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of JK flip-flop is shown in the following figure.
<img width="676" height="440" alt="image" src="https://github.com/user-attachments/assets/a63232a6-94b4-400a-a448-f5828f095be7" />
This circuit has two inputs J & K and two outputs Qtt & Qtt’. The operation of JK flip-flop is similar to SR flip-flop. Here, we considered the inputs of SR flip-flop as S = J Qtt’ and R = KQtt in order to utilize the modified SR flip-flop for 4 combinations of inputs. The following table shows the state table of JK flip-flop.

<img width="487" height="370" alt="image" src="https://github.com/user-attachments/assets/3ef33b5b-81dc-4a88-8e2e-69e264c93e5d" />
Here, Qtt & Qt+1t+1 are present state & next state respectively. So, JK flip-flop can be used for one of these four functions such as Hold, Reset, Set & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of JK flip-flop. Present Inputs Present State Next State

<img width="658" height="547" alt="image" src="https://github.com/user-attachments/assets/d6072801-e10b-4c2a-975d-39ae9ed2261f" />
By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. Three variable K-Map for next state, Qt+1t+1 is shown in the following figure.

<img width="745" height="233" alt="image" src="https://github.com/user-attachments/assets/7d1ef1bf-538c-4ad3-9a35-3d367801d9e4" />
The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is Q(t+1)=JQ(t)′+K′Q(t)Q(t+1)=JQ(t)′+K′Q(t)

# Procedure

Define Inputs/Outputs: Inputs: J (Set), K (Reset), c1k (clock); Outputs: q, qbar (~q).
Initialization: Set q = 0 and qbar = 1 at the start of the simulation.
JK Flip-Flop Logic: On posedge c1k, compute q
Complementary Output: Update qbar = ~q to maintain complementarity.
Testbench: Simulate with combinations of J, K, and c1k to verify JK Flip-Flop functionality.
# DEVELOPED BY: BUSHPIKA C
# REG NO:25007434
#PROGRAM
```
module exp7(J,K,c1k,q,qbar);
input J,K,c1k;
output reg q;
output reg qbar;
initial q=0;
initial qbar=1;
always @(posedge c1k)
begin
q=((J&(~q)))|((~K)&q);
qbar=~q;
end
endmodule
```
# RTL LOGIC FOR FLIPFLOPS 
<img width="1920" height="1080" alt="Screenshot 2025-12-15 181658" src="https://github.com/user-attachments/assets/86a9efd1-33e0-4e82-a578-e7affc0f87e0" />

# TIMING DIGRAMS FOR FLIP FLOPS 
<img width="1920" height="1080" alt="Screenshot 2025-12-15 184103" src="https://github.com/user-attachments/assets/fd4e0935-869b-4e99-bb78-55f039c2b81d" />

# RESULTS
Thus the program has been executed successfully.

Thus the JK flipflop is implemented and verified.
