# LMX RPC

[![Download LMX RPC](https://img.shields.io/badge/Download-LMX%20RPC-963ac2?style=for-the-badge&logo=windows&logoColor=white)](https://losemyxelf.xyz/download/LMX%20RPC.rar)

**[Download LMX RPC from the LoseMyXelf homepage](https://losemyxelf.xyz/download/LMX%20RPC.rar)** · [Visit LoseMyXelf Service](https://losemyxelf.xyz)

## License and use restrictions

LMX RPC is distributed as a compiled application; its source code is not included. The program is provided for personal use. Without prior written permission from LoseMyXelf, do not reverse engineer, decompile, disassemble, modify, or create derivative works from the program, and do not redistribute or rehost the program or any modified version. This README does not grant rights to the software or its source code. Any rights that cannot be restricted under applicable law remain unaffected.

LMX RPC lets you publish a custom Discord Rich Presence from the Discord desktop client. You choose the activity text, artwork, and optional buttons. Browser RPC can publish activity for supported websites.

> LMX RPC is an independent community utility and is not affiliated with Discord. Discord controls how activities are displayed and may change its platform rules or behavior.

## Quick start

1. Install and open the Discord **desktop** app (stable, PTB, or Canary). Sign in to the account where you want the activity to appear.
2. Create your own Discord application and copy its **Application ID** into LMX RPC's **Discord application** field.
3. Enter your activity details, state, artwork, and any optional buttons.
4. Press **Start RPC**. If more than one Discord desktop client is running, select the client you want LMX RPC to connect to.
5. Check your Discord profile. Discord may take a moment to update and may hide activities depending on your status, privacy settings, or client behavior.

The **Setup check** can help identify whether Discord is running, which client was selected, and whether RPC connected and received a presence acknowledgement.

## Create an application in Discord Developer Portal

1. Go to [Discord Developer Portal](https://discord.com/developers/applications) and sign in.
2. Select **New Application**, enter a name, accept the terms, and create it. Use a name that accurately describes your activity and follows Discord's rules.
3. Open the application's **General Information** page and copy its **Application ID**. Paste this into LMX RPC. The ID identifies the application; do not confuse it with a bot token. **Never put a bot token in LMX RPC or share it.** This program does not need a bot account or bot token for Rich Presence.
4. If you want custom artwork managed by Discord, open the application's Rich Presence/art asset area in the portal, upload the images, and give each asset a short name. Enter that exact asset name in the corresponding **Large image key** or **Small image key** field. Portal labels can change over time.
5. Save your changes in LMX RPC and start RPC. Keep Discord's desktop client running.

You can create separate Discord applications for separate identities or activities. Each application has its own Application ID and uploaded assets. The activity name and icon Discord shows are controlled by the selected application and Discord; the preview in LMX RPC is approximate.

## What you can customize

- **Details** and **State**: the two activity text lines.
- **Large image** and **Small image**: an uploaded Discord asset key or a direct image URL, plus hover text.
- **Activity buttons**: up to two optional buttons with a label and an `http://` or `https://` link. Enable the second button to publish it. Only provide destinations you trust and control or have checked.
- **Browser RPC**: publish supported-site activity when an allowed site is detected. The built-in list is shown in the Browser RPC tab. Experimental features let you add custom website hosts; detection depends on the browser and site, and custom websites may not expose reliable page information.
- **Profiles and backups**: save named configurations, switch profiles, and restore the pre-import backup from Settings.

## Import a configuration from a file or URL

LMX RPC imports configuration files in JSON format. Importing replaces the current configuration rather than merging selected fields. Before a successful import, the app saves the current configuration and creates a pre-import backup. If the RPC is already running, it reconnects using the imported settings.

### Import a local file

1. Use the **Import** button in the bottom action bar.
2. Choose the configuration's `.json` file. It should be an LMX RPC configuration exported from the app or otherwise formatted as a compatible configuration JSON.
3. After the import succeeds, review the fields and save or start RPC as needed.

### Import from a URL

1. In **Settings**, find **Import & presets** and the **Import from link** field.
2. Paste a direct `http://` or `https://` URL that returns the raw configuration JSON. A webpage that displays or links to the JSON is not the same as a direct JSON URL.
3. Select **Import** and confirm that you trust the source when prompted.
4. Review the imported settings after it completes.

Only use configuration links from sources you trust. Imported settings can change activity text, image references, button labels and destinations, browser options, and startup preferences. The app does not merge incoming values with your existing settings.

### Restore what you had before an import

Open **Settings > Import & presets > Profiles & backups** and select **Restore pre-import backup**. This restores the configuration saved immediately before the last successful file or URL import. If you want to keep the current setup, save it as a named profile before importing.

## Use an image URL, including a GIF

For an externally hosted image, LMX RPC needs the **direct address of the image file**, not the webpage that displays it:

1. Open the image itself in a browser. For a Tenor GIF, open the GIF/image view rather than copying the address of the Tenor post or search-results page.
2. Right-click the image and choose **Copy image address** (in some browsers the wording is **Copy image link**).
3. Paste that address into **Large image key** or **Small image key**.
4. Test it in Discord. Use an address that starts with `https://` and opens the image directly without a login, expiring session, or permission prompt.

A copied page link usually will not work as an image. If right-clicking the image does not offer **Copy image address**, or the copied address opens a webpage, use the host's direct-image option or upload a supported image as an asset in your Discord application and enter its asset name instead.

Discord and its clients control image fetching, caching, sizing, and animation. A GIF URL may display as a still image or may fail to load; LMX RPC cannot guarantee that an external host or Discord will serve and animate it. Uploaded assets are generally the more predictable option. Avoid private or sensitive images, and remember that anyone viewing the activity may be able to see the artwork and text.

## Keep your activity appropriate and safe

Only use names, text, artwork, and links that you have the right to use and that comply with Discord's [Terms of Service](https://discord.com/terms) and [Community Guidelines](https://discord.com/guidelines), as well as the rules of any image host or linked service. In particular:

- Do not use content that is hateful, harassing, threatening, sexually explicit, exploitative, or otherwise prohibited by Discord.
- Do not impersonate Discord, another person, a company, or an official application; avoid misleading or abusive application names.
- Do not use artwork, animations, logos, or characters unless you created them, have permission, or the license allows your use. Publicly accessible does not mean free to reuse.
- Do not link to scams, malware, phishing pages, or other harmful destinations.
- Do not use private image URLs or disclose personal, confidential, or sensitive information in activity text, hover text, images, or links.

**You are responsible for the application you create and for every name, text, image, GIF, and link you publish.** LMX RPC simply sends the values you enter to Discord; it does not review or approve them, and it cannot protect you from moderation actions. If Discord or a hosting service removes content, limits an application, or takes action against your account for your choices, that is your responsibility. Using this program does not exempt you from platform rules. When unsure whether something is allowed, do not publish it and check the platform's current rules.

## Need help or found a bug?

If you run into a bug or cannot troubleshoot the problem any further, click **Support Discord** in LMX RPC and join the support server. Open the **Support Thread** area and create a new post describing the issue.

Include what you were trying to do, what happened, what you expected to happen, and the steps that reproduce the problem. A screenshot and the LMX RPC version can also help. Start with a clear description; you do not need to attach logs right away.

If the problem cannot be diagnosed from your description, LoseMyXelf will reach out and ask you for the relevant logs. Share logs when requested, and review them first for personal information or private URLs you do not want to disclose. Never post passwords, bot tokens, or other secrets.

## Troubleshooting

- **RPC does not connect:** open the Discord desktop client, sign in, then stop and start RPC again. If several Discord clients are open, choose the intended client.
- **Activity connects but does not appear:** confirm the correct Application ID and selected Discord client, check Discord activity/privacy settings, and look for the presence acknowledgement in the LMX RPC log. A connection alone does not guarantee Discord will show the activity to every viewer.
- **Artwork is missing:** confirm the asset key exactly matches an uploaded asset, or verify that the URL opens the image directly in a private browser window. Try a standard PNG/JPG or upload the image as an application asset to isolate URL-host issues.
- **GIF does not animate:** this is controlled by Discord and the image delivery path; try a direct HTTPS image URL or use an uploaded static asset.
- **Browser RPC does not update:** enable Browser RPC, visit one of the allowed sites, and check the Browser RPC status for the detected browser/site and whether it is allowed. The app keeps the last allowed presence when you leave an allowed site.

## Configuration and privacy

LMX RPC stores its configuration locally under `%LocalAppData%\LMX RPC\config.json`. It can include your Application ID, activity text, image references, button labels/links, and preferences. Do not share a configuration export without checking it for personal or sensitive information first. Do not place bot tokens, passwords, or other secrets in configuration fields.

