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

Eşitliğin her iki tarafının integralini k=t<sub>0</sub>'dan k=t anına kadar alalım.

<img src="eşitlikler/KGY_sonucu_3.JPG" alt="KGY sonucu elde edilen eşitliğin düzenlenmiş ve manipüle edilmiş hali" height="55"/>

Dikkat edilirse soldaki ifade doğal logaritma ile alakalı bir integral. İntegralleri alarak ilerleyecek olursak

<img src="eşitlikler/KGY_sonucu_4.JPG" alt="KGY sonucu elde edilen eşitliğin düzenlenmiş ve manipüle edilmiş hali" height="60"/>

<img src="eşitlikler/KGY_sonucu_5.JPG" alt="KGY sonucu elde edilen eşitliğin düzenlenmiş ve manipüle edilmiş hali" height="50"/>

soldaki doğal logaritma içeren ifadelerle yapılan çıkarma işlemi, aşağıdaki halini alırken

<img src="eşitlikler/KGY_sonucu_6.JPG" alt="KGY sonucu elde edilen eşitliğin düzenlenmiş ve manipüle edilmiş hali" height="55"/>

her iki tarafı e ≈ 2.71'in üssü olarak yazarsak (birşey değişmeyeği gibi sol taraftaki doğal logaritma ln ifadesinden kurtulmuş olacağız)

<img src="eşitlikler/KGY_sonucu_7.JPG" alt="KGY sonucu elde edilen eşitliğin düzenlenmiş ve manipüle edilmiş hali" height="55"/>

en sonunda aşağıdaki çözümü elde ederiz.

<img src="eşitlikler/KGY_sonucu_8.JPG" alt="KGY sonucu elde edilen eşitliğin düzenlenmiş ve manipüle edilmiş hali" height="50"/>

Genelde t<sub>0</sub>=0 olarak kabul ettiğimizden elde ettiğimiz çözüm aşağıdaki son halini alır.

<img src="eşitlikler/KGY_sonucu_9.JPG" alt="KGY sonucu elde edilen eşitliğin düzenlenmiş ve manipüle edilmiş hali" height="50"/>

Aşağıda grafiğini çizdireceğimiz kapasitörün üzerindeki voltajın matematiksel ifadesi olan bu ifade hakkında hemen kabaca (yani ekstrem değerlere bakarak) düşünecek olursak t=0 anında V<sub>C</sub>(0)=V<sub>C</sub>(0) ve t→∞ durumunda V<sub>C</sub>(∞)=V<sub>cc</sub> olduğunu görebiliriz. Ayrıca zaman sabitimiz olan τ = RC arttıkça V<sub>C</sub>(t)'nin V<sub>cc</sub>'ye ulaşması yavaşlarken τ azalırken V<sub>C</sub>(t)'nin V<sub>cc</sub>'ye ulaşması hızlanır.

Şimdi elde ettiğimiz çözümün değişik R ve C değerlerine göre grafiklerini çizdirelim ve zaman sabitinin kapasitörün voltajına olan etkisini görelim.

<img src="figures/step response of RC circuit.png" alt="plot of RC circuit step response for various R and C values" height="300"/>

*Figure 2:* Step response of the RC circuit when V<sub>cc</sub> = 5V, V<sub>C</sub>(0) = 0V while R and C takes various values.<sup>2</sup>.

<img src="figures/step response of RC circuit python.png" alt="plot of RC circuit step response for various R and C values" height="300"/>

*Figure 3:* RC devresinin basamak cevabının V<sub>cc</sub> = 5V, V<sub>C</sub>(0) = 0V ve değişik R ve C değerlerine göre grafiği<sup>3</sup>.


## Footnotes
<sup>1</sup> İng. Step response. Basamak cevabı [1]'de geçen bir kavramdır. Aynı kaynağı referans kullanan [2], bu cevabı zorlanmış cevap diye isimlendirerek yaklaşımı daha genelleştirmiştir (i.e., güç kaynağından devreye etki eden sinyalin sadece sabit bir DC gerilim olma şartı yok). Biz burada [1]'de geçen haliyle kullanmayı uygun gördük.</br> 
<sup>2</sup> Bu grafik **MATLAB**'da çizdirilmiştir. Siz de **MATLAB**'da çizdirmek için *kodlar* dizinindeki *RC_devresi_zorlanmis_cevap.m* programını koşturun.</br>
<sup>3</sup> Bu grafik  **MATLAB** ile çizdirilmiştir. Siz de **MATLAB** ile çizdirmek için *kodlar* dizinindeki *RC_devresi_dogal_cevap.m* programını koşturun.</br>
## References
[1] J. W. Nilsson, S. A. Riedel, Electric Circuits, 10. Baskı, Prentice Hall, Upper Saddle River, New Jersey, 2014.</br>
[2] M. Ö. Efe, Devre Analizi-I, 3. Baskı, Seçkin Yayıncılık, Ankara, 2016.
