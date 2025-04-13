# InsiderTweak

![Screenshot of InsiderTweak](https://i.imgur.com/YTtU1to.png)

## Description

**InsiderTweak** is a simple Windows Command Prompt script designed to enable access to the Windows Insider Program without requiring you to sign in with a Microsoft Account or submit any enrollment request. It is ideal for users who prefer not to leave personal data or go through the hassle of filling out a request—even if you already have a Microsoft Account.

This script is compatible only with Windows 11 or Windows 10 version 1809 and later.

Additionally, this fork includes new features such as fast Insider-Preview update checking and integrated multilingual support (English, Russian, Simplified Chinese). Use the links at the bottom to switch between languages.

## Usage

This script requires administrative privileges to run. To start, simply right-click the script and choose **`Run as Administrator`**.

### Installation and Configuration

Upon launching the script, you will be presented with a selection of Windows Insider Program channels:
- **Canary Channel**
- **Dev Channel**
- **Beta Channel**
- **Release Preview Channel**

Choose the option corresponding to your desired channel by pressing the appropriate key and then **ENTER**.

If your machine was not previously enrolled in the Insider Program, you will be prompted to restart your computer in order to enable *Microsoft Flight Signing*, which is required for full participation in the Windows Insider Program.

**Note:**  
The Windows Insider Program requires your telemetry settings to be set to **Full**. After enrolling, please verify that your diagnostic data collection settings are configured to **Full**, as some Insider Preview builds may not be offered via Windows Update otherwise. You can verify or modify these settings as follows:

- **Windows 11**: *Settings* > *Privacy and Security* > *Diagnostics & feedback*
- **Windows 10**: *Settings* > *Privacy* > *Diagnostics & Feedback*

### Restoring Default Windows Insider Program Settings

To restore the Windows Insider Program to its default configuration, simply choose the option to **Stop receiving Insider Preview builds** within the script. You will be prompted to reboot, as this process disables *Microsoft Flight Signing*.

## How Does It Work?

The script leverages undocumented registry settings—specifically the `TestFlags` value—to disable access to online Windows Insider services. When `TestFlags` is set to `0x20`, all online contact is effectively blocked. This allows the script to configure Insider Preview settings locally in the registry without interference from Microsoft's online services. As Windows Update does not verify whether a machine is enrolled in the program, simply setting the correct registry values is enough to receive Insider Preview builds.

## Translations

Switch between languages by using the links below:

- [English](#english)
- [Русский](#русский)
- [简体中文](#简体中文)

### English
<a name="english"></a>
InsiderTweak is your offline solution for joining the Windows Insider Program, ideal for those who do not wish to use a Microsoft Account or submit a participation request. Benefit from fast Insider-Preview update checking and a user-friendly, multilingual interface that keeps you in control of your system’s update experience.

### Русский
<a name="русский"></a>
**InsiderTweak** — это ваш автономный инструмент для участия в программе Windows Insider, предназначенный для пользователей, которые не хотят использовать учётную запись Microsoft или оставлять заявку на участие. Программа также обеспечивает быструю проверку обновлений Insider-Preview и удобный многоязычный интерфейс, позволяющий полностью контролировать процесс обновления системы.

### 简体中文
<a name="简体中文"></a>
**InsiderTweak** 是一款离线加入 Windows Insider 计划的解决方案，非常适合那些不希望使用 Microsoft 帐户或提交参与申请的用户。该工具还支持快速检查 Insider-Preview 更新，并提供用户友好的多语言界面，让您轻松掌控系统更新体验。

## License

This project is licensed under the [MIT License](LICENSE).

---

*This fork reflects our shared vision to empower users with enhanced control over their system updates and privacy—without the need to compromise by submitting personal data or filling out lengthy enrollment requests. Enjoy a more flexible and privacy-respecting Insider experience on your terms!*
