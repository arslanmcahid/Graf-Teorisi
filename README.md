# Graf Teorisi - Gezgin Satıcı Problemi (TSP) Projesi

Bu proje, **Graf Teorisi** dersi kapsamında geliştirilmiştir. Amaç, Google Maps API kullanarak gerçek dünya verileriyle Gezgin Satıcı Problemi'ni (Traveling Salesman Problem, TSP) çözmek ve farklı optimizasyon kriterlerine göre (zaman, mesafe, yakıt) en iyi rotayı bulmaktır.

## Özellikler

- Google Maps API ile gerçek zamanlı mesafe, süre ve yükseklik verisi çekme
- Zaman, mesafe veya yakıt tüketimine göre rota optimizasyonu
- NetworkX ile grafik oluşturma ve TSP çözümü
- Matplotlib ile grafiksel görselleştirme
- Google Maps üzerinde tam rotayı görüntüleme linki

## Gereksinimler

- Python 3.7+
- [Google Maps API Key](https://console.cloud.google.com)
- Aşağıdaki Python paketleri:
  - networkx
  - numpy
  - matplotlib
  - googlemaps

Kurulum için:

```bash
pip install networkx numpy matplotlib googlemaps
```

## Google Maps API Key Nasıl Alınır?

1. [Google Cloud Console](https://console.cloud.google.com) üzerinden yeni bir proje oluşturun.
2. Aşağıdaki API'leri etkinleştirin:
   - Distance Matrix API
   - Elevation API
   - Geocoding API
3. API anahtarı oluşturun ve kodda `API_KEY_SECRET` yerine kendi anahtarınızı yazın:
   ```python
   gmaps = googlemaps.Client(key='API_KEY_SECRET')
   ```

## Kullanım

1. `21118080067-Mücahid Sezgin ARSLAN Graf Teorisi.ipynb` dosyasını açın.
2. `locations` listesine ziyaret etmek istediğiniz şehir veya adresleri ekleyin:
   ```python
   locations = [
       "İstanbul, Türkiye",
       "Ankara, Türkiye",
       "İzmir, Türkiye"
   ]
   ```
3. Notebook'u çalıştırın. Sizden optimizasyon türü istenecek: `time`, `distance` veya `fuel`.
4. Sonuçlar:
   - Grafik üzerinde rota ve ağırlıklar
   - TSP çözümü ve detaylı yol bilgileri
   - Google Maps üzerinde tam rotayı gösteren link

## Notlar

- API anahtarınızı kimseyle paylaşmayın.
- Çok fazla istek atarsanız Google API kota sınırına ulaşabilirsiniz.
- Yakıt tüketimi hesabı için varsayılan değerler kullanılmıştır, isterseniz koddan değiştirebilirsiniz. Bunu çevrimiçi kaynaklarla da sağlamak mümkündür. İnternette yer alan bazı sitelerde araçların marka, model ve üretim yılına göre yakıt tüketimi verileri paylaşılmaktadır.

---

**Ders:** Graf Teorisi  
**Hazırlayan:** Mücahid Sezgin ARSLAN
