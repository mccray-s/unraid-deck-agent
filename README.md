# Unraid Deck Notification Agent

This is a simple Unraid notification agent plugin for the **Unraid Deck iOS App**. It forwards Unraid system alerts and notices directly to your iPhone.

The plugin converts Unraid events into a JSON payload and pushes it to your phone securely via a Cloudflare Worker, without saving any of your data on third-party servers.

## Features
- **Native Integration**: Works directly in Unraid's `Settings -> Notifications -> Agents`.
- **Zero Dependencies**: Pure Bash script, no Python or other heavy dependencies required.
- **Privacy First**: Direct pass-through of notifications; no data is logged or tracked by our servers.

---

## Installation

1. Open your Unraid Web UI and go to the **Plugins** tab.
2. Select the **Install Plugin** tab.
3. Paste the following URL into the text field:
   ```text
   https://raw.githubusercontent.com/mccray-s/unraid-deck-agent/main/UnraidDeck.plg
   ```
4. Click **Install**.

---

## Configuration

1. **Get your App Token**
   - Open the **Unraid Deck** app on your iPhone.
   - Go to Server Settings where you enabled Push Notifications.
   - Copy your **10-character App Token** (e.g., `0Wfj6ZXxf3`).

2. **Setup the Unraid Agent**
   - In Unraid, go to **Settings** -> **Notification Settings**.
   - Scroll down to the **Agents** section and find **Unraid Deck**.
   - Toggle the switch to **Enable**.
   - Paste your App Token into the field.
   - Click **Apply**.

3. **Test the Connection**
   - Click the **Test** button next to the Unraid Deck agent to verify it works. You should receive a push notification on your iPhone.

---

## Troubleshooting
If you aren't receiving test messages:
- Ensure you have clicked "Apply" after entering your App Token.
- Make sure you have allowed Push Notifications for Unraid Deck in your iOS Settings.

## License
MIT License
