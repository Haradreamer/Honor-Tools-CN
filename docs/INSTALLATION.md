# Installation and ADB connection / Установка и подключение ADB

## English

### 1. Prepare the device

1. On your HONOR phone, enable **Developer options** (the menu location may differ by MagicOS version).
2. Enable **USB debugging** in Developer options.
3. Connect the phone to Windows with a USB cable that supports data transfer.
4. Unlock the phone and accept the **Allow USB debugging?** prompt for this computer.

### 2. Check the connection

If the utility cannot detect the phone, use a terminal with the Android platform-tools installed:

```cmd
adb devices
```

Typical outcomes:

- `device`: ADB recognizes the authorized phone.
- `unauthorized`: Unlock the phone and accept the debugging permission prompt. If no prompt appears, revoke USB debugging authorizations on the phone, then reconnect.
- Empty device list: Try a different USB data cable, port or Windows ADB driver. Make sure the phone is not in charge-only mode if your device requires selecting a data mode.
- `offline`: Disconnect/reconnect, restart the ADB server, and reauthorize.

If needed:

```cmd
adb kill-server
adb start-server
adb devices
```

Close other Android tools that may be using ADB, and confirm you have selected the intended device if multiple devices or emulators are connected. For multiple devices, use `adb -s <serial> ...`; do not run package-changing commands without checking the target serial number.

### 3. Wireless debugging

Wireless ADB setup varies by Android/MagicOS version. Ensure the phone and PC are reachable over the same trusted network; use the pairing and connection steps appropriate to the phone. Do not expose the ADB port to the public internet.

### 4. Troubleshooting

**Windows shows a storage device but not ADB:** USB debugging and file-transfer detection are separate. Check the phone's authorization dialog, its ADB interface in Device Manager, and the Windows driver.

**No authorization prompt:** Revoke USB debugging authorizations, toggle debugging off/on, unlock the phone and reconnect.

**Connection drops:** Replace the cable, switch USB port, disable conflicting ADB servers and try again.

**A package was disabled accidentally:** Restore it using the utility's restore feature where available, or seek model-specific guidance before changing more packages.

## Русский

1. На HONOR откройте настройки разработчика и включите **«Отладка по USB»**.
2. Подключите телефон исправным кабелем передачи данных к компьютеру.
3. Разблокируйте экран и подтвердите запрос **«Разрешить отладку по USB»**.
4. При проблемах выполните в Windows команду `adb devices`.

Что означают результаты:
- **`device`** — связь установлена.
- **`unauthorized`** — разрешение не подтверждено на телефоне. Отзовите разрешения отладки, переподключитесь и подтвердите запрос.
- **Пустой список** — проверьте USB-кабель, порт, драйвер ADB и режим подключения.
- **`offline`** — перезапустите сервер ADB: `adb kill-server`, затем `adb start-server`.

Не вводите команды, изменяющие пакеты, пока не убедитесь в правильном подключённом устройстве. Не открывайте доступ к беспроводному ADB из интернета.

Полезные данные для отчёта об ошибке: модель телефона, версия MagicOS, Windows, версия инструмента, подключение USB/Wi-Fi, текст `adb devices` (серийный номер закройте) и сообщение об ошибке.
