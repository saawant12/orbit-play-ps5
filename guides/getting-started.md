# Get started with Orbit Play

[All guides](../README.md#guides) · [Install the app](installation.md) · [Troubleshooting](troubleshooting.md)

Orbit Play is a Remote Play app for jailbroken PS5s, available on Mac, Windows
and Linux. It supports local PS5 accounts without PSN sign-in and can enable
Remote Play when needed. Start the included helper on your PS5, enter its
address and code in the app, then pair and play. You do not need a
separate Chiaki app, a PSN sign-in in Orbit Play, an account ID to copy by hand,
or a separate tool to generate the Remote Play PIN.

> See [download availability and requirements](../README.md#beta-status) before
> installing. This beta connects over the same local network only.

## Before you start

If account setup is needed, **we recommend a separate new PS5 profile with no
saves**. Creating a new local account ID may make existing saves on that profile
inaccessible. Read [account setup and recovery](account-setup.md) before continuing.

- Install the [computer app](installation.md) and use the PS5 helper from the
  **same release**.
- Keep the computer and PS5 on the same trusted local network. Keep the PS5 awake.
- Load your jailbreak and log into the PS5 profile you want to play as.
- Connect a controller to your computer if you want to use one. Keyboard controls
  are also available.

Screenshots show **0.2.0-beta.1** with example profile data. Use the address and
code shown on **your PS5** when following the steps.

## 1. Open Orbit Play on your computer

Choose **Console setup**. **Start playing** also takes you to setup when you
have not connected a console yet.

![Orbit Play main menu with Start playing, Playback, Console setup and Get PS5 helper](../assets/screenshots/0.2.0-beta.1/01-main-menu.jpg)

*Console setup starts the connection flow. Playback changes the next stream's picture settings.*

## 2. Run the helper on your PS5

Run the matching `orbit-play-<version>-ps5.elf` through Payload Manager or your
ELF loader. You can save the included copy from **Get PS5 helper** in the computer
app; that copy is named `orbit-play.elf`.

The helper shows a console address and a six-digit trust code. If its notification
has disappeared, open the **Orbit Play** icon in the PS5 **Media** row while the
helper is running. See [the helper guide](ps5-helper.md) if you do not see it.

![PS5 helper screen showing an example console address and six-digit trust code](../assets/screenshots/0.2.0-beta.1/02-ps5-helper.jpg)

*Sample data: use your console's address and current trust code. The Media icon opens the helper screen; it does not start the payload.*

## 3. Find your console

In **Console address**, enter your PS5's local IP address (`PS5_IP` in these
guides), then choose **Find console**. Enter only the address, without `http://`
or a port number.

![Console setup with an example address entered and Find console beside it](../assets/screenshots/0.2.0-beta.1/03-console-address.jpg)

*Find console checks the running helper. If the app reports a version mismatch, update the app and helper together.*

## 4. Trust this computer

Enter the six-digit code currently shown by the helper, then choose **Trust this
computer**. This step may be skipped when the running helper already trusts
this computer.

![Trust screen with a sample six-digit code and Trust this computer button](../assets/screenshots/0.2.0-beta.1/04-trust-code.jpg)

*This is Orbit Play's trust code. You do not need to retrieve or type the PS5's Remote Play PIN.*

## 5. Check the profile and pair

Make sure **PS5 profile** names the user you want to play as. Choose **Pair locally**
and keep that user logged in while pairing finishes.

![Pair locally screen showing the fictional Player One profile](../assets/screenshots/0.2.0-beta.1/05-pair-locally.jpg)

*Orbit Play exchanges the Remote Play PIN and account ID for the displayed profile.*

If you see **Set up Remote Play** or **Enable Remote Play** instead, the profile
needs setup first. Follow [account setup](account-setup.md), read the proposed
changes, then return to pairing. Setup is experimental. Creating a new local ID
can affect access to existing saves; it requires your explicit confirmation.
Profiles that are already ready skip this step.

If the wrong profile appears, stop here. Log into the intended user on the PS5,
choose **Change console**, and find the console again. Each user is paired
separately.

## 6. Start playing

When you see **Ready when you are**, choose **Start playing**. The player opens
in a separate window. Click the video to give it keyboard focus.

![Ready when you are screen with Start playing for the fictional Player One profile](../assets/screenshots/0.2.0-beta.1/06-ready-to-play.jpg)

*Your pairing is saved. Choose Start playing to open the player.*

Use **arrow keys** for menus, **Enter** to confirm and **Esc/Backspace** to go
back. Press **F1** in the player for the complete controls. See
[playback and controls](playback-and-controls.md) for controllers, picture
settings, stopping and reconnecting.

## Next time you play

Keep the PS5 awake, the helper running and the same profile logged in. Open
Orbit Play and choose **Start playing**; use **Console setup** if it needs to
find or trust the console again. Saved pairings are kept for each console
address and PS5 profile.

After a PS5 reboot, reload the jailbreak and helper. A helper restart changes
the trust code, so enter the new one when asked. If your PS5's IP address
changes, find the new address and pair again.

**Next:** [Playback and controls](playback-and-controls.md) ·
[Switch profiles or recover a connection](troubleshooting.md)
