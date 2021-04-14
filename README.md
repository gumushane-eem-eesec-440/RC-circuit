# RC Circuit
We will analyze resistor-capacitor (RC) circuits in this page.
## Step Response of RC Circuit
Mathematical model of the capacitor is given by

<img src="equations/capacitor equation.JPG" alt="capacitor equation" height="45"/>

If we take the integral of both sides of the equation from k=t<sub>0</sub> to k=t, then we obtain the solution

<img src="equations/capacitor equation solution.JPG" alt="capacitor equation solution" height="60"/>

Here k is known as the dummy variable that serves as a temporary variable name as now t becomes a certain moment in time. Now, let's analyze the step response<sup>1</sup> of RC circuit shown in Fig. 1.

<img src="figures/RC circuit with Vcc.jpg" alt="RC circuit with power supply" height="300"/>

*Figure 1:* RC circuit connected to a DC power supply.

When we apply Kirchoff's Voltage Law (KVL) on the RC circuit shown in *Fig. 1*, we get

-V<sub>cc</sub> + Ri(t) + V<sub>C</sub>(t) = 0

The current that passes through the capacitor i<sub>C</sub>(t) is the same as the current i(t) that flows in the circuit (i.e., i<sub>C</sub>(t)=i(t)) as can be seen in *Fig. 1*. Considering this fact while substituting the capacitor's mathematical model in the equation obtained by KVL yields

<img src="equations/KGY_result_0.JPG" alt="equation obtained after applying KVL on RC circuit 0" height="55"/>

the first order differential equation. If we manipulate the equation, it becomes

<img src="equations/KGY_result_1.JPG" alt="equation obtained after applying KVL on RC circuit 1" height="55"/>

More manipulations result in

<img src="equations/KGY_result_2.JPG" alt="equation obtained after applying KVL on RC circuit 2" height="55"/>

Now, let's take the integral of both sides from k=t<sub>0</sub> to k=t.

<img src="equations/KGY_result_3.JPG" alt="equation obtained after applying KVL on RC circuit 3" height="55"/>

Notice that the statement at the left is related to natural logarithm. Let's continue step by step

<img src="equations/KGY_result_4.JPG" alt="equation obtained after applying KVL on RC circuit 4" height="60"/>

<img src="equations/KGY_result_5.JPG" alt="equation obtained after applying KVL on RC circuit 5" height="50"/>

The expression with natural logarithm at the left becomes

<img src="equations/KGY_result_6.JPG" alt="equation obtained after applying KVL on RC circuit 6" height="55"/>

and now if we write both sides as exponents of e ≈ 2.71 (nothing is going to change while we eliminate the ln from the left side)

<img src="equations/KGY_result_7.JPG" alt="equation obtained after applying KVL on RC circuit 7" height="55"/>

eventually we obtain the equation

<img src="equations/KGY_result_8.JPG" alt="equation obtained after applying KVL on RC circuit 8" height="50"/>

In general, we assume t<sub>0</sub>=0 that updates the equation above as

<img src="equations/KGY_result_9.JPG" alt="equation obtained after applying KVL on RC circuit 9" height="50"/>

We will plot the graph of this final equation but before that, let's think roughly on how the voltage across the capacitor would behave by focusing on extreme values: At t=0 moment, V<sub>C</sub>(0)=V<sub>C</sub>(0) and while t→∞, V<sub>C</sub>(∞)=V<sub>cc</sub>. Also as the time constant τ := RC increases, V<sub>C</sub>(t) reaches V<sub>cc</sub> slower while lower values of τ result in V<sub>C</sub>(t) to converge to V<sub>cc</sub> faster.

Now, let's illustrate the solution for various values of R ve C and see the effect of the time constant on the capacitor voltage.

<img src="figures/step response of RC circuit.png" alt="plot of RC circuit step response for various R and C values" height="300"/>

*Figure 2:* Step response of the RC circuit for V<sub>cc</sub> = 5V, V<sub>C</sub>(0) = 0V and various R and C values.<sup>2</sup>.

<img src="figures/step response of RC circuit python.png" alt="plot of RC circuit step response for various R and C values" height="300"/>

*Figure 3:* Step response of the RC circuit for V<sub>cc</sub> = 5V, V<sub>C</sub>(0) = 0V and various R and C values.<sup>3</sup>.
## Footnotes
<sup>1</sup> The response is called as the step response in [1] as we assume that at t=0, a DC power supply is connected to the circuit. If power supply becomes an AC source, then it is more reasonable to refer to the response as the forced response (as [2] does), which is a more general name.</br> 
<sup>2</sup> This graph is plotted in **MATLAB**. To obtain the same plot, run *RC_circuit_step_response.m* script in the [codes](https://github.com/gumushane-eem-eesec-440/RC-circuit/codes) subdirectory at this page.</br>
<sup>3</sup> This graph is plotted with **Python** in **Google COLAB** environment. To obtain the same plot, run *RC_circuit.ipynb* file in the *codes* subdirectory at this page.</br>
## References
[1] J. W. Nilsson, S. A. Riedel, Electric Circuits, 10. Baskı, Prentice Hall, Upper Saddle River, New Jersey, 2014.</br>
[2] M. Ö. Efe, Devre Analizi-I, 3. Baskı, Seçkin Yayıncılık, Ankara, 2016.
