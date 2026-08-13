# 🚀 Teknoloji ve Finans Yapay Zekâ Asistanı (Ollama Tool Calling)

Bu proje, **Magibu Uygulamalı Yapay Zekâ Mimarisi Eğitimi** kapsamında geliştirilmiş, yerel (local) bir dil modeli üzerinde **Araç Kullanımı (Tool Calling)** yeteneklerini sergileyen modüler bir asistan uygulamasıdır. 

Sistem, internete bağlanarak gerçek zamanlı veri çekebilir, finansal kıyaslamalar yapabilir ve teknoloji gündemini anlık olarak takip edebilir.

## 🌟 Proje Özellikleri ve Araçlar (Tools)

Asistanın "Alet Çantasında" dış dünyaya (API'lere ve Web'e) bağlanan 3 ana araç bulunmaktadır:

1. 📰 **`get_donanimhaber_news(keyword)`:** DonanımHaber sitesini arka planda (BeautifulSoup ile) anlık olarak tarar. Kullanıcının sorusuna göre spesifik konulardaki (örn: *Yapay Zeka*, *Apple*, *Nvidia*) en güncel haberleri özetleriyle birlikte getirir.
2. 💱 **`get_exchange_rate(from, to, amount)`:** Frankfurter API kullanarak güncel döviz kurlarını çeker ve istenilen tutarı hedeflenen para birimine çevirir.
3. 🪙 **`get_crypto_performance(coin_id)`:** CoinGecko API kullanarak kripto paraların anlık dolar fiyatını ve **son 30 günlük getiri/kayıp** performanslarını çeker.

> **⚠️ Etik ve Yasal Tasarım (Mimari Kural):** Sistem İstemine (System Prompt) eklenen katı kurallar gereği, asistan **kesinlikle yatırım tavsiyesi (YTD) vermez**. Sadece API'lerden gelen 30 günlük verileri objektif şekilde karşılaştırır ve kararı kullanıcıya bırakır.

---

## 🛠️ Kurulum ve Gereksinimler

Bu projeyi kendi bilgisayarınızda çalıştırmak için aşağıdaki adımları izleyin:

**1. Gereksinimleri Yükleyin**
Projeyi indirdikten sonra terminalinizde gerekli Python kütüphanelerini kurun:
```bash
pip install requests beautifulsoup4
```
## 🛠️ Ollama'yı başlatın
Bilgisayarınızda Ollama'nın kurulu olduğundan ve arka planda çalıştığından emin olun. Tool calling için **llama3.1** veya **qwen2.5** modelleri önerilir.

## 🛠️ 🧪 Örnek Kullanım ve Log Çıktıları
