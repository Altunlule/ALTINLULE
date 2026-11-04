# Altın Lüle Tobacco – GitHub Pages sürümü

PHP gerektirmez. Site GitHub Pages'te çalışır, yönetim paneli değişiklikleri doğrudan GitHub'a kaydeder.

- `index.html` : site
- `admin.html` : yönetim paneli (`https://KULLANICI.github.io/REPO/admin.html`)
- `data.json`  : sitenin verileri (ürün, kategori, ayarlar). Panel kaydedince bu dosya güncellenir.
- `uploads/`   : panelden yüklenen fotoğraflar

## 1. Repo ve yükleme
1. github.com/new → ad: `altin-lule` → **Public** seçin (ücretsiz Pages için gerekli) → Create.
2. "uploading an existing file" bağlantısı → zip'teki tüm dosyaları sürükleyin → **Commit changes**.

## 2. Siteyi yayına alma
Repo > **Settings > Pages** > Source: **Deploy from a branch** > Branch: `main` / `(root)` > **Save**.
1-2 dakika sonra adres görünür: `https://KULLANICI.github.io/altin-lule/`

## 3. Kaydetme anahtarı (token) – bir kez
1. GitHub > sağ üst profil > **Settings > Developer settings > Personal access tokens > Fine-grained tokens > Generate new token**
2. Repository access: **Only select repositories** → `altin-lule`
3. Permissions > **Contents: Read and write**
4. Süre seçin, oluşturun ve çıkan `github_pat_...` anahtarını kopyalayın.
5. `.../altin-lule/admin.html` adresini açın, şifreyi girin, üstteki "GitHub bağlantısı" kutusuna anahtarı yapıştırıp **Bağlantıyı kaydet**, sonra **Test et**.

Anahtar sadece o tarayıcıda saklanır. Kimseyle paylaşmayın.

## Yönetim şifresi
Giriş şifresi `cumhur2000`. Değiştirmek için yeni şifrenin SHA-256 değerini üretip `admin.html` içindeki `HASH` değerine yazın:
`echo -n "yenisifre" | sha256sum`

Not: Bu şifre sadece giriş ekranıdır; asıl koruma GitHub anahtarıdır. Anahtarı olmayan kimse değişiklik kaydedemez.

## Kendi alan adı
Settings > Pages > Custom domain bölümüne alan adını yazın ve alan adı sağlayıcınızda DNS ayarını GitHub'ın gösterdiği şekilde yapın.

## Bilmeniz gerekenler
- Her KAYDET'ten 1-2 dakika sonra site güncellenir.
- Repo herkese açıktır; ürünler, fiyatlar ve fotoğraflar zaten sitede herkese açık olduğu için sorun değildir.
- Tütün ürünlerinin internetten satışı ve kargosu yasaktır; sitede sadece aksesuar ve mekan tanıtımı yapın.
