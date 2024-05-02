## Telegram Messenger For Android

[Telegram](https://telegram.org) is a messaging app with a focus on speed and security. It’s super fast, simple and free.
This repo contains the official source code for [Telegram App for Android](https://play.google.com/store/apps/details?id=org.telegram.messenger).

## Creating Your Telegram Application

We welcome all developers to use our API and source code to create applications on our platform.
There are several things we require from **all developers**.

1. [**Obtain your own api_id**](https://core.telegram.org/api/obtaining_api_id) for your application.
2. **Do not** use the name Telegram for your app. Or make sure your users understand that it is unofficial.
3. **Do not** use our standard logo (white paper plane in a blue circle) as your app's logo.
3. Study our [**security guidelines**](https://core.telegram.org/mtproto/security_guidelines) and take care of the data and privacy of your users.
4. Remember to publish **your** code in order to comply with the licences.

### API, Protocol Documentation

[Telegram API manuals](https://core.telegram.org/api)

[MTproto protocol manuals](https://core.telegram.org/mtproto)

### Compilation Guide

**Note**: In order to support [reproducible builds](https://core.telegram.org/reproducible-builds), this repo contains dummy release.keystore,  google-services.json, and filled variables inside BuildVars.java. Before publishing your own APKs, please make sure to replace all these files with your own.

You will need Android Studio 3.4, Android NDK rev. 20 and Android SDK 8.1

1. Download the Telegram source code from [GitHub](https://github.com/DrKLO/Telegram): `git clone https://github.com/DrKLO/Telegram.git`
2. Copy your release.keystore into TMessagesProj/config
3. Fill out RELEASE_KEY_PASSWORD, RELEASE_KEY_ALIAS, RELEASE_STORE_PASSWORD in gradle.properties to access your release.keystore
4. Go to [Firebase](https://console.firebase.google.com/), create two android apps with the application IDs "org.telegram.messenger" and "org.telegram.messenger.beta", turn on Firebase messaging, and download google-services.json which should be copied to the same folder as TMessagesProj.
5. Open the project in the Studio. **Note:** It should be opened, NOT imported.
6. Fill out values in TMessagesProj/src/main/java/org/telegram/messenger/BuildVars.java. There’s a link for each of the variables showing where and which data to obtain.
7. You are ready to compile Telegram.

### Localization

We moved all [translations](https://translations.telegram.org/en/android/).

### Frequently Asked Questions (FAQs)

**Note**: If you have questions you would like us to answer, please let us know by opening a GitHub issue detailing your problem.

1. **How can I obtain an api_id for my Telegram application?**<br/>
To obtain an api_id for your Telegram application, please visit the official [Telegram API documentation](https://core.telegram.org/) for detailed instructions. You'll need to register your application and obtain the necessary credentials to access the Telegram API.

2. **Can I use the Telegram name or logo for my unofficial app?**<br/>
No, we kindly request that developers refrain from using the name "Telegram" for their unofficial applications. If you're developing an unofficial app, please ensure that your users understand that it is not affiliated with or endorsed by Telegram. Additionally, avoid using the standard Telegram logo as your app's logo to maintain clarity regarding its unofficial status.

3. **What security measures should I consider when developing with the Telegram API?**<br/>
Security is key when developing applications that handle user data. We highly recommend familiarizing yourself with our security guidelines to ensure that your application adequately protects users' data and privacy. Additionally, always implement secure coding practices and encryption mechanisms to safeguard sensitive information transmitted through your app.

4. **How do I contribute translations to the Telegram Android app?**<br/>
We've centralized all translations for the Telegram Android app on our [translation platform](https://translations.telegram.org/en/android/). If you're interested in contributing translations, simply visit the platform, select your language, and start translating the provided strings.

5. **Can I customize the Telegram app for my specific use case or audience?**<br/>
Yes, you're welcome to customize the Telegram app to suit your specific requirements or audience. However, please note that any modifications should comply with our licensing terms, and we encourage you to publish your modified code as per the requirements outlined in the licenses. Additionally, ensure that your customizations adhere to our branding guidelines and respect users' privacy and security.
