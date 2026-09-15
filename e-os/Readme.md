#e/os installation instructions

## 📥 Downloads

| Component | Description | File Type | Download Link |
| :--- | :--- | :--- | :--- |
| **/e/OS ROM** | Operating system installation package | `.zip` | [Download /e/OS](https://github.com/Android-Ports-Archive/Android-Ports-Sapphire-/releases/download/e%2Fos/e-4.2-a16-20260915-unofficial-sapphire.zip) |
| **/e/OS Recovery** | Custom recovery partition image | `.img` | [Download Recovery](https://github.com/Android-Ports-Archive/Android-Ports-Sapphire-/releases/download/e%2Fos/recovery.img) |


```markdown
# How to Install /e/OS


Connect your device to your PC via USB.

On the computer, open a command prompt (on Windows) or terminal (on Linux or macOS) window, and type:

```bash
adb reboot bootloader

```

Once the device is in fastboot mode, verify your PC finds it by typing:

```bash
fastboot devices

```

---

## Flash a recovery image onto your device

```bash
fastboot flash boot recoveryfilename.img

```

> **Note:** Replace `recoveryfilename` with the name of the recovery image you downloaded in the previous section.

---

## Manually reboot into recovery mode

1. With the device powered off.
2. Hold **Volume Up + Power**.
3. Then select **recovery** from bootloader using the hardware keys.

---

## Steps to install /e/OS from recovery

Use **Volume** to navigate and **Power** to select — to go back to the main screen, use **Volume Up** to choose the arrow at the top.

> **Tip:** If your PC can’t detect the device over adb, tap **Advanced » Enable adb** from the /e/OS recovery main screen.

---

### Format the device

On /e/OS Recovery main screen:

1. Select **Factory reset**
2. Select **Format data / Factory reset** option
3. Next screen will display a warning that this action cannot be undone
4. Select **Format data** to proceed or **Cancel** if you want to go back

If you selected **Format data**, the format process will complete.

You’ll see text in small font on the lower left side of the screen showing format progress, similar to this:

```text
Wiping data...
Formatting /data...
Formatting /cache...
Data wipe complete.

```

Display will now return to the **Factory Reset** screen.

---

### Install /e/OS

In /e/OS recovery main screen:

1. Select **Apply Update** and in next screen **Apply update from adb**.
2. In the next screen, the device is now in sideload mode.

> **Note:** At this point the **Cancel** option is highlighted that does not mean you have canceled the action. The device is in adb sideload mode.

On your PC begin adb sideload. Type the below command in a console:

```bash
adb sideload downloaded_file_name.zip

```

> **Note:** Replace `downloaded_file_name.zip` with the name of the /e/OS file you downloaded in the previous section.

1. Press enter key on the keyboard to start the sideloading.
2. The screen will show the progress percentage… This might pause at **47%**. Give it some time.
3. The PC console will now display:
```text
Total xfer: 1.00x

```


4. The phone screen will now display some text with a message similar to:
```text
Script succeeded result was [1.000000]

```



This means that the install was successful.

---

### Reboot the device

In /e/OS recovery main screen:

1. Select **Reboot system now**
2. The reboot process may take **5 - 10 minutes**

---

> [!NOTE]
> **Success:** Congratulations! Your phone should now be booting into /e/OS.

```

```
