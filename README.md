# Remootio integration for Home Assistant

## About
This is an integration that allows Remootio garage door openers to be used with Home Assistant (HA). There's no official HA Remootio integration (yet...) so it uses HACS (Home Assistant Community Store) 

## Prerequisites
- Home Assistant 
- HACS (https://hacs.xyz/) installed
- Remootio device connected to your Wi-Fi, with a fixed IP address
- API access enabled.
  - Within the Remootio app, click settings (cog/sproket icon), scroll down to Device software, and click "Websocket API".
  - Make a note of the IP address.
  - Enable Websocket API and click Copy API Keys. Copy them to somewhere you can paste into HA.
  - Within the Remootio app, click settings (cog/sproket icon), scroll down to Network setup and click Wi-Fi to view the IP address.

## Installation
### Home Assistant
See https://www.home-assistant.io/installation/

### HACS
See https://hacs.xyz/docs/setup/prerequisites

### Remootio Integration
- From the HA main page, click `HACS` in the left column, then `Integrations`. 
- Click the 3 vertical dots in the top right corner, then click `Custom repositories`.
- For Repository, use: https://github.com/peaceduck/remootio, and for Category, choose `Integration`, then click `ADD`. Click the X to close the Custom repositories window.
- Click `+ Explore & download repositories` in the bottom right corner.
- In the Search for repository box, type in `remootio`, and select `Remootio Smart Garage Door Opener`, then click `Download` in the bottom right corner.
- On the Remootio Smart Garage Door Opener window, leave the current version, and click `Download`.
- Click the `<-` button within HA, to see the Remootio integration is pending a restart of HA.

- Restart HA - Click `Settings`, `System`, the power button in the top right corner, `Restart Home Assistant`. `RESTART`.

- Click `Settings`, `Devices & services`, `+ Add integration` in the bottom right corner. 
- In the select brand windown, type in `Remootio`, and select `Remootio Smart Garage Door Opener`.

- In the Remootio integration :: Settings window, enter the IP address, API Secret Key and the API Auth Key. Click Submit.

- After a while it should display "Success!", and let you assign an area. Choose an area, and click Finish.


## Troubleshooting
 
- Check your Remootio IP address is correct.
  - Within the Remootio app, click `settings` (cog/sproket icon), scroll down to `Network setup` and click `Wi-Fi` to view the IP address.
- If you set a static IP recently, you may have to restart Remootio for the app to show the current IP address. Within the Remootio app, click `settings` (cog/sproket icon), scroll down to `Device software`, and click `Restart device`. It may take a while to update the IP. Ping the device to confirm the IP is accessible.


## Notes
original creator: ivgg-me,   Temp repo setup until this makes it into the main core one day 
