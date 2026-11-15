# How to Sync Files, Clipboard and Passwords Between Phone and Computer Without a Cloud (2026)

The best pick is Off Grid AI, because one app syncs your files, copied text and AI chats between your phone and computer over your local network, with no account and no server in the middle. Its vault doesn't sync, so pair it with KeePassXC for passwords. If you want a free alternative for files and clipboard, KDE Connect is the one to try, and Syncthing is the free choice for keeping whole folders in sync.

I build Off Grid AI, one of the apps below. I've tried to be fair, and every fact links to its source.

## The tools compared

Checked 15 November 2026 on each tool's own site, docs or GitHub.

| Tool | Does | Phones | Computers | Works over the internet | Price |
|---|---|---|---|---|---|
| [Off Grid AI](https://getoffgridai.co/) | Files, clipboard text, chats and projects | iPhone, Android | Mac (Apple silicon), Windows x64, Linux x64 | No, local network only | Sync needs Pro: one payment of $34.99 right now (regular $119), or $7.99/month |
| KDE Connect / GSConnect | Files, clipboard text, notifications, SMS | Android, iOS (limited) | Linux, Windows, macOS | Same network, or a VPN | Free |
| Syncthing | Keeps whole folders in sync | Community apps (Syncthing-Fork, Möbius Sync) | Windows, macOS, Linux, BSD | Yes, through encrypted relays | Free, MPL-2.0 |
| KeePassXC + a KeePass phone app | Passwords in one encrypted file | KeePassDX (Android), KeePassium or Strongbox (iPhone) | Windows, macOS, Linux | However you move the file | KeePassXC and KeePassDX free; iPhone apps have paid tiers |
| LocalSend | Sends files and text by hand | Android, iOS | Windows, macOS, Linux | No, local Wi-Fi | Free, Apache-2.0 |
| Möbius Sync | Syncthing on iPhone and iPad | iOS | Pairs with any Syncthing device | Yes, via Syncthing | Free up to 20MB, one-time unlock |

## 1. Off Grid AI

You install one app on your phone and one on your computer, pair them once, and your files, copied text and AI chats show up on both without an account or a cloud. [Off Grid AI](https://getoffgridai.co) is a local AI app for iPhone, Android, Mac, Windows and Linux. With Pro you pair by scanning a QR code or typing a code, and after that your conversations, projects, files and copied text sync over your local network, encrypted. The computer keeps a searchable clipboard history. On Android, select the text and choose **Copy to Off Grid AI** to send it, because the system blocks apps from reading the clipboard in the background.

The same Pro payment also covers meetings without a bot, dictation into any app, memory and the local AI itself.

**The limit.** It doesn't sync passwords. The Vault stays on the one computer where you made it, and the phone app has no vault, so pair Off Grid AI with KeePassXC for passwords. It only syncs when both devices are on the same network, so nothing moves while you're out. Pro is one payment of $34.99 right now (regular $119) or $7.99 a month for up to 5 devices. The [devices page](https://getoffgridai.co/features/devices-and-privacy/) has the details.

**Pick it if** you want files, clipboard and your chats in one app on your phone and computer, with nothing stored on anyone's server.

## 2. KDE Connect or GSConnect

[KDE Connect](https://kdeconnect.kde.org/) links your phone and computer for file sharing, clipboard text, phone notifications on the desktop and SMS from the computer. Its [download page](https://kdeconnect.kde.org/download.html) lists Linux, Windows, macOS, Android and iOS. On GNOME, install [GSConnect](https://extensions.gnome.org/extension/1319/gsconnect/) instead, a separate implementation of the same protocol that won't work with KDE Connect installed at the same time.

**The limit.** The [user guide](https://userbase.kde.org/KDE_Connect) says the clipboard carries text only, never images. Android 10 and later block background clipboard reads, so you tap **Send Clipboard** in the notification. On iPhone there's no notification sync, no SMS and no background connection, and clipboard only goes from phone to computer when you tap to push it. Both devices need the same network, with ports 1714 to 1764 open.

**Pick it if** you live on Linux and Android and want texts, notifications and copied text on the computer for free.

## 3. Syncthing

[Syncthing](https://syncthing.net/) keeps folders identical across your devices, all the time. Its site says "There is no central server that might be compromised", all traffic uses TLS, and it works over your home network and over the internet. When two devices can't reach each other directly, public [relays](https://docs.syncthing.net/users/relaying.html) pass the data along still encrypted end to end, though a relay sees your IP address, device ID and how much data moves. The code is on [GitHub](https://github.com/syncthing/syncthing) under MPL-2.0.

**The limit.** The official Android app is gone. Its [repository](https://github.com/syncthing/syncthing-android) says "This app is discontinued" and was archived on 3 December 2024. On Android, use [Syncthing-Fork](https://f-droid.org/en/packages/com.github.catfriend1.syncthingfork/) from F-Droid, a community app last updated 25 October 2026. Syncthing doesn't share your clipboard.

**Pick it if** you want photos, documents or a password file to follow you without pressing send, even away from home.

## 4. KeePassXC with a phone app for passwords

[KeePassXC](https://keepassxc.org/) is a free, GPLv3 password manager for Windows, macOS and Linux, and its site says "no data is stored on remote servers". Everything sits in a single encrypted .kdbx database that you can put anywhere. Its [docs](https://keepassxc.org/docs/) say there's no KeePassXC mobile app and point you to [KeePassDX](https://github.com/Kunzisoft/KeePassDX) or KeePass2Android on Android and to [KeePassium](https://keepassium.com/) or [Strongbox](https://strongboxsafe.com/) on iPhone. KeePassDX is free and GPLv3. KeePassium's free plan covers one database, with Premium at €19.99 a year or Pro at €79.99 once, and Strongbox has a paid Pro tier.

**The limit.** KeePassXC has no sync of its own, and its docs suggest a shared cloud folder. Put the file in a Syncthing folder instead and you skip the cloud. If you change the database on the phone and the computer before they sync, Syncthing [keeps both versions](https://docs.syncthing.net/users/syncing.html) and you merge them by hand, so make changes in one place at a time.

**Pick it if** you need passwords on your phone without any company holding them.

## 5. LocalSend

[LocalSend](https://localsend.org/) sends files and text to nearby devices over your Wi-Fi with no account. Its site says it "Works completely offline" and uses HTTPS with end-to-end encryption. It runs on Windows, macOS, Linux, Android and iOS, and it's free under Apache-2.0.

**The limit.** You send every transfer by hand. Nothing stays in sync, and it doesn't handle passwords.

**Pick it if** you move a file now and then and don't want anything running in the background.

## 6. Möbius Sync

[Möbius Sync](https://mobiussync.com/) is a third-party iOS app that brings Syncthing to iPhone and iPad. Its [FAQ](https://mobiussync.com/faq/) says the free version syncs up to 20MB, and a one-time in-app purchase removes the limit.

**The limit.** iOS doesn't let apps run in the background for long. The FAQ says sync can take up to 24 hours to settle in, and after that you can expect roughly one to two hours of sync activity a day, so open the app when you need a file now.

**Pick it if** you have an iPhone and want it in your Syncthing setup, including for a KeePass file.

## How to choose

If you want one app for files, clipboard and chats on both phone platforms, use Off Grid AI and add KeePassXC for passwords.

If you'd rather stay free, split the job. Copied text and the odd photo go through KDE Connect, GSConnect or LocalSend. Folders that change often belong in Syncthing, with Syncthing-Fork on Android or Möbius Sync on iPhone. Passwords belong in KeePassXC, synced as a file.

On iPhone, the free tools get harder. KDE Connect's clipboard only goes one way there, and Möbius Sync runs when iOS lets it.

## FAQ

### What is the best way to sync files and clipboard between phone and computer without a cloud?

Off Grid AI. You pair your phone and computer once, and files, copied text and chats sync over your local network with no account. KDE Connect is the free alternative.

### How do I sync whole folders between my phone and computer for free?

Syncthing. It keeps folders in sync device to device with no central server. Use Syncthing-Fork on Android and Möbius Sync on iPhone, since the official Android app was discontinued in December 2024.

### How do I sync KeePass passwords to my phone without a cloud?

Keep the .kdbx file from KeePassXC in a Syncthing folder, sync it to your phone, and open it in KeePassDX on Android or KeePassium or Strongbox on iPhone.

### Does Off Grid AI sync passwords?

No. Its Vault stays on one computer and the phone app has no vault, so use KeePassXC for passwords. Off Grid AI syncs conversations, projects, files and clipboard text between paired devices.

### Does Syncthing send my files through someone else's server?

Only when your devices can't connect directly. Then a relay forwards the traffic, still encrypted end to end, and sees your IP address and how much data moves, never the files.

*Also on [dev.to](https://dev.to/alichherawalla/how-to-sync-files-clipboard-and-passwords-between-phone-and-computer-without-a-cloud-2026-26ff).*
