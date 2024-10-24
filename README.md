# Fish_Classification_With_ANN
Global ai hub öncülünde ANN Proje Uygulması



Balık Türlerini Sınıflandırma Projesi

Bu proje, Kaggle'dan alınan "A Large Scale Fish Dataset" veri setini kullanarak balık türlerini sınıflandırmaya yönelik bir model geliştirmeyi amaçlamaktadır. Projede balık türlerini tanıyabilen bir derin öğrenme modeli oluşturulmuştur. Adım adım veri işleme, model eğitimi ve değerlendirme yapılmıştır.

# Kullanılan Kütüphaneler
Proje için Python'da temel veri işleme ve görselleştirme kütüphaneleri olan "Pandas", "NumPy", "Matplotlib" ve "Seaborn" kullanılmıştır. Derin öğrenme modeli için ise "TensorFlow" ve "Keras" kütüphaneleri tercih edilmiştir. Ayrıca, veri arttırma ve resim işleme işlemleri için ImageDataGenerator kullanılmıştır.

# Veri Seti
Veri seti, balık resimlerinden oluşuyor ve her bir balık türü için ayrı bir klasörde bulunuyor. Resimler `.png` formatında. Projede, veri setindeki resimler taranarak etiket bilgisi ve dosya yolları bir DataFrame'e yüklendi. Resimlerin her biri bir balık türünü temsil eden etiketlerle birlikte işlendi.

# Veri Ön İşleme
Veriler yüklendikten sonra, her balık türüne ait resimlerin dağılımı görselleştirildi. Veri seti eğitim ve test olarak ikiye ayrıldı (%80 eğitim, %20 test). Veri arttırma yöntemleriyle eğitim setinin çeşitliliği artırıldı; döndürme, yakınlaştırma, kaydırma gibi işlemler uygulandı.

# Model Yapısı
Model olarak Sequential yapı kullanıldı ve şu katmanlar oluşturuldu:
- Conv2D: Görsellerin özelliklerini çıkaran konvolüsyon katmanları.
- MaxPooling2D: Boyut küçültme işlemi.
- Dropout: Aşırı öğrenmeyi (overfitting) önlemek için bazı nöronların geçici olarak eğitim dışı bırakılması.
- Flatten ve **Dense** katmanları: Tam bağlantılı katmanlar, sınıflandırmayı sağlar.

Modelin son katmanında softmax aktivasyon fonksiyonu kullanılarak, her balık türüne olasılık ataması yapılır.

# Eğitim ve Sonuçlar
Model 20 epoch boyunca eğitildi ve sonuçlar test setiyle değerlendirildi. Eğitimin her epoch'unda modelin doğruluğu ve kaybı izlendi. Test setindeki doğruluk sonuçlarına göre, modelin balık türlerini ne kadar başarılı bir şekilde sınıflandırabildiği görüldü.

# Sonuç ve Değerlendirme
Model eğitiminde veri arttırma teknikleri sayesinde daha iyi sonuçlar alındı. Ancak, daha yüksek başarı oranı elde etmek için model yapısı ve hiperparametreler üzerinde daha fazla deneme yapılabilir. 

Bu proje ile birlikte temel bir derin öğrenme modelinin nasıl oluşturulacağı ve resim verileriyle nasıl çalışılacağı öğrenilmiş oldu.


# Kaggle proje linki 
https://www.kaggle.com/code/vedataydn/fish-classification-project/edit/run/202925573
