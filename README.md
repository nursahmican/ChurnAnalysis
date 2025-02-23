# Churn Analysis

**Churn Analizinde Makine Öğrenmesi ve Derin Öğrenme Yaklaşımları**

Churn, bir müşteri ya da kullanıcının bir ürünü ya da hizmeti kullanmayı bırakması anlamına gelirken Churn Analizi bir müşterinin veya kullanıcının bir ürünü ya da hizmeti terk etme olasılığını tahmin etmeye yönelik yapılan çalışmalardır. Genellikle CRM (Müşteri İlişkileri Yönetimi) alanında kullanılır. Bu analiz, işletmelerin proaktif bir yaklaşım benimsemelerini sağlamak amacıyla yapılır. Müşterileri kaybetme risklerinin önceden belirlenmesi ve uygun stratejiler geliştirerek müşteri sadakatinin arttırılması planlanır.


Bu proje, müşterilerin hizmeti terk etme (churn) olasılıklarını tahmin etmek için makine öğrenmesi ve derin öğrenme tekniklerinin nasıl kullanılabileceğine dair bir inceleme sunmaktadır. Çalışmada, karar ağaçları gibi temel algoritmalardan yapay sinir ağları gibi daha ileri düzey yöntemlere kadar çeşitli algoritmaların churn tahminindeki rolü ele alınmaktadır.

Makine Öğrenmesi (ML) : Veri setlerinden öğrenmeyi ve tahminler üretmeyi amaçlar. Öznitelik çıkarımı genellikle insan tarafından yapılır, küçük-orta büyüklükteki veri setleriyle çalışabilir, belirli kurallar ve modellerle işler.

Derin Öğrenme (DL) : Büyük miktarda veriyi çok katmanlı yapay sinir ağlarını kullanarak analiz eder. Öznitelikleri kendisi öğrenebilir, ML algoritmalarına göre daha fazla işlem gücü gerektirir ve daha uzun sürede eğitilir.

**Proje İçeriği**
**Makine Öğrenmesi Yöntemleri:** Karar ağaçları, K-NN ve SVM gibi temel algoritmaların ve BaggingClassifier, XGBoost, Random Forest gibi kollektif algoritmaların churn tahminindeki kullanımı.

**Derin Öğrenme Yöntemleri:** Yapay sinir ağları (ANN) ve TabNet gibi daha gelişmiş derin öğrenme algoritmalarının churn tahmininde nasıl etkili olduğu.

**Özellik Mühendisliği:** Churn tahmininde kullanılan verilerin işlenmesi ve model başarısını artırmak için özellik mühendisliğinin önemi.

**Model Değerlendirme:** Çeşitli makine öğrenmesi ve derin öğrenme modellerinin karşılaştırılması ve performans değerlendirmesi.

**Çalışma Sonuçları:** Hangi algoritmaların churn tahmininde daha iyi sonuçlar verdiği ve hangi parametrelerin model başarısını etkilediği üzerine bir analiz.

**Kullanılan Algoritmalar:**

**ML ALGORİTMALARI**

**Temel (Base) Algoritmalar:**

**K-NN (K-Nearest Neighbors):** Bu algoritma, bir veri noktasının hangi sınıfa ait olduğunu tahmin etmek için çevresindeki en yakın K komşusuna bakar. Komşular genellikle Euclidean mesafesi gibi ölçütlere göre belirlenir. Örneğin, bir ürünü diğerlerinden ayırmak istiyorsak, o ürünü en yakın K ürünü ile karşılaştırarak hangi grupta olduğunu tahmin ederiz. K sayısı küçük olduğunda model daha duyarlı , K büyüdükçe model daha genel hale gelir.

**Karar Ağaçları (Decision Tree):** Karar ağacı, verileri bir ağaç yapısına benzer şekilde sınıflandırır. Her dal, veriyi farklı özelliklere göre ayırır, sonunda ise sınıf etiketlerini buluruz. Mesela, bir müşteri profilini çeşitli özelliklere göre (yaş, gelir, vs.) ayırarak hangi gruba ait olduğunu tahmin edebiliriz.

**SVM (Support Vector Machine):** Bu algoritma, verileri mümkün olan en geniş marginle ayıran bir sınır (hiper düzlem) bulmaya çalışır. SVM, hem doğrusal hem de doğrusal olmayan verileri ayırmak için kullanılabilir. Bu sayede, karmaşık sınırları bile öğrenebiliriz.

**Kollektif (Ensemble) Algoritmalar:**

**BaggingClassifier:** Bu yöntem, veriyi farklı parçalara ayırıp her bir parçada ayrı bir model eğitir. Sonra bunların sonuçlarını birleştirerek daha doğru bir tahmin yapar. Özellikle karar ağaçları gibi hataya eğilimli modeller için faydalıdır.

**XGBoost:** Bu yöntem, bir modelin hatalarını düzeltmeye yönelik olarak bir dizi model oluşturur. Her yeni model, öncekinin yaptığı hataları düzeltir. Bu sayede genellikle çok güçlü ve doğru tahminler yapar.

**Random Forest:** Random Forest, birden fazla karar ağacının bir arada çalıştığı bir algoritmadır. Her ağaç, rastgele seçilen veri parçaları ve özelliklerle eğitilir. Sonuçta, birden fazla ağacın tahminlerini birleştirerek daha doğru sonuçlar elde edilir. Bu da genelleme yeteneğini artırır ve aşırı öğrenme (overfitting) riskini azaltır.

**DL ALGORİTMALARI**

**Yapay Sinir Ağı (ANN) :** Yapay Sinir Ağı, insan beynine benzer şekilde çalışan bir sistemdir. Beyindeki nöronlar gibi, yapay sinir ağlarında da “nöron” denilen birimler bulunur. Bu nöronlar birbirine bağlanır ve her biri, aldığı bilgiyi işler. Bilgiler, ağın farklı katmanlarından geçerek işlenir ve sonuç çıkar.

**TabNet :** Hem sayısal hem de kategorik veriler üzerinde güçlü performans gösteren, dikkat mekanizmalarını (attention) ve ağaç tabanlı yöntemleri birleştiren bir modeldir. Her adımda dikkat mekanizmaları kullanarak sadece önemli verilere dikkat eder ve hangi bilgileri ne zaman kullanacağına karar verir. Bu sayede hem daha doğru sonuçlar sağlar hem de işlemleri daha hızlı yapar. Yani, veriyi en iyi şekilde analiz etmek için bir tür akıllı seçim yapma yöntemine dayanır.

**Model Değerlendirme**

Model performansı, aşağıdaki metrikler kullanılarak değerlendirilmiştir:

**Precision (Doğruluk):** Precision, modelin pozitif tahminlerde ne kadar doğru olduğunu gösterir. Yani, modelinizin “bu kişi hastadır” dediğinde gerçekten hasta olma olasılığı ne kadar yüksek? Yüksek precision, yanlış pozitif (yani hasta olmayan birini hasta olarak tahmin etmek) oranının düşük olduğunu gösterir.

**Recall (Duyarlılık):** Recall, modelinizin gerçek pozitifleri (gerçekten hasta olan kişileri) ne kadar iyi tahmin ettiğini gösterir. Yüksek recall, modelin hastaları doğru tahmin etme oranının yüksek olduğunu gösterir.

**F1-Score:** F1-Score, precision ve recall arasında bir denge kurar. Bu, modelin hem doğru tahmin yapma (precision) hem de hasta olanları bulma (recall) becerisini ölçer. Düşük F1-Score, modelin birine (precision veya recall) daha çok odaklanıp diğerini ihmal ettiğini gösterebilir.

**Accuracy (Doğruluk):** Accuracy, modelinizin toplamda ne kadar doğru tahmin yaptığını gösterir. Ancak, çok dengesiz verilerde (örneğin, çoğunluk hasta olmayan) accuracy yanıltıcı olabilir. Yüksek accuracy, modelin genel olarak iyi tahminler yaptığını gösterir.

**ROC AUC (ROC Eğrisinin Altındaki Alan):** ROC AUC, modelinizin tüm sınıflandırma eşiklerinde (yani “hasta” ya da “hasta değil” kararını verdiği her noktada) nasıl performans gösterdiğini ölçer. Yüksek AUC, modelin doğru tahminler yapma oranının yüksek olduğunu ve pozitif ile negatif örnekleri iyi ayırt ettiğini gösterir. Bu, modelinizin “hasta” ve “hasta değil” gibi sınıfları ne kadar iyi ayırt ettiğini gösterir.

**Çalışma Sonuçları**

En iyi performans gösterenler: SVM, XGBoost ve TabNet, doğruluk ve ROC-AUC açısından öne çıkıyor, SVM en yüksek ROC-AUC’ye sahip.

ANN ve Random Forest de güçlü modeller, ancak recall ve AUC puanları biraz daha düşük.

Bagging ve Decision Tree iyi performans gösteriyor ancak precision ve AUC açısından en yüksek modellerin gerisinde kalıyor.

K-NN , hem doğruluk hem de AUC açısından genel olarak en zayıf model.

