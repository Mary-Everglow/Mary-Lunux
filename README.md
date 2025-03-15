# **Mary Linux**  
**Full Linux distribution for jailbroken iPhones & iPads**  

Mary Linux is a custom Linux OS designed to run on jailbroken iPhones and iPads. It uses the **Ubuntu Linux kernel**, **PongoOS**, and **checkra1n** to boot, providing a full touchscreen Linux experience.  

---

## **⚠ WARNING**  
**Installing Mary Linux will:**  
❌ **Erase all data** on the device (full storage wipe)  
❌ **Prevent future iOS updates** (Apple will no longer support the device)  
❌ **Void your Apple warranty** (Apple will not repair or replace your device)  
❌ **Remove Apple features** (Face ID, iCloud, App Store, iMessage, and other Apple services will no longer work)  
❌ **Require a jailbroken device** (Mary Linux can only be installed on jailbroken iPhones/iPads)  

🔴 **Proceed at your own risk! Once installed, there is no easy way back to iOS!**  

---

## **Features**  
✔ Custom Ubuntu ARM64 kernel optimized for Apple devices  
✔ Uses **PongoOS** for booting  
✔ Full **touchscreen support** for mobile usability  
✔ Command-line access with full Linux capabilities  
✔ **Future**: KDE Plasma Mobile for a full GUI experience  

---

## **Installation**  

### **Requirements:**  
- Jailbroken iPhone/iPad (checkra1n-supported devices)  
- A **Linux PC** (Ubuntu recommended)  
- Basic knowledge of SSH & terminal commands  

### **1. Clone the Repository**  
```bash
git clone https://github.com/YOUR_USERNAME/mary-linux.git
cd mary-linux
```

### **2. Build the Kernel & Root Filesystem**  
```bash
chmod +x scripts/build-mary-linux.sh
./scripts/build-mary-linux.sh
```

### **3. Transfer Files to iPhone/iPad**  
Replace `YOUR_DEVICE_IP` with your actual device’s IP:  
```bash
scp output/kernel.img output/initramfs.img root@YOUR_DEVICE_IP:/var/root/
```

### **4. Boot Mary Linux**  
SSH into your device and start PongoOS:  
```bash
ssh root@YOUR_DEVICE_IP
pongoOS -k /var/root/kernel.img -i /var/root/initramfs.img
```

---

## **Contributing**  
Want to help improve Mary Linux?  
- Report issues via GitHub Issues  
- Fork the project and submit pull requests  
- Suggest features & improvements  

---

## **License**  
Mary Linux is open-source under the **MIT License**.
