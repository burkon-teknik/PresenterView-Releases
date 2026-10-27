# PresenterView

**[Türkçe](#türkçe) · [English](#english)**

📥 **İndir / Download:** [Son sürüm / Latest release](https://github.com/burkon-teknik/PresenterView-Releases/releases/latest)

---

## Türkçe

PresenterView, kongre ve salon sunumları için bir Windows bildirim alanı (tray) uygulamasıdır. Üç ekranlı bir dizüstü bilgisayarda PowerPoint **Sunucu Görünümünü**, konuşmacının önündeki ayrı bir ekrana (kürsü ekranı) güvenli şekilde yansıtır.

### Ekran düzeni

| Ekran | Ne gösterir |
|---|---|
| **Ana ekran** (laptop) | PowerPoint Sunucu Görünümü burada açılır. |
| **Salon ekranı** (HDMI) | İzleyicinin gördüğü slayt. |
| **Konuşmacı ekranı** (kürsü) | Gösteri yokken yalnızca masaüstü duvar kağıdı, gösteri sırasında Sunucu Görünümünün canlı kopyası. Hangi porttan bağlandığı önemsizdir. |

### Özellikler

- **Sunucu Görünümü Modu** (PowerPoint için): F5 ile gösteri başlayınca Sunucu Görünümü konuşmacı ekranına kopyalanır, Esc ile bitince duvar kağıdına döner.
  - Ana ekranda yaptığınız hiçbir şey (pencereler, masaüstü simgeleri, görev çubuğu) konuşmacı ekranına **sızmaz**.
  - Sunucu Görünümünün üstüne başka bir pencere gelse bile o pencere konuşmacı ekranına gitmez.
  - Görüntü 1 saniyeden uzun güncellenmezse konuşmacı ekranında turuncu **"Görüntü güncellenmiyor"** uyarısı çıkar; konuşmacı eski slaytı canlı sanmaz.
- **Genel Mod** (PDF, Canva, tarayıcı vb. için): Salon ekranında ne görünüyorsa, fare imleci dahil, birebir konuşmacı ekranına kopyalanır.
- **Alt+O** ile modlar arasında geçilir; seçilen mod kaydedilir.
- **Ekran koruması:** Fare konuşmacı ekranına giremez, oraya taşınan pencereler ana ekrana geri alınır.
- **Kaplama pencereleri:** Kongre sayacı gibi programların gösterge penceresi, hangi ekranda olursa olsun konuşmacı ekranında da görünür. Kontrol panelleri ve ayar pencereleri görünmez.
- **Logitech Spotlight lazeri** (Logitech yazılımı gerekmez): Üst tuş basılı tutulunca salon ekranında lazer noktası çıkar; Sunucu Görünümü Modunda aynı nokta konuşmacı ekranındaki slaytta da görünür. Renk ve boyut ayarlanabilir.
- **Yalnızca lazer:** Üç ekran yoksa program yalnızca Spotlight lazeriyle çalışır, üçüncü ekran takılınca kendiliğinden normale döner.
- **Güncelleme:** Simge menüsündeki "Güncellemeleri denetle..." ile yeni sürüm indirilip kurulur, ayarlar korunur. Program kendiliğinden güncelleme aramaz; slayt gösterisi açıkken güncelleme yapılmaz.

### Gereksinimler

- Windows 10 veya 11
- .NET Framework 4.5 veya üzeri (Windows'ta hazır gelir)
- Microsoft PowerPoint (Sunucu Görünümü Modu için)
- İsteğe bağlı: Logitech Spotlight

### Kurulum

1. **Windows ekran ayarları:** Laptop ekranını ana ekran yapın. Üç ekran da "Masaüstünü bu ekrana genişlet" modunda olsun (yansıtma değil).
2. **PowerPoint:** Slayt Gösterisi > Monitör ayarında salon (HDMI) ekranını seçin ("Otomatik" değil) ve "Sunucu Görünümünü Kullan" seçeneğini işaretleyin.
3. **Programı kurun:**
   - [Releases](https://github.com/burkon-teknik/PresenterView-Releases/releases/latest) sayfasından `PresenterView-x.y.z.zip` dosyasını indirin.
   - Zip'i yazma izniniz olan bir klasöre açın, örneğin `Belgeler\PresenterView`. "Program Files" kullanmayın, yoksa güncelleme o klasöre yazamaz.
   - `PresenterView.exe` dosyasını çalıştırın. Windows "bilinmeyen yayımcı" uyarısı verirse **Ek bilgi > Yine de çalıştır** deyin.
4. **Konuşmacı ekranını seçin:** Açılan pencerede her ekranın köşesinde numarası görünür. Konuşmacı ekranını seçip **Tamam** deyin. Seçim kaydedilir.
5. **Otomatik başlatma (isteğe bağlı):** Saatin yanındaki simgeye sağ tıklayıp "Windows açılınca otomatik başlat" seçeneğini açın.

### Sorun çıkarsa

- **"Ekranlar karıştı" uyarısı:** PowerPoint gösteriyi konuşmacı ekranına açmış demektir. Slayt Gösterisi > Monitör ayarından salon ekranını seçin.
- **Konuşmacı ekranında yanlış ekran görünüyor:** Simgeye çift tıklayıp ekranı yeniden seçin. Kablolar başka porta takıldıysa da aynısını yapın.
- **Ayar dosyası:** `%APPDATA%\PresenterView\ayar.txt`. Silerseniz program ekranı yeniden sorar.
- **Hata günlüğü:** `%APPDATA%\PresenterView\hata.log`

---

## English

PresenterView is a Windows system tray application for conference and stage presentations. On a laptop with three displays, it safely mirrors PowerPoint **Presenter View** to a separate screen in front of the speaker (confidence monitor).

> The user interface is in Turkish. Menu and message names are given below in Turkish with an English translation.

### Display layout

| Display | What it shows |
|---|---|
| **Main display** (laptop) | PowerPoint Presenter View opens here. |
| **Audience display** (HDMI) | The slide the audience sees. |
| **Speaker display** (podium) | Only the desktop wallpaper when no slideshow is running; a live copy of Presenter View during the slideshow. The connection port does not matter. |

### Features

- **Presenter View Mode** (for PowerPoint): When the slideshow starts (F5), Presenter View is copied to the speaker display; when it ends (Esc), the speaker display returns to the wallpaper.
  - Nothing you do on the main display (windows, desktop icons, taskbar) ever **leaks** to the speaker display.
  - If another window covers Presenter View, that window is not shown on the speaker display.
  - If the image stops updating for more than 1 second, an orange **"Görüntü güncellenmiyor"** (image not updating) banner appears, so the speaker never mistakes an old slide for the current one.
- **General Mode** (for PDF, Canva, browsers, etc.): Whatever is on the audience display, including the mouse cursor, is cloned to the speaker display.
- Switch between modes with **Alt+O**; the selected mode is remembered.
- **Display protection:** The mouse cannot enter the speaker display, and windows moved there are sent back to the main display.
- **Overlay windows:** The display window of programs such as a conference timer is shown on the speaker display no matter which screen it is on. Their control panels and settings windows are not shown.
- **Logitech Spotlight laser** (no Logitech software required): Hold the top button to show a laser dot on the audience display. In Presenter View Mode the same dot also appears on the slide shown on the speaker display. Color and size are adjustable.
- **Laser only:** With fewer than three displays, the program runs only the Spotlight laser and returns to normal automatically when the third display is connected.
- **Updates:** "Güncellemeleri denetle..." (check for updates) in the tray menu downloads and installs a new version, keeping your settings. The program never checks on its own and never updates during a slideshow.

### Requirements

- Windows 10 or 11
- .NET Framework 4.5 or later (included with Windows)
- Microsoft PowerPoint (for Presenter View Mode)
- Optional: Logitech Spotlight

### Installation

1. **Windows display settings:** Make the laptop screen the main display. Set all three displays to "Extend desktop to this display" (not duplicate).
2. **PowerPoint:** Under Slide Show > Monitor, select the audience (HDMI) display (not "Automatic") and check "Use Presenter View".
3. **Install the program:**
   - Download `PresenterView-x.y.z.zip` from the [Releases](https://github.com/burkon-teknik/PresenterView-Releases/releases/latest) page.
   - Extract it to a folder you can write to, for example `Documents\PresenterView`. Do not use "Program Files", or updates will not be able to write there.
   - Run `PresenterView.exe`. If Windows shows an "unknown publisher" warning, choose **More info > Run anyway**.
4. **Select the speaker display:** A window opens with a number shown in the corner of each display. Select the speaker display and click **Tamam** (OK). The choice is saved.
5. **Start automatically (optional):** Right-click the tray icon and enable "Windows açılınca otomatik başlat" (start with Windows).

### Troubleshooting

- **"Ekranlar karıştı" (displays mixed up) warning:** PowerPoint opened the slideshow on the speaker display. Select the audience display under Slide Show > Monitor.
- **The wrong display is used as the speaker display:** Double-click the tray icon and select the display again. Do the same if cables were moved to other ports.
- **Settings file:** `%APPDATA%\PresenterView\ayar.txt`. Delete it to be asked for the display again.
- **Error log:** `%APPDATA%\PresenterView\hata.log`
