# 🧊 WebGL Sample Projects
### (Bilgisayar Grafiği Dersi Kapsamında Hazırladığım WebGL Çalışmaları)

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)](#)
[![WebGL](https://img.shields.io/badge/WebGL-990000?style=flat&logo=webgl&logoColor=white)](#)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)](#)

Bu depo, Bilgisayar Grafiği dersi kapsamında WebGL kullanarak geliştirdiğim temel grafik programlama örneklerini ve ödevleri içermektedir. Çalışmalar; gölgelendirici (shader) yönetimi, model dönüşümleri, etkileşim ve ünlü fraktal yapılar gibi konuları kapsar.

## 📚 İçindekiler
- [Proje Hakkında](#proje-hakkında)
- [Özellikler](#özellikler)
- [Kullanılan Teknolojiler ve Kaynaklar](#kullanılan-teknolojiler-ve-kaynaklar)
- [Kurulum ve Kullanım](#kurulum-ve-kullanım)
- [Proje Yapısı](#proje-yapısı)
- [Geliştirme Süreci](#geliştirme-süreci)
- [Katkıda Bulunma](#katkıda-bulunma)
- [İletişim](#iletisim)
- [Lisans](#lisans)

---

## Proje Hakkında
Bu çalışma, bilgisayar grafiğinin temel prensiplerini (model-view dönüşümleri, ışıklandırma modelleri, tampon nesneler) uygulamalı olarak öğrenmek amacıyla hazırlanmıştır. Her bir klasör, bağımsız olarak çalıştırılabilen farklı bir WebGL sahnesini içerir.

* **Geliştirici:** Haluk Can SARIÖZ
* **Ders:** Bilgisayar Grafiği (Computer Graphics)
* **Amaç:** GPU tabanlı grafik programlamayı ve OpenGL ES gölgelendirici yapısını kavramak

---

## Özellikler
* **Gerçek Zamanlı Render:** Doğrudan tarayıcı üzerinde GPU hızlandırmalı grafik işleme.
* **Çoklu Örnek:** Temel çizimden, gölgeli cisimlere ve etkileşimli uygulamalara kadar farklı zorluk seviyelerinde projeler.
* **Phong Işık Modeli:** `Shaded Teapot` ve bazı ödevlerde Phong yansıma modelinin pratik uygulaması.
* **Kullanıcı Etkileşimi:** Fare ve klavye ile 3B cisimlerin (özellikle demlik modelinin) kontrolü.
* **Yardımcı Kütüphaneler:** Ders kapsamında sağlanan `initShaders` ve `MV.js` gibi yardımcı araçların etkin kullanımı.

---

## Kullanılan Teknolojiler ve Kaynaklar
* **WebGL (OpenGL ES 2.0):** Temel grafik API'si.
* **JavaScript (ES6):** Tüm uygulama mantığı ve shader yönetimi.
* **HTML5 Canvas:** Görüntüleme yüzeyi.
* **Eğitim Kaynakları:** Proje, büyük ölçüde Prof. Edward Angel'ın kaynak kodlarına dayanmaktadır:
  * [WebGL Examples (UNM)](https://www.cs.unm.edu/~angel/WebGL/)
* **Teorik Altyapı:**
  * [Phong Reflection Model (Wikipedia)](https://en.wikipedia.org/wiki/Phong_reflection_model)

---

## Kurulum ve Kullanım

Bu projeler sunucu taraflı herhangi bir kod içermediği için herhangi bir paket yüklemeye gerek yoktur. Ancak, WebGL shader'ları dış kaynaklı dosyalardan yüklendiği için **doğrudan dosyaya çift tıklayarak çalıştırmak güvenlik kısıtlamalarına takılabilir.**

Bu nedenle, bir yerel sunucu (local server) üzerinden çalıştırmanız **zorunludur**.

### 1. Depoyu Klonlayın
```bash
git clone https://github.com/halukcansarioz/WebGl-Sample.git
```

### 2. Proje Dizinine Gidin
```bash
cd WebGl-Sample
```

### 3. Yerel Sunucu Başlatın ve Çalıştırın

Aşağıdaki yöntemlerden birini kullanarak projeyi görüntüleyebilirsiniz:

* **VS Code Live Server (Önerilen):** VS Code'da herhangi bir `.html` dosyasına sağ tıklayıp `"Open with Live Server"` seçeneğine tıklayın.
* **Node.js `http-server`:**
    ```bash
    npx http-server .
    ```
    Komutu çalıştırdıktan sonra terminalde yazan adresi (genelde `http://127.0.0.1:8080`) tarayıcıda açın ve istediğiniz klasöre gidin.
* **Python:** Python kurulu ise terminalde şu komutu çalıştırın:
    ```bash
    python -m http.server
    ```

> ⚠️ **Not:** Projelerin çalışması için tarayıcınızın WebGL'yi desteklemesi gerekmektedir. Çoğu modern tarayıcı (Chrome, Firefox, Edge) varsayılan olarak destekler.

---

## Proje Yapısı
Her bir klasör, birbirinden bağımsız bir WebGL uygulamasını temsil eder. Bir klasörün içinde genellikle `.html` arayüz dosyası, `.js` mantık/shader dosyası ve ortak kütüphaneleri içeren bir `src` klasörü bulunur.

```text
WebGl-Sample/
├── Base/                 # Temel çokgen (küp) çizimi ve renklendirme
├── Rotation/             # Döndürme dönüşümleri (Rotation transform)
├── Teapot/               # Klasik Utah Demliği çizimi
├── Shaded Teapot/        # Phong ışık modeli ile gölgelendirilmiş demlik
├── View/                 # Kamera ve görüş açısı ayarları
├── Interaction/          # Fare ve klavye etkileşimli demlik kontrolü
├── Sierpinski/           # 2B Sierpinski Üçgeni fraktalı
├── Sierpinski-2/         # Gelişmiş Sierpinski fraktal uygulaması
├── İlk/                  # İlk WebGL denemesi (başlangıç seviyesi)
├── Ödev/                 # Ders kapsamında teslim edilen ödev(ler)
├── Ödev Örnek/           # Ödev için referans örnek çalışma
├── Ödev-2/               # İkinci ödev çalışması
└── README.md             # Proje dökümantasyonu
```

---

## Geliştirme Süreci

### 1. Forklama
Kendi grafik denemelerinizi eklemek için depoyu fork'layabilirsiniz.

### 2. Yeni Dal (Branch) Oluşturma
```bash
git checkout -b yeni-örnek/phong-küre
```

### 3. Kodları Gönderme (Push)
```bash
git push origin yeni-örnek/phong-küre
```

---

## Katkıda Bulunma
1. Bu depoyu **Fork**'layın.
2. Bir **Branch** oluşturun (`git checkout -b feature/YeniSahne`).
3. Yeni bir klasöre `.html` ve `.js` dosyalarınızı ekleyin.
4. Değişikliklerinizi **Commit** edin (`git commit -m 'Ekleme: Yeni ışıklandırma örneği'`).
5. Kodlarınızı **Push**'layın (`git push origin feature/YeniSahne`).
6. Bir **Pull Request** açın.

> 💡 **Öneri:** Yeni bir örnek eklerken, ortak `src` klasörünü kullanarak `initShaders` ve `MV.js` gibi yardımcı fonksiyonlara erişebilirsiniz.

---

<a name="iletisim"></a>
## İletişim
**Haluk Can Sarıöz** - [GitHub Profilim](https://github.com/halukcansarioz)  
**Proje Linki:** [https://github.com/halukcansarioz/WebGl-Sample](https://github.com/halukcansarioz/WebGl-Sample)

---

## Lisans
Bu proje [MIT Lisansı](LICENSE) ile lisanslanmıştır.
