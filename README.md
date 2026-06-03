# Sharpa Pilot

 Sharpa Pilot is the official application for device configuration, monitoring, firmware updates, and routine operations.

---

## 📥 Download

Download the latest `.deb` package from Releases:

👉 https://github.com/sharpa-robotics/sharpa-pilot/releases

---

## 🚀 Installation (Ubuntu)

Install the package using:

```bash
sudo dpkg -i sharpa-pilot-<version>.deb
```

If there are missing dependencies, run:

```bash
sudo apt-get install -f
```

---

## ▶️ Run

After installation, you can launch the application:

```bash
sharpa-pilot
```

Or find it in your application menu.

---

## 📦 SDK (Linux)

Sharpa Pilot ships with a **matched Sharpa Wave SDK** and manages it automatically.

### Do not override the SDK used by Pilot

- **Do not** install, upgrade, or replace `sharpa-wave-sdk` on your own.
- **Do not** copy or edit files under `/opt/sharpa-wave-sdk/` or `/opt/sharpa-pilot/pilot_sdk` (binaries, `config.yaml`, libraries, etc.) expecting Pilot to keep using your changes.

To change the SDK version that Pilot uses, **only upgrade or reinstall `sharpa-pilot`** (same `.deb` workflow as in [Update](#-update)). That is the supported path.

### Where files live (reference)

After `sharpa-pilot` installed, typical layout:

| Item | Path |
|------|------|
| Pilot application | `/opt/sharpa-pilot/` |
| Wave SDK root (what Pilot prefers) | `/opt/sharpa-wave-sdk/` |
| `pilot_sdk` service binary | `/opt/sharpa-wave-sdk/pilot_sdk`, with a copy at `/opt/sharpa-pilot/pilot_sdk` |

Under `/opt/sharpa-wave-sdk/` you may see `pilot_sdk`, `config.yaml`, `VERSION`, `lib/`, `python/`, `include/`, `sample/`. Treat these as **managed by the Pilot installer**, not as a user-editable SDK install.

### Uninstall

Removing `sharpa-pilot` also removes `/opt/sharpa-wave-sdk` and the `sharpa-wave-sdk` package. That is expected; reinstall `sharpa-pilot` if you need Pilot and its SDK again.

---

## 🔄 Update

To upgrade to a newer version:

```bash
sudo dpkg -i sharpa-pilot-<new-version>.deb
```

---

## ❌ Uninstall

To remove the application:

```bash
sudo dpkg -r sharpa-pilot
```

---

## ⚠️ Requirements

- Ubuntu 20.04 / 22.04
- x86_64 architecture

---

## 📌 Notes

- This is an internal tool for Sharpa Robotics
- Make sure the device is properly connected before running

---

## 📞 Support

For issues or questions, please contact the Sharpa Robotics development team.
