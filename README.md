# RC Circuit
We will analyze resistor-capacitor (RC) circuits in this page.
## Step Response of RC Circuit
Mathematical model of the capacitor is given by

<img src="equations/capacitor equation.JPG" alt="capacitor equation" height="45"/>

If we take the integral of both sides of the equation from k=t<sub>0</sub> to k=t, then we obtain the solution

<img src="equations/capacitor equation solution.JPG" alt="capacitor equation solution" height="60"/>

Here k is known as the dummy variable that serves as a temporary variable name as now t becomes a certain moment in time. Now, let's analyze the step response<sup>1</sup> of RC circuit shown in Fig. 1.

<img src="figures/RC circuit step response.jpg" alt="RC circuit with power supply" height="300"/>

*Figure 1:* RC circuit with an external power supply.

*Şekil 1*'de gösterilen devrede ok yönünde dolaşırken Kirchoff'un Gerilimler Yasasını (KGY) uygularsak aşağıdaki eşitliği elde ederiz.

-V<sub>cc</sub> + Ri(t) + V<sub>C</sub>(t) = 0

Devremizde kapasitörün üzerinden geçen akım i<sub>C</sub>(t), aynı yönde tamamlandıklarından dolayı devrede dolaşan akım i(t)'ye eşit (i.e., i<sub>C</sub>(t)=i(t)). Bunu göz önünde bulundurarak yukarıda elde ettiğimiz ilk denklem olan kapasitörün matematiksel modelini KGY ile elde ettiğimiz denklemde yerine koyacak olursak

<img src="eşitlikler/KGY_sonucu_0.JPG" alt="KGY sonucu elde edilen eşitlik" height="55"/>

birinci dereceden adi diferansiyel denklemini elde ederiz. Bu denklemi düzenlersek

<img src="eşitlikler/KGY_sonucu_1.JPG" alt="KGY sonucu elde edilen eşitliğin düzenlenmiş hali" height="55"/>

haline gelir. Biraz daha manipüle edersek

<img src="eşitlikler/KGY_sonucu_2.JPG" alt="KGY sonucu elde edilen eşitliğin düzenlenmiş ve manipüle edilmiş hali" height="55"/>

denklemini elde ederiz. Eşitliğin her iki tarafının integralini k=t<sub>0</sub>'dan k=t anına kadar alalım.

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

<img src="şekiller/RC_devresi_basamak_cevabı_grafik.png" alt="Rc devresinin basamak cevabının değişik R ve C değerlerine göre çizdirilmiş hali" height="300"/>

*Şekil 2:* RC devresinin basamak cevabının V<sub>cc</sub> = 5V, V<sub>C</sub>(0) = 0V ve değişik R ve C değerlerine göre grafiği<sup>3</sup>.

<img src="şekiller/RC_devresi_dogal_cevabı_grafik.png" alt="RC devresinin basamak cevabının değişik R ve C değerlerine göre çizdirilmiş hali" height="300"/>

*Şekil 3:* RC devresinin doğal cevabının V<sub>C</sub>(0) = 5V ve değişik R ve C değerlerine göre grafiği<sup>4</sup>. Anahtarlama ile *Şekil 2*'de kaldığı durumdan devam edilmiştir.

<img src="şekiller/RL devresi basamak cevabı.jpg" alt="RL devresi." height="300"/>

*Şekil 4:* RL devresi.

<img src="şekiller/RL_devresi_basamak_cevabı_grafik.png" alt="RL devresinin basamak cevabının değişik R ve L değerlerine göre çizdirilmiş hali" height="300"/>

*Şekil 5:* RL devresinin basamak cevabının V<sub>cc</sub> = 5V, i<sub>L</sub>(0) = 0A ve değişik R ve L değerlerine göre grafiği<sup>5</sup>.

<img src="şekiller/RL_devresi_dogal_cevabı_grafik.png" alt="RL devresinin basamak cevabının değişik R ve L değerlerine göre çizdirilmiş hali" height="300"/>

*Şekil 6:* RL devresinin doğal cevabının i<sub>L</sub>(0) *Şekil 5*'de hangi değere oturduysa kaldığı yerden ve değişik R ve L değerlerine göre grafiği<sup>6</sup>.
## Dipnotlar
<sup>1</sup> İng. Dummy variable.</br>
<sup>2</sup> İng. Step response. Basamak cevabı [1]'de geçen bir kavramdır. Aynı kaynağı referans kullanan [2], bu cevabı zorlanmış cevap diye isimlendirerek yaklaşımı daha genelleştirmiştir (i.e., güç kaynağından devreye etki eden sinyalin sadece sabit bir DC gerilim olma şartı yok). Biz burada [1]'de geçen haliyle kullanmayı uygun gördük.</br> 
<sup>3</sup> Bu grafik **MATLAB**'da çizdirilmiştir. Siz de **MATLAB**'da çizdirmek için *kodlar* dizinindeki *RC_devresi_zorlanmis_cevap.m* programını koşturun.</br>
<sup>4</sup> Bu grafik  **MATLAB** ile çizdirilmiştir. Siz de **MATLAB** ile çizdirmek için *kodlar* dizinindeki *RC_devresi_dogal_cevap.m* programını koşturun.</br>
<sup>5</sup> Bu grafik **MATLAB**'da çizdirilmiştir. Siz de **MATLAB**'da çizdirmek için *kodlar* dizinindeki *RL_devresi_zorlanmis_cevap.m* programını koşturun.</br>
<sup>6</sup> Bu grafik  **MATLAB** ile çizdirilmiştir. Siz de **MATLAB** ile çizdirmek için *kodlar* dizinindeki *RL_devresi_dogal_cevap.m* programını koşturun.
## Referanslar
[1] J. W. Nilsson, S. A. Riedel, Electric Circuits, 10. Baskı, Prentice Hall, Upper Saddle River, New Jersey, 2014.</br>
[2] M. Ö. Efe, Devre Analizi-I, 3. Baskı, Seçkin Yayıncılık, Ankara, 2016.