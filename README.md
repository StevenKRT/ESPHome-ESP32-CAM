# ESP32-CAM mit ESPHome und Home Assistant

Dieses Repository enthält eine vollständige ESPHome-Konfiguration für eine ESP32-CAM (AI-Thinker kompatibel), integriert in Home Assistant über die native ESPHome-API.

---

## Funktionen

- Kamera-Streaming über ESP32-CAM
- MJPEG-Webstream über integrierten Webserver
- Integration in Home Assistant
- Schaltbare Blitz-LED
- WLAN-Signalstärke als Sensor
- Uptime-Sensor
- Gerätestatus als Binary Sensor
- OTA-Updates
- Fallback-Access-Point bei WLAN-Ausfall
- Automatischer Neustart bei Verbindungsverlust
- Zyklischer Watchdog-Log

---

## Hardware

- ESP32-CAM (AI-Thinker)
- OV2640 Kamera
- USB-TTL-Adapter (für Erstflash)
- 5 V Stromversorgung (mind. 1 A empfohlen)

AliExpress:
[ESP32-CAM WiFi-Modul 2,4 G Antenne ESP32 Seriell zu WiFi ESP32 CAM Entwicklungsboard 5 V Bluetooth mit OV2640 Kameramodul DIY](https://s.click.aliexpress.com/e/_Ey4DMXm)

3D-Druck:
[ESP32 Cam Gehäuse Kit - Steckverbindung - Kugelgelenk](https://makerworld.com/de/models/1220385-esp32-cam-case-kit-snap-fit-ball-joint#profileId-1497626)

---

## Technische Parameter

| Parameter        | Wert        |
|------------------|-------------|
| Auflösung        | 1600x1200   |
| JPEG-Qualität    | 10          |
| Max. Framerate   | 3 FPS       |
| PSRAM            | Quad / 80 MHz |
| Weißabgleich     | AUTO        |
| Belichtung       | AUTO        |
| Gain Control     | AUTO        |
| Stream-Port      | 8080        |

---

## GPIO-Belegung (AI-Thinker)

| Funktion          | GPIO |
|------------------|------|
| XCLK             | GPIO0 |
| SDA              | GPIO26 |
| SCL              | GPIO27 |
| D0–D7            | GPIO5, GPIO18, GPIO19, GPIO21, GPIO36, GPIO39, GPIO34, GPIO35 |
| VSYNC            | GPIO25 |
| HREF             | GPIO23 |
| PCLK             | GPIO22 |
| Power Down       | GPIO32 |
| Blitz-LED        | GPIO4 |

---

## Home-Assistant-Entitäten

- Kamera
- Licht (Blitz)
- WLAN-Signalstärke
- Uptime
- Status
- Neustart-Button

---

## Netzwerkverhalten

- WLAN mit Fallback-Access-Point
- Neustart nach 60 Sekunden WLAN-Trennung
- OTA-Update-Unterstützung
- Verschlüsselte ESPHome-API

---

## Flash-Hinweis

Erstflash:
- GPIO0 auf GND
- Flashen
- Neustart ohne GPIO0-Brücke

Danach sind OTA-Updates möglich.

---

## Dateien

- `espcam1.yaml` – ESPHome-Konfiguration

---

## Lizenz

Freie Nutzung. Keine Gewährleistung.
