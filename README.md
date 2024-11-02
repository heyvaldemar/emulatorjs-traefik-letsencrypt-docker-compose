# EmulatorJS with Let's Encrypt Using Docker Compose

[![Deployment Verification](https://github.com/heyvaldemar/emulatorjs-traefik-letsencrypt-docker-compose/actions/workflows/00-deployment-verification.yml/badge.svg)](https://github.com/heyvaldemar/emulatorjs-traefik-letsencrypt-docker-compose/actions)

The badge displayed on my repository indicates the status of the deployment verification workflow as executed on the latest commit to the main branch.

**Passing:** This means the most recent commit has successfully passed all deployment checks, confirming that the Docker Compose setup functions correctly as designed.

📙 The complete installation guide is available on my [website](https://www.heyvaldemar.com/install-emulatorjs-using-docker-compose/).

❗ Change variables in the `.env` to meet your requirements.

❗ Place your ROM files into the respective folders for each platform within the `roms` directory.

💡 Note that the `.env` file and `roms` folder should be in the same directory as `emulatorjs-traefik-letsencrypt-docker-compose.yml`.

Create networks for your services before deploying the configuration using the commands:

`docker network create traefik-network`

`docker network create emulatorjs-network`

Deploy EmulatorJS using Docker Compose:

`docker compose -f emulatorjs-traefik-letsencrypt-docker-compose.yml -p emulatorjs up -d`

# EmulatorJS Configuration Guide

💡 Replace all instances of `http://emulatorjs.heyvaldemar.net` in this guide with your own domain specified in the `.env` file. This setup uses Docker Compose for deployment, so ensure your domain is correctly configured there.

🔒 Since the app runs over HTTP on port 3000, it’s recommended to keep this port closed on your network hardware (e.g., router or firewall) to restrict access to your internal network only. This helps prevent external access to the emulator’s configuration interface.

## Steps

1. **Download Default Fileset:**
   - Go to your configured URL (replace with your domain, e.g., `http://emulatorjs.heyvaldemar.net:3000` as specified in your `.env` file).
   - Click the **Download** button to download the default fileset. This may take a few moments.

2. **ROM Management:**
   - Navigate to **ROM Management**.
   - You’ll see options for different consoles (e.g., `gbc`, `nes`).
   - Click **Scan** under each console to scan your ROMs. This will identify any ROM files you’ve added for each platform within the `roms` directory.

3. **Config Management:**
   - After scanning, go to **Config Management** to verify your ROMs have been added.
   - Ensure that the ROM count is accurate and the scanned count reflects your available ROMs.

4. **Download Artwork:**
   - In **Config Management**, under **Step 1**, click **Download All Available Art**. This will fetch artwork for your ROMs, enhancing the visual experience.

5. **Add ROMs to Config:**
   - Click on **Add All ROMs to Config** to ensure that all scanned ROMs are now available within the emulator.

6. **Play Games:**
   - Go to your main domain (replace with your domain, e.g., `https://emulatorjs.heyvaldemar.net`) to access the game library.
   - Select your desired console and game, then enjoy playing!

# Author

I’m Vladimir Mikhalev, the [Docker Captain](https://www.docker.com/captains/vladimir-mikhalev/), but my friends can call me Valdemar.

🌐 My [website](https://www.heyvaldemar.com/) with detailed IT guides\
🎬 Follow me on [YouTube](https://www.youtube.com/channel/UCf85kQ0u1sYTTTyKVpxrlyQ?sub_confirmation=1)\
🐦 Follow me on [Twitter](https://twitter.com/heyValdemar)\
🎨 Follow me on [Instagram](https://www.instagram.com/heyvaldemar/)\
🧵 Follow me on [Threads](https://www.threads.net/@heyvaldemar)\
🐘 Follow me on [Mastodon](https://mastodon.social/@heyvaldemar)\
🧊 Follow me on [Bluesky](https://bsky.app/profile/heyvaldemar.bsky.social)\
🎸 Follow me on [Facebook](https://www.facebook.com/heyValdemarFB/)\
🎥 Follow me on [TikTok](https://www.tiktok.com/@heyvaldemar)\
💻 Follow me on [LinkedIn](https://www.linkedin.com/in/heyvaldemar/)\
🐈 Follow me on [GitHub](https://github.com/heyvaldemar)

# Communication

👾 Chat with IT pros on [Discord](https://discord.gg/AJQGCCBcqf)\
📧 Reach me at ask@sre.gg

# Give Thanks

💎 Support on [GitHub](https://github.com/sponsors/heyValdemar)\
🏆 Support on [Patreon](https://www.patreon.com/heyValdemar)\
🥤 Support on [BuyMeaCoffee](https://www.buymeacoffee.com/heyValdemar)\
🍪 Support on [Ko-fi](https://ko-fi.com/heyValdemar)\
💖 Support on [PayPal](https://www.paypal.com/paypalme/heyValdemarCOM)
