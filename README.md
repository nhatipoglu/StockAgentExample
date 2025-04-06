
## Örnek Sipariş Tahmin Raporu

### 1. Model Tahmin Ortalaması ve Varyansı
**Prophet Modeli:**
- Ortalama Tahmin: 9.59
- Varyans: 1.56

**XGBoost Modeli:**
- Ortalama Tahmin: 11.65
- Varyans: 2.63

**Analiz:**
- Prophet modeli daha düşük bir ortalama tahmin sunarken, XGBoost modeli daha yüksek bir ortalama tahmin sunmaktadır. Varyans açısından XGBoost'un daha yüksek bir varyansa sahip olması, tahminlerinin daha değişken olduğunu gösterir. Bu nedenle, Prophet modeli daha istikrarlı ve güvenilir bir tahmin sunmaktadır.

### 2. EOQ, ROP ve SS Değerleri Karşılaştırması
**Prophet Modeli:**
- EOQ: 380.75
- ROP: 73.90
- SS: 6.78

**XGBoost Modeli:**
- EOQ: 419.76
- ROP: 93.01
- SS: 11.44

**Analiz:**
- XGBoost modeli daha yüksek EOQ, ROP ve SS değerlerine sahiptir. Bu, XGBoost'un daha büyük sipariş miktarları ve daha yüksek güvenlik stokları önerdiği anlamına gelir. Ancak, bu durum daha fazla maliyet anlamına gelebilir. Prophet modeli daha düşük değerler sunarak daha az riskli bir sipariş stratejisi sunmaktadır.

### 3. Toplam Maliyet Analizi
**Prophet Modeli:**
- Toplam Maliyet: 2039.87 TL

**XGBoost Modeli:**
- Toplam Maliyet: 2519.71 TL

**Analiz:**
- Prophet modeli, toplam maliyet açısından daha avantajlıdır. Daha düşük maliyetler, işletmenin karlılığını artırır.

### 4. Varyant Bazlı Risk Skorları
**Yüksek Riskli Varyantlar:**
- Tüm varyantlar (Kırmızı, Mavi, Siyah) için risk skorları 0.855 ile 0.884 arasında değişmektedir. Bu, tüm varyantların yüksek risk taşıdığını göstermektedir.

**Önceliklendirme:**
- Tüm varyantlar yüksek risk taşıdığı için, sipariş önceliği verilmesi gereken varyantlar arasında ayrım yapmak zordur. Ancak, XGBoost modelinin tahminleri daha yüksek olduğu için, bu modelin tahminlerine göre sipariş verilmesi önerilebilir.

### 5. Sipariş Önerisi
- **Toplam Sipariş Miktarı:** 
  - Prophet: 51.90
  - XGBoost: 71.01
- **Öncelik Verilecek Varyantlar:**
  - Tüm varyantlar yüksek risk taşıdığı için, sipariş miktarları eşit dağıtılabilir. Ancak, XGBoost modelinin tahminleri dikkate alınarak, her varyant için önerilen sipariş miktarları artırılabilir.

### 6. Nihai Model Seçimi
**Seçim: Prophet Modeli**
- Prophet modeli, daha düşük maliyetler, daha istikrarlı tahminler ve daha az risk sunmaktadır. Ayrıca, daha düşük EOQ ve ROP değerleri ile daha az sermaye bağlamaktadır.

### 7. Nihai Karar ve Öneri
- **Servis Seviyesi:** �, bu da müşteri memnuniyetini artırır.
- **Stok-out Riski:** Prophet modeli ile daha düşük.
- **Maliyetler:** Prophet modeli daha düşük maliyet sunuyor.
- **Varyant Dengesi:** Tüm varyantlar yüksek risk taşıyor, bu nedenle eşit dağıtım önerilebilir.
- **Operasyonel Uygulanabilirlik:** Prophet modeli daha az risk ve maliyet sunduğu için daha uygulanabilir.

**Nihai Sipariş Miktarı:** 51 adet (her varyant için eşit dağıtım önerilir).

**Öneri:** Prophet modeline dayanarak, toplam 51 adet sipariş verilmesi ve tüm varyantlar arasında eşit dağıtım yapılması önerilmektedir. Bu, maliyetleri minimize ederken, müşteri memnuniyetini de artıracaktır.