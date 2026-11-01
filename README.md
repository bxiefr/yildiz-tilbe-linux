# Yıldız Tilbe Linux

Debian 13 (trixie) tabanlı, XFCE masaüstlü meme dağıtımı. GNU/Linux'tan büyük olma iddiasındadır.

> Resmi değildir, parodi bir hobi projesidir.

## Yerelde derleme (Debian/Ubuntu)

```bash
sudo apt install live-build
sudo lb config
sudo lb build
```

Çıkan `.iso` dosyası proje klasöründe olur.

## GitHub ile release çıkarma

```bash
git tag v1.0
git push origin v1.0
```

Tag atılınca `.github/workflows/build.yml` ISO'yu derler ve Releases sayfasına yükler.

## Site

`docs/` klasörü GitHub Pages ile yayınlanır:
Settings → Pages → Branch: `main`, klasör: `/docs`.

## Klasör yapısı

| Yol | Ne işe yarar |
|---|---|
| `auto/` | live-build ana ayarları |
| `config/package-lists/` | kurulacak paketler |
| `config/includes.chroot/` | sisteme kopyalanan dosyalar (motd, alias vb.) |
| `config/hooks/live/` | derleme sırasında çalışan betikler |
| `branding/` | logo ve duvar kağıdı (kendi çizimlerin) |
| `docs/` | GitHub Pages sitesi |
| `.github/workflows/` | otomatik derleme ve release |
