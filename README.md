# EV Scooter & E-Bike Tracker (NWOW WSP Tracker)

A standalone, local-first digital odometer, GPS speedometer, route recorder, multi-chemistry battery monitor (Lead-Acid, Lithium-Ion NMC, and LiFePO4), charging advisor, and maintenance tracker built for electric scooter and e-bike riders.

Developed by **Jestopher F. Quirino**.

---

## Download (Android APK)

Download the latest Android APK directly from the **Releases** section:

- **Latest Release**: `v2.2.0` (see the **Releases** tab on the right sidebar, or `/releases/latest`)
- **APK SHA-256 Checksum (`v2.2.0`)**:
  ```text
  63B102E9EC4E10168E6D3DE2464E17D07FF701C5E482F658B2D0C68C0D85B169
  ```

### Installing on Android
1. Download the `.apk` file from **Releases > Assets**.
2. Open the downloaded file on your Android phone.
3. If prompted, enable **Install unknown apps** for your browser or file manager.
4. Tap **Install**, open the app, and allow **Location (GPS)** access when starting your first trip.

---

## Key Features

### GPS Speedometer, Odometer & Handlebar Ride Mode
- **Smooth 1 Hz GPS Speedometer**: Critically-damped interpolation with 3-sample median speed filtering, hardware GPS speed primary reading, and automatic distance/time fallback.
- **Accumulated Odometer + Trip A / Trip B**: Lifetime GPS odometer (Haversine distance with drift, poor-accuracy, and spike filters) plus two independent resettable sub-odometers.
- **Zero-Scroll Handlebar Ride Mode**: Dedicated landscape and portrait cockpit view with in-cluster Trip ODO, live Est. Remaining Range, Incline/Slope (%), Elevation Gain, Avg/Max Speed, Elapsed time, live compass heading, and a compact lower-right live map.
- **Offline Ready (Hide Live Map)**: 1-tap **Hide Map** mode removes map tile usage while riding offline while continuing to record all GPS coordinates and telemetry locally.
- **Auto-Pause & Auto-Resume**: Optional stationary auto-pause (30s, 45s, 60s, or 2 min) that resumes automatically when movement is detected.
- **EV Audio Chimes & Haptics**: Synthesized Web Audio startup, lower standby ready chime until moving, pause/resume, shutdown, GPS drop warning, and 6-second milestone chimes at 30, 40, 50+ km/h with synchronized speedometer flashes and Android vibration.

### Multi-Chemistry Battery Monitor & Charging Advisor
- **Lead-Acid & Lithium Support**: Presets and OCV curves for EV Deep-Cycle SLA (6-DZF), AGM, Gel, Flooded, Lithium-Ion NMC/NCA (36V to 72V), and LiFePO4 (48V to 72V), plus custom vehicle branding and optional Observed Full Resting Voltage calibration.
- **Two-Stage Charging Advisor**: Estimates realistic CC Bulk + CV Absorption charging duration ranges and completion windows based on your battery bank, charger current, and resting voltage.
- **Estimated Remaining Range**: Live active-trip countdown and Dashboard range estimates derived from your own historical `km/V` trips (unlocks after 2+ recorded trips with voltage data).
- **Electricity Cost & Battery Health**: Track estimated kWh spend (total, 30-day, per-km, per-charge), equivalent full charge cycles, and baseline `V/km` draw trends.
- **Odometer-Based Maintenance Log**: Track tire pressure, brake pads, battery terminals, equalization charges, or custom intervals with automatic Dashboard due-soon and overdue banners.

### Trip History, Tags & Exports
- **Ride Tags & Comparison**: Tag trips (`Commute`, `Errand`, `Long Ride`, `Passenger`, `Hills`, `Rain`) and filter Trip History to compare average distance, speed, and `V/km`.
- **Exports & Backup**: Export routes as **GPX 1.1** (with `<ele>` elevation tags), **CSV** (trips and charging logs), **Shareable PNG Ride Summary Cards** (`1080x1350`), and complete validated **JSON Backup / Restore**.
- **Privacy First**: 100% local on-device storage (IndexedDB). No account, login, telemetry tracking, or cloud server required.

---

## Permissions & External Services
- **Location (GPS)**: Required only while tracking trips to measure speed, distance, route, heading, and elevation.
- **Map Tiles & Routing (Optional)**: Uses OpenStreetMap tiles (Leaflet) for route maps and OSRM for optional secondary road route estimates when online. Core tracking, speedometer, battery monitoring, and storage work completely offline.

---

## Safety & Accuracy Disclaimer
- GPS speed, elevation, incline, estimated remaining range, charging time, and battery SOC are monitoring estimates for reference only and do not replace calibrated vehicle instruments or manufacturer charger limits.
- Operate controls only while parked and keep your eyes on the road while riding.
- Stop charging immediately and seek professional inspection if your battery shows abnormal heating, swelling, odor, leakage, or casing damage.

---

## Author
Built by **Jestopher F. Quirino**.
