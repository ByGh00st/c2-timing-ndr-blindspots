[English README](README.md)

Bu depo, ByGhost C2/NDR araştırma yayınının ana deposudur. Ayrıntılı matematiksel açıklamalar, mimari diyagram ve tespit mühendisliği bölümleri [İngilizce README](README.md) içinde korunmaktadır.

# Komuta-Kontrol (C2) Trafiğinin Evrimi ve NDR Kör Noktaları

### Şekillendirilmiş Zamanlama Dinamiklerine Karşı İleri Düzey Mavi Takım Taktikleri

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.23141650.svg)](https://doi.org/10.5281/zenodo.23141650)
[![Lisans: CC BY-NC-ND 4.0](https://img.shields.io/badge/License-CC_BY--NC--ND_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-nd/4.0/)
[![Sürüm: v1.0](https://img.shields.io/badge/version-v1.0-blue.svg)](https://github.com/ByGh00st/c2-timing-ndr-blindspots/releases/tag/v1.0)
[![Diller: Türkçe | İngilizce](https://img.shields.io/badge/diller-T%C3%BCrk%C3%A7e%20%7C%20%C4%B0ngilizce-blue.svg)](#yayınlar)

## Genel Bakış

Bu savunma odaklı siber güvenlik araştırması, Komuta-Kontrol (C2) trafiğinin zamanlama dinamiklerini ve yalnızca ağ akışlarına dayanan NDR yaklaşımlarının kör noktalarını inceler. İstatistiksel trafik analizini katmanlar arası telemetri, tespit mühendisliği ve dedektör validasyonuyla birlikte ele alır.

Çalışma; olay-zamanı jitter ile aralık jitter ayrımını, gelişler arası süre (Inter-Arrival Time, IAT) analizini, periyodiklik ve spektral analizi, öz-benzerliği, uzun menzilli bağımlılığı (LRD), Hurst üssünü, ağır kuyruklu trafiği ve Hill tahmincisini kapsar. Ağ gözlemlerinin yorumlanmasında uç nokta, süreç, oturum ve kimlik bağlamının rolünü; ETW ve eBPF savunma telemetrisi ile T1-T20 tespit ve korelasyon kataloğu üzerinden tartışır.

Sigma, KQL, SPL ve eBPF odaklı tespit mühendisliği; temel hat / baseline kalibrasyonu, yanlış pozitif yönetimi ve validasyonla birlikte değerlendirilir. Teknik içeriğin esas kaynağı PDF yayınlarıdır. Bu depo, yayınlara erişim, atıf bilgileri ve dosya bütünlüğü doğrulaması sağlar.

## Temel Araştırma Alanları

- C2 zamanlama modelleri, IAT istatistikleri, periyodiklik ve spektral analiz.
- Öz-benzerlik, uzun menzilli bağımlılık, Hurst üssü tahmini ve Hill tahmincisiyle ağır kuyruk analizi.
- Akış düzeyindeki tespit sınırları; akış ↔ süreç ↔ oturum ↔ kimlik korelasyonu ve uç nokta durumu.
- ETW ve eBPF ile savunma telemetrisi.
- T1-T20 savunma odaklı tespit ve korelasyon kavramları; Sigma, KQL, SPL ve eBPF odaklı tespit mühendisliği.
- Temel hat / baseline kalibrasyonu, yanlış pozitif yönetimi ve dedektör validasyonu.

## Temel Mimari Tez

Bir ağ akışının yalnızca “insan davranışına benzer” görünmesi, meşru olduğuna dair yeterli kanıt değildir. Tespit yaklaşımı; bu akışı üreten sürecin, oturumun, kimliğin, uç nokta durumunun ve ağ davranışının birbiriyle tutarlı olup olmadığını değerlendirmelidir.

Bu yaklaşım, bağlamsal tespit ve validasyonu gerekçelendiren bir mimari görüştür; deneysel olarak kanıtlanmış evrensel bir teorem olarak sunulmaz.

## Matematiksel Kapsam

- **Model A: olay-zamanı jitter** ile **Model B: aralık jitter** arasındaki ayrım.
- İstatistik ve spektrum yorumunda olay dizisi (event train) ile skaler IAT dizisinin ayrılması.
- Açıkça belirtilen varsayımlar altında bir gecikmeli (lag-1) otokorelasyon sonucu ve geçerlilik sınırları.
- Yenilenme spektrumu (renewal spectrum) ve zamanlama modelleriyle ilişkisi.
- Öz-benzer / uzun menzilli bağımlı trafik ve Hurst üssü tahmini.
- Hill tahmincisi dahil ağır kuyruk tanı yöntemleri ve yorumlama sınırları.

Matematiksel sonuçlar, yayında verilen varsayımlarla birlikte okunmalıdır. Bu özet, operasyonel uygulama prosedürlerini aktarmaz.

## Taktik Kataloğu

Yayın, **T1-T20 savunma odaklı tespit ve korelasyon kavramlarını** içerir. Katalog, istatistiksel gözlemleri bağlamsal telemetri ve tespit mühendisliğiyle ilişkilendirir. Teknik ayrıntılar, varsayımlar, kalibrasyon gereksinimleri ve validasyon değerlendirmeleri PDF yayınlarında yer alır.

## Yayınlar

| Dil | Yayın | Doküman kimliği |
| --- | --- | --- |
| İngilizce | [Teknik Rapor EN v1.0](publications/ByGhost-C2-NDR-Technical-Report-EN-v1.0.pdf) | `SOC-NDR-MASTER-001-EN` |
| Türkçe | [Teknik Rapor TR v1.0](publications/ByGhost-C2-NDR-Technical-Report-TR-v1.0.pdf) | `SOC-NDR-MASTER-001` |

## Zenodo / DOI

- **Sürüm DOI:** [10.5281/zenodo.23141650](https://doi.org/10.5281/zenodo.23141650), doğrudan v1.0 sürümünü tanımlar.
- **Kavram DOI:** [10.5281/zenodo.23141649](https://doi.org/10.5281/zenodo.23141649), Zenodo'daki en güncel sürüme yönlendirir.

Bu sürüme atıf yaparken sürüm DOI'sini kullanın.

## Atıf

Erarslan, Oğulcan (ByGhost). (2026). *The Evolution of Command-and-Control (C2) Traffic and NDR Blind Spots: Advanced Blue Team Tactics Against Shaped Timing Dynamics*. Version 1.0. ByGhost Security. Zenodo. [https://doi.org/10.5281/zenodo.23141650](https://doi.org/10.5281/zenodo.23141650).

Makine tarafından okunabilir atıf bilgileri [CITATION.cff](CITATION.cff) dosyasındadır.

## Kamuya Açık Yayının Kapsamı

Yayın; savunma odaklı tespit, ölçüm, telemetri, validasyon ve tespit mühendisliğine odaklanır. Özel mülkiyete konu C2 uygulama mimarisini, operasyonel saldırı kullanımına yönelik prosedürleri, saldırgan trafik üretim kodunu, devreye alma parametrelerini veya tespitten kaçınma reçetelerini açıklamaz.

## Dosya Bütünlüğü

Aşağıdaki SHA-256 değerleri, kopyalama öncesinde nihai kaynak PDF'lerden hesaplanmıştır. Depodaki iki kopyanın kaynak dosyalarla bayt düzeyinde aynı olduğu doğrulanmış, yalnızca kopyaların dosya adları değiştirilmiştir.

| Dosya adı | SHA-256 |
| --- | --- |
| `ByGhost-C2-NDR-Technical-Report-EN-v1.0.pdf` | `96d8138312ca84f2cdfe905a64566aede2fdcc0de4d7a589dbdb8e471e27bc85` |
| `ByGhost-C2-NDR-Technical-Report-TR-v1.0.pdf` | `d1da8d191cdb5ff661a659c56aa13c7645bf5b2ce77af149c7b076d048ae4e2a` |

## Lisans

Aksi açıkça belirtilmedikçe, depodaki yayın materyalleri [Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International (CC BY-NC-ND 4.0)](https://creativecommons.org/licenses/by-nc-nd/4.0/) lisansı altında sunulur. Ayrıntılar için [LICENSE.md](LICENSE.md) dosyasına bakın.

## Yazar

**Oğulcan (ByGhost) Erarslan**

Senior Solutions Architect | Cyber Security Specialist

ByGhost Security

- [Web sitesi](https://byghost.tr/)
- [GitHub](https://github.com/ByGh00st)
- [LinkedIn](https://linkedin.com/in/byghost-tr)
