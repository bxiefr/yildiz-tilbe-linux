# Yıldız Tilbe Linux

Debian 13 (trixie) tabanlı, XFCE masaüstlü, Türkçe hazır gelen eğlenceli bir Linux dağıtımı.

> Resmi değildir, parodi bir hobi projesidir. Yıldız Tilbe ile bağlantısı yoktur.

## Özellikler

- Debian 13 (trixie) tabanlı, kararlı ve güvenilir
- Hafif ve hızlı XFCE masaüstü
- Türkçe dil, klavye ve saat dilimi hazır
- USB'den canlı açılır, beğenirsen Calamares ile kurulur
- Firefox ve temel araçlar yüklü gelir
- Terminalde meme komutları ve renkli karşılama

## İndirme ve kullanma

1. [Releases](../../releases/latest) sayfasından `.iso` dosyasını indir.
2. İndirdiğin dosyanın doğruluğunu `SHA256SUMS` ile kontrol et.
3. ISO'yu USB belleğe yaz (Ventoy, balenaEtcher ya da Rufus kullanabilirsin).
4. Bilgisayarı USB'den başlat, canlı oturum açılır.
5. Beğenirsen masaüstündeki kurucuyla diske kur.

Canlı oturumda varsayılan kullanıcı `user`, şifre `live`'dır.

### Meme komutları

Terminale şunları yazabilirsin:

| Komut | Ne yapar |
|---|---|
| `yildiz` | Renkli büyük karşılama yazısı |
| `hosgeldin` | Sistem bilgisini gösterir (fastfetch) |
| `guncelle` | Sistemi günceller |

Ayrıca her terminal açılışında rastgele bir söz inek tarafından okunur.

## Yerelde derleme (Debian/Ubuntu)

```bash
sudo apt install live-build
sudo lb config
sudo lb build
```

Çıkan `.iso` dosyası proje klasöründe olur.

## GitHub ile release çıkarma

Tamamen GitHub üzerinden, elle tetiklenir:

1. Repoda **Actions** sekmesine git.
2. Soldan **ISO Derle ve Release Cikar** workflow'unu seç.
3. **Run workflow** butonuna bas, sürüm adını yaz (örnek: `v1.0`).
4. Derleme bitince ISO **Releases** sayfasına otomatik yüklenir.

Derleme yaklaşık 20-40 dakika sürer. "Releases sayfasına yükle" kutusunun işaretini kaldırırsan ISO sadece çalışmanın **Artifacts** bölümünde kalır.

## Site

`docs/` klasörü GitHub Pages ile yayınlanır:
Settings → Pages → Branch: `main`, klasör: `/docs`.

## Klasör yapısı

| Yol | Ne işe yarar |
|---|---|
| `auto/` | live-build ana ayarları |
| `config/package-lists/` | kurulacak paketler |
| `config/includes.chroot/` | sisteme kopyalanan dosyalar (motd, alias, duvar kağıdı vb.) |
| `config/hooks/live/` | derleme sırasında çalışan betikler |
| `config/bootloaders/` | USB açılış menüsü görselleri |
| `branding/` | logo ve duvar kağıdı kaynakları |
| `docs/` | GitHub Pages sitesi |
| `.github/workflows/` | ISO derleme ve release workflow'u |
