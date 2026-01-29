# ING Hubs Türkiye Datathon – Churn Prediction

Bu repository, **ING Hubs Türkiye Datathon** kapsamında geliştirdiğim **müşteri churn tahmin çözümünü** içermektedir.

Amaç, müşterilerin **referans tarihinden sonraki 6 ay içinde churn yaşama olasılıklarını** tahmin etmektir.

---

## 📂 Repository İçeriği

* **Notebook:**

  * Veri okuma ve birleştirme
  * Feature engineering (reference-date bazlı, leakage-free)
  * Model eğitimi
  * Yarışma metriğine uygun değerlendirme
  * Submission dosyası üretimi

Tüm çözüm **tek notebook** üzerinden uçtan uca yürütülmüştür.

---

## 🧠 Kullanılan Yaklaşım

* Aylık müşteri işlem geçmişinden **davranışsal özet özellikler**
* Referans tarihine göre **zaman pencereli feature engineering**
* Demografik ve işlem verilerinin birleştirilmesi
* Dengesiz churn problemi için **olasılık bazlı modelleme**
* Kaggle yarışma metriğine birebir uyumlu skor hesaplama

Model çıktıları, **en yüksek %10’luk churn olasılığı dilimi** üzerinden Recall ve Lift metrikleri dikkate alınarak optimize edilmiştir.

---

## 📊 Evaluation

Yarışma metriği şu bileşenlerden oluşmaktadır:

* **Gini (%40)**
* **Recall@10% (%30)**
* **Lift@10% (%30)**

Notebook içerisinde:

* ROC AUC → Gini dönüşümü
* Recall@10% ve Lift@10% hesapları
  ayrı ayrı açık şekilde uygulanmıştır.

---

## 📁 Kullanılan Datasetler

* `customer_history.csv` – Aylık işlem özetleri
* `customers.csv` – Demografik bilgiler
* `reference_data.csv` – Train etiketleri
* `reference_data_test.csv` – Test seti
* `sample_submission.csv` – Gönderim formatı

---

## 📤 Output

Notebook sonunda:

* Test müşterileri için **churn olasılıkları**
* Kaggle formatına uygun **submission.csv**
  üretilmektedir.

---

## 📝 Notlar

* Feature engineering adımları **data leakage içermeyecek** şekilde tasarlanmıştır
* Modelleme ve değerlendirme tamamen yarışma kural setine uygundur
* Kodlar okunabilirlik ve tekrar üretilebilirlik gözetilerek yazılmıştır


* ya da **CV/GitHub profilinde gözüksün diye daha “showcase”** yaparım

Hangisi?
