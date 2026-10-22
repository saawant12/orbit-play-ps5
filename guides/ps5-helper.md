# Start the PS5 helper

[All guides](../README.md#guides) · [First connection](getting-started.md) · [Troubleshooting](troubleshooting.md)

The helper shows the code used to trust your computer and handles the Remote
Play PIN automatically. You do not need a separate PIN-generation tool. Keep it running while using Orbit Play. The computer
app and helper must come from the **same release**.

The tested PS5 setup is **firmware 13.60, Relapse and Payload Manager v0.5.2**.
See [beta status](../README.md#beta-status) for the limits on other firmware.

## Get the ELF

Choose either copy from the same version:

- **In the app:** choose **Get PS5 helper**. Save `orbit-play.elf`, then upload
  or send it through your payload loader.
- **From a release:** download `orbit-play-<version>-ps5.elf` and
  [check its checksum](installation.md#check-your-downloads).

Save the ELF on your computer, then run it on the console using the steps below.
Check [download availability](../README.md#beta-status) for the current release.

## Run it on the console

1. Turn on the PS5 and log into the profile you want to play as.
2. Load your jailbreak, then run the Orbit Play ELF with Payload Manager or
   your compatible ELF loader.
3. Read the helper's console address and six-digit trust code. Open the
   **Orbit Play** icon in the **Media** row if you need to see the screen again.
4. In the computer app, choose **Console setup** and follow
   [the connection walkthrough](getting-started.md#3-find-your-console).

![Orbit Play helper screen with a fictional address and trust code](../assets/screenshots/0.2.0-beta.1/02-ps5-helper.jpg)

*Example address and code. Use the values shown on your own PS5.*

## The two codes

| Code | What you do |
| --- | --- |
| Six-digit **Orbit Play trust code** | Enter it in the computer app to trust that computer. Use the new code after the helper restarts. |
| PS5 **Remote Play PIN** | Nothing to copy. Orbit Play exchanges it automatically when you choose **Pair locally**. |

Neither code is a PSN password. Orbit Play does not ask you to sign into PSN in
the app.

## The Media icon and restarts

The Media icon opens a page served by the running helper. It **does not start the
payload**. After a PS5 reboot, load the jailbreak and run the helper again before
opening the icon or connecting the computer app.

Replacing or deleting the ELF does not stop an older copy already running in
memory. If the app reports the wrong helper version or the loader says the port
is already in use, follow [the update steps](installation.md#update-the-app-and-helper-together).

## Use it on your local network

Keep the PS5 and computer on the same trusted network. The helper's control
channel uses local HTTP on **TCP port 34179**; the computer app takes just
`PS5_IP` in its address field. Do not forward the helper port to the internet.

Guest Wi-Fi, client isolation or a VPN can prevent the devices from reaching
each other. If the PS5 has no address, connect it to your local network and run
the helper again. Orbit Play does not wake a PS5 from Rest Mode in this beta.
Support for waking the console is in development.

## Add the Payload Manager source

The [Payload Manager source](../payloads.json) includes the **0.2.0-beta.1** helper.

1. Copy the source URL below.
2. In Payload Manager, open **Settings → Manage Sources → Add Source**.
3. Paste that URL, choose Orbit Play and download the helper.
4. Run it and use the computer app from the same release.

```text
https://raw.githubusercontent.com/saawant12/orbit-play-ps5/main/payloads.json
```

**Next:** [Trust, pair and play](getting-started.md#3-find-your-console) ·
[Helper problems](troubleshooting.md#the-helper-icon-does-not-open)
