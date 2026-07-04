# **Apex Kernel v2.0 : "The Skirmisher"**
### **Release Date:** July 4, 2026

### **Target Device:** Realme 8i / Narzo 50 (spaced)

### **by:** DΞΞZNUTZ | @daizeuz-dred
---
### 🤝🏻 **Buy me a coffee?**
### Github Sponsor: [**Sponsor**](https://github.com/sponsors/daizeuz-dred)
### Sociabuzz: [**Sponsor**](https://sociabuzz.com/daizeuzdred/tribe)
---

### **🛡️ Security & Root**
* **KernelSU-Next v3 Integration:** Imported KernelSU-Next v3.2.0-legacy-susfs-v2 bundled with SUSFS v2.2.0 for advanced root management.
* **SUSFS Hook Wiring:** Implemented SUSFS hooks across VFS, proc, devpts, and SELinux for stable stealth-root operation.
* **Submodule Sync:** Updated KernelSU-Next submodule pointer to resolve version and UAPI mismatches.
* **Config Enablement:** Enabled KSU, SUSFS, and all related feature flags in `spaced_defconfig`.

### **🌐 Networking**
* **TCP Buffer Tuning:** Increased TCP buffer sizes across the stack for improved network throughput.

### **🧠 Memory Management**
* **Cache & Swap Tuning:** Tuned cache pressure, dirty ratios, and swappiness for smoother multitasking under memory pressure.
* **KSM + Expanded CMA:** Enabled Kernel Samepage Merging and doubled the CMA pool to 32MB for better memory headroom.

### **🔋 Power & PMIC**
* **IRQ Stability Fix:** Added `IRQF_SHARED` to vibrator and regulator overcurrent IRQs to prevent shared-line IRQ conflicts.

### **✋ Touch**
* **IRQ State Tracking:** Fixed unbalanced enable/disable calls in the touchpanel driver by tracking IRQ state explicitly.
* **Screen-Off Gesture Support:** Reworked `oplus_touchscreen` driver to properly support screen-off gestures.

### **🎨 Graphics**
* **DRM Clock Fix:** Resolved an unbalanced `spin_unlock` in the clock-disable path within the DRM driver, preventing lock-state corruption.

---

**Note:** Flash via compatible recovery.
