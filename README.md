# Unraid Deck Notification Agent

A lightweight, native Unraid notification agent plugin designed explicitly for the **Unraid Deck iOS App**. This plugin bridges the gap between your Unraid server's built-in alert system and your iPhone, forwarding system notices, warnings, and alerts directly to your mobile device via secure Apple Push Notification service (APNs).

Unlike generic messengers, this agent is purpose-built to send structured JSON payloads directly to Unraid Deck's Cloudflare-powered push gateway, ensuring zero external dependencies and prioritizing your privacy.

## ✨ Features
- **Native Unraid Integration**: Integrates directly into Unraid's `Settings -> Notifications -> Agents` panel.
- **Real-time Push**: Delivers push notifications instantly over Apple's APNs infrastructure.
- **Privacy First**: Uses anonymized Device & Server Tokens. Message contents are securely forwarded through a stateless Cloudflare Worker, with nothing saved or tracked.
- **Adaptive Importance**: Translates Unraid's severity levels (Normal, Warning, Alert) to the app.

---

## 🚀 Installation

Install the plugin directly inside your Unraid Web Interface:

1. Open your Unraid Web UI and navigate to the **Plugins** tab.
2. Click on the **Install Plugin** tab.
3. Paste the following URL into the text field:
   ```text
   https://raw.githubusercontent.com/mccray-s/unraid-deck-agent/main/UnraidDeck.plg
   ```
4. Click **Install**. The plugin will automatically download and set up the necessary scripts.

---

## ⚙️ Configuration

1. **Get your Webhook Token from the App**
   - Open the **Unraid Deck** app on your iPhone.
   - Go to the Server Settings where you enabled Push Notifications.
   - Find and copy your unique **10-character Webhook Token** (e.g., `0Wfj6ZXxf3`).

2. **Setup the Unraid Agent**
   - Head back to your Unraid Web UI.
   - Go to **Settings** -> **Notification Settings**.
   - Scroll down to the **Agents** section and find **Unraid Deck**.
   - Toggle the agent on to **Enable**.
   - Paste your 10-character Webhook Token into the designated field.
   - Click **Apply** at the bottom of the page.

3. **Test the Connection**
   - While still on the Notification Settings page, click the **Test** button next to the Unraid Deck agent.
   - You should receive a popup banner on your iPhone confirming the setup!

---

## 🛠 Troubleshooting
If you aren't receiving test messages:
- Ensure you have pressed "Apply" after entering your Webhook Token and enabling the agent.
- Make sure Push Notifications are fully allowed inside iOS Settings for the Unraid Deck app.
- Check the Unraid **System Log** via the window icon at the top right of your Unraid UI. Look for labels prefixed with `UnraidDeckAgent` to see HTTP response codes and potential errors.

## 📄 License
MIT License
