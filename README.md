<div align="center">

<img src="assets/ui/logo.png" alt="Tohum Three" width="128" />

# Tohum Three

**Three.js WebGPU ile calisan acik kaynak prosedurel agac ve bitki ureticisi.**

**▶ [Canli demoyu ac](https://anubiszk.github.io/tohum-three/)** &nbsp;(WebGPU destekli Chrome/Edge onerilir)

</div>

Tohum Three; tur secip parametreleri ayarlayarak dokulu, ruzgarla hareket eden benzersiz 3D agaclar ve bitkiler uretmenizi saglar. Uretilen bitkiyi sahnede inceleyebilir, LOD ayarlarini degistirebilir ve tek tikla `.glb` olarak disa aktarabilirsiniz.

![Tohum Three - Ak Mese agaci ve canli kontrol paneli](docs/media/hero_temperate.png)
![Tohum Three - Col biyomunda Joshua Agaci ve kontrol paneli](docs/media/hero.png)

> **Durum: `v0.1.0-alpha`.** On tur, LOD zinciri, disari aktarma ve yasayan sahne mevcut. Proje erken asamada oldugu icin keskin kenarlar olabilir.

## Icerik

- **Iki biyomda on tur**
  - *Iliman:* Ak Mese, Kizil Akcaagac, Lale Agaci, Sigla, Amerikan Kayini, Ponderosa Cami, Loblolly Cami, Douglas Goknari
  - *Col:* Joshua Agaci, Saguaro
- **Iki uretici.** Genis yapraklilar ve kozalaklilar icin Weber-Penn parametrik modeli; col sukulentleri icin bastan yazilmis dikotom L-sistemi.
- **Gercekci morfoloji.** Dal acilari, incelme, kivrim ve tac formu tur referanslarina gore ayarlanir.
- **Kart tabanli yapraklar.** Tek yaprak ve igne kartlari, arka isik gecirgenligi, ruzgar animasyonu ve LOD uyumuyla calisir.
- **LOD zinciri ve impostorlar.** LOD0 tam geometri, LOD1 azaltilmis geometri, LOD2 pisirilmis dal kartlari ve uzak mesafe billboard gorunumu.
- **Yasayan sahne.** Agac halkasi, ruzgarli otlar/col calilari, prosedurel kayalar, PBR arazi, bulutlar, oynatilabilir gunes ve biyoma gore ortam sesi.
- **glTF aktarimi.** Tek tikla `.glb` indirir.

## Gereksinimler

WebGPU destekli guncel Chrome veya Edge onerilir. WebGL2 fallback vardir, ancak hedef yol WebGPU'dur.

## Calistirma

```bash
npm install
npm run dev      # http://localhost:5390
```

Production build:

```bash
npm run build    # dist/
npm run preview  # build'i servis eder
```

## Tur ekleme ozeti

Yeni bitkiler `src/species/<ad>.js` icine bir preset ekleyerek ve `src/species/index.js` dosyasina kaydederek eklenir. Doku dosyalari `assets/bark/` ve `assets/leaves/` altindaki adlandirma kurallarini izler:

- Kabuk: `<ad>_albedo.png`, yaninda `_normal` ve `_roughness`
- Yaprak/igne: `<ad>_albedo.png`, yaninda `_normal`, `_roughness`, `_translucency`

Detayli notlar `docs/` klasorundedir.

## Lisans ve kaynak

MIT lisansi ile yayinlanmistir. Bu repo, SkyeShark/SeedThree temel alinarak Turkcelestirilmis ve `tohum-three` adiyla yayinlanmistir.
