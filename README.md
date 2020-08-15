# <h1 align=center> BERT ile Sentiment Analizi </h1>

---
<h3 align=center>(BERT: Bidirectional Encoder Representations for Transformers)</h3>

---

### Bilinse iyi olurlar


- Orta düzey Python ve NumPy ve Pandas kütüphanelerine aşina olmak
- PyTorch kullanmaya yatkın olmak
- Derin Öğrenme ve Dil Modellerinin temelleri bilgisi (özellikle BERT) 

## GİRİŞ

### Terminolojiler

- **NPL Görevleri:** İnsanların kullandıkları dillerle ilgili görevleri kapsar. Dil çevirisi, metin sınıflandırma, duygu durumu kestirimi, okuduğunu anlama, isimlendirilmemiş varlıkları tanıma (metindeki kişiyi, şirketi, yeri vb. isimlerin tanınması) 
- **Dil Modelleri:** Bir dizi kelime verildiğinde (Google sorgusu otomatik tamamlama vb.) en olası sonraki kelimeleri (ve olasılıklarını) tahmin edebilen modellerdir. Bu tür modellerin, sıradan bir sonraki kelime tahmini üzerine eğitilmiş olsalar da, bir dizi başka görev için yararlı olduğu bilinmektedir. Klasik dil modelleri kelimelerin soldan sağa akışını tahmin ederken BERT hem önceki hem sonraki -yani bidirectional- bir yaklaşıma sahiptir. Yani geçmiş ve gelecek bilgilerinden faydalanmaktadır.
- **Sıfır / Bir / Az Shot öğrenme:** Modelin, o görev için sıfır / bir / birkaç örnek görerek yeni bir görevi öğrenme yeteneğini ifade eder.
- **Transfer Öğrenme:** Bir görev için bir model eğittiğiniz (görüntülerde örnek nesne algılama), ancak diğer bazı farklı görevler için bundan yararlanma ve geliştirme becerisi olan Derin Öğrenme kavramını ifade eder. Bilgisayarlı görüdeki (Computer vision) büyük başarıdan sonra, günümüzde NLP içinde güncel modeller sayesinde mümkün olmaktadır.
- **Transformatör (Transformers) Modelleri:** Öncelikle NLP'de kullanılan ve bugünlerde en son teknoloji NLP mimarilerinin temel yapı taşını oluşturan derin öğrenme modelleri ailesi. Yalnızca dikkat mekanizmalarına dayanan, yineleme ve evrişimleri tamamen ortadan kaldıran yeni ve basit bir ağ mimarisidir. Makine dil çevirileri konusunda özellikle tercih edilir. Kaynak: https://arxiv.org/pdf/1706.03762.pdf

---

### BERT nedir?
Google şirketi tarafından geliştirilmiştir. Büyük bir veri kümesi ile eğitilen genelleştirilmiş bir dil modelidir. Dildeki tüm dil bilimsel yapıyı bir çerçevede tutmuş, gerekli olduğunda diğer küçük dil işleme görevleri için transfer edilmesine olanak sağlamaktadır. Böylece bu küçük dil görevleri için minimal düzeye inmesinin yanı sıra 11 doğal dil işleme görevi için state-of-the-art başarı sergilemiştir.  
Uzun süreli kelimeler arasında bağımlılıkları belirleme yeteneği ve başarısı yüksek olan çift yönlü kodlayıcı modelidir. GPT-n ve diğer dil modellerinden ayıran özellikleri aşağıdaki gibidir:

- 24 Transformer bloğu ve 1024 gizli katmanı ve 349M parametre hesaplayan büyük bir modeldir.
- 800 milyon İngilizce kelime (BooksCorpus) ve 2.5 Milyar İngilizce kelime (Wikipedia) dahil, toplam 3.3 milyar kelimelik korpus üzerinde eğitilmiştir.
- Bu modelin eğitimi için 16 TPU’ya ihtiyaç duyulmuştur.

---

**Harika bir Türkçe Kaynak: [Susam Sokağı’ndan Doğal Dil İşlemeye](https://medium.com/basakbuluz/susam-soka%C4%9F%C4%B1ndan-do%C4%9Fal-dil-i%CC%87%C5%9Flemeye-7cc37903b5d4)**

---

Daha fazla bilgi için:

[HuggingFace Kaynak Dokümanı](https://huggingface.co/transformers/model_doc/bert.html)

---

[BERT için Kaynak Doküman](https://characters.fandom.com/wiki/Bert_(Sesame_Street)
<img src="https://i.hizliresim.com/SghEUo.png" width="500">

