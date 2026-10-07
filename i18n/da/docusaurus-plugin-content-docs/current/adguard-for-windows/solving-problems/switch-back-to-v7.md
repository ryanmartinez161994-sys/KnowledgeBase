---
title: How to switch back to v7 after updating to v8.0
sidebar_position: 14
---

:::info

This article covers AdGuard for Windows, a multifunctional ad blocker that protects your device at the system level. For at se, hvordan den fungerer, [download AdGuard-appen](https://agrd.io/download-kb-adblock)

:::

## How to switch back to v7 after updating to v8.0

AdGuard til Windows v8.0 introducerer væsentlige ændringer. Findes den nye brugerflade ubekvem, eller opleves problemer, kan der skiftes tilbage til version 7.

:::note

If you wish to preserve your settings, it’s recommended that you export them before changing versions. You can then import your saved settings after updating the app. The steps needed to do so are listed below.

:::

1. Efter opgradering til v8, åbn mappen `C:\ProgramData\Adguard\Backups` og lokalisér ZIP-filen med et navn i stil med `adguard_settings_7.22.5008.0-08-04-2025-13_42_15.276.zip`.

2. Kopiér denne ZIP-fil til et sted uden for `C:\ProgramData\Adguard`, f.eks. til skrivebordet. Dette er vigtigt, da mappen renses i næste trin.

3. Afinstallér v8.0 via _Indstillinger_ → _Apps_ → _Installerede apps_. Markér i afinstallationsdialoen afkrydsningsfeltet for at fjerne alle brugerindstillinger og data, så ingen v8-rester efterlades.

   ![Afinstallation \*border](https://cdn.adtidy.org/content/kb/ad_blocker/windows/version_8/solving_problems/uninstall.png)

   :::note

   For trinvis vejledning, se [Sådan afinstalleres AdGuard til Windows](/adguard-for-windows/installation#uninstall).

   :::

4. Installer den foregående version. You can find the download link in the _Assets_ section of the latest stable v7 release on [GitHub](https://github.com/AdguardTeam/AdguardForWindows/releases/tag/v7.22.9).

5. Afslut version 7 fra systembakken for at stoppe filtrering.

6. Udpak indholdet af ZIP-filen fra trin 2, og erstat flg. filer:

   - `adguard.db` → `C:\ProgramData\Adguard` — hovedindstillingsdatabase, inkl. filtre og tilpassede regler
   - `agflm_dns.db` → `C:\ProgramData\Adguard\FLM` — DNS-filterdatabase
   - `agflm_standard.db` → `C:\ProgramData\Adguard\FLM` — standardfilterdatabase

7. Start AdGuard. Version 7 starter med sine tidligere indstillinger gendannet.
