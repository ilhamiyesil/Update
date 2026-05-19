# 🚀 Hesap Programı - Gelişmiş, hızlı ve basit.

Bu proje, finansal işlemleri (KDV, İskonto, Valör vb.) hızlı ve güvenilir bir şekilde yapmak, müşteri lisanslarını yönetmek ve modern bir arayüz sunmak amacıyla geliştirilmiş bir masaüstü yazılımıdır.

## 🛠 Kullanılan Teknolojiler
* **Dil:** C# (.NET Framework)
* **Arayüz (UI/UX):** Guna.UI2.WinForms, Özel ThemeManager (Dark/Light Mode)
* **Veritabanı:** SQLite & Dapper/Ado.Net Katmanlı Mimari (DAL)
* **Grafikler:** LiveCharts
* **Bulut & Otomasyon:** GitHub API (Otomatik Güncelleme & Lisans Kontrolü)

## 📌 Temel Özellikler
* **Dinamik KDV Yönetimi:** Veritabanı güdümlü, anlık hesaplama yapan ve pano (clipboard) dinleyen zeki hesap motoru.
* **Gelişmiş UX:** Kusursuzlaştırılmış TextBox formatlamaları (Anlık binlik ayraç, IBAN doğrulama).
* **Tema Motoru:** Sisteme tamamen entegre, anında geçiş yapılabilen Dark (Füme/Gri) ve Light (Lacivert/Beyaz) mod.
* **Bulut Lisanslama:** Cihaza özel HWID (Donanım Kimliği) üretimi, SHA256 şifreleme ve GitHub üzerinden anlık lisans doğrulama/iptal etme (Upsert mantığı).
* **Crash Kalkanı:** Global Exception Handling ile program çökmeden hataları yakalama ve loglama.

## ⚙️ Geliştirici Kurulumu (Setup)
1. Repoyu bilgisayarınıza klonlayın.
2. `ThemeManager.cs` dosyalarındaki referansların tam olduğundan emin olun.
3. **KRİTİK:** GitHub API bağlantıları için gerekli olan `Personal Access Token (PAT)` hiçbir zaman koda açık (hardcode) yazılmamalıdır. Ortam değişkenlerinden (Environment Variables) çekilmelidir.
4. Çözümü (Solution) `Release` modunda derleyip `HesapProgrami.db` şablonunun doğru kopyalandığından emin olun.

## 🔒 Güvenlik Notları
* `lisanslar.txt` dosyasına müdahale eden Admin (Lisans Üretici) formu ayrı bir projedir ve asla son kullanıcıya dağıtılmaz.
* Uygulama içi `Application.Exit()` yerine, güvenli kapanış için `Environment.Exit(0)` kullanılmaktadır.

---
*© 2026 İlhami YEŞİL - Tüm Hakları Saklıdır.*
