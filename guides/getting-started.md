# Get started with Orbit Play

[All guides](../README.md#guides) · [Install the app](installation.md) · [Troubleshooting](troubleshooting.md)

This walkthrough takes you from starting the helper on your PS5 to your first
stream. You don't need a separate Chiaki app, a PSN sign-in, an account ID to
copy by hand or a tool to generate the Remote Play PIN.

> See [download availability and requirements](../README.md#beta-status) before
> installing. You usually connect at home first; afterwards you can also
> [play away from home](play-away-from-home.md). Not at home?
> [Set up from anywhere](play-away-from-home.md#set-up-from-anywhere) with a code
> from the PS5.

## Before you start

If account setup is needed, **we recommend a separate new PS5 profile with no
saves**. Creating a new local account ID may make existing saves on that profile
inaccessible. Read [account setup and recovery](account-setup.md) before continuing.

- Download and install just the [desktop app](installation.md). It includes the
  PS5 helper and starts it for you; a separate ELF download is not needed.
- Keep the computer and PS5 on the same trusted local network. Keep the PS5 awake.
- Load your jailbreak, open Payload Manager (or enable an ELF loader) and log
  into the PS5 profile you want to play as.
- Connect a controller to your computer if you want to use one. Keyboard controls
  are also available.

Screenshots show **0.2.0-beta.1**, **0.4.0** and **0.8.0** with example profile data. Use the address and
code shown on **your PS5** when following the steps.

## 1. Open Orbit Play on your computer

Choose **Console setup**. **Start playing** also takes you to setup when you
have not connected a console yet.

![Orbit Play main menu with Start playing, Playback, Controls, Console setup, Settings and Get PS5 helper](../assets/screenshots/0.8.0/23-main-menu.jpg)

*Console setup starts the connection flow. Playback changes the next stream's picture settings; Settings holds the language and the update check.*

## 2. Start the helper on your PS5

In **Console address**, enter your PS5's IP address, then choose **Start helper
on PS5**. Orbit Play sends its helper through Payload Manager, or an ELF loader
if Payload Manager isn't running, and starts it. The PS5 then shows a
notification with its address and a six-digit trust code, and Orbit Play moves on
to [step 4](#4-trust-this-computer).

You can find the PS5's IP address in **Settings → Network → Connection Status**
on the PS5. If the notification has disappeared, open the **Orbit Play** icon in
the PS5 **Media** row while the helper is running. See [the helper guide](ps5-helper.md)
if you prefer to run the helper yourself.

![PS5 helper screen showing an example console address and six-digit trust code](../assets/screenshots/0.2.0-beta.1/02-ps5-helper.jpg)

*Sample data: use your console's address and current trust code. The Media icon opens the helper screen; it does not start the payload.*

## 3. Find your console

If the helper is already running, or you started it yourself, enter the address
it shows and choose **Find console** instead. Enter only the address, without
`http://` or a port number.

![Console setup with an example address entered and Find console beside it](../assets/screenshots/0.2.0-beta.1/03-console-address.jpg)

*Find console checks the running helper. If the app reports a version mismatch, install the latest desktop app and choose **Replace helper on PS5**.*

## 4. Trust this computer

Enter the six-digit code currently shown by the helper, then choose **Trust this
computer**. From 0.8.0 you do this once per computer: the PS5 remembers it, even
after the helper or the PS5 restarts. The Orbit Play page on the PS5 lists
**Trusted computers**, where **Forget computers** removes them all; each one then
needs the new code.

![Trust screen with a sample six-digit code and Trust this computer button](../assets/screenshots/0.2.0-beta.1/04-trust-code.jpg)

*This is Orbit Play's trust code. You do not need to retrieve or type the PS5's Remote Play PIN.*

**No screen on the PS5?** From 0.7.0 the helper also saves the current code in
`/data/orbit-play/trust-code.txt` on the PS5. Open that file with a file or FTP
app connected to the PS5, such as **Files** in Orbit Store (**Internal storage →
orbit-play → trust-code.txt**), and enter its six digits. The file changes each
time the helper starts.

![Trust screen naming the trust-code.txt file for a PS5 without a screen](../assets/screenshots/0.7.0/21-trust-code-file.jpg)

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

To go straight into a game, choose it under **Start in** first: Orbit Play asks
the PS5 to start it as soon as your stream opens, and remembers the choice for
that console. Below the buttons, **Play away from home** shows whether it is on
(open it to [set it up](play-away-from-home.md)), and **Profile & connection
options** holds the console's own settings.

If the PS5 profile has a login passcode, Orbit Play asks for it in **Console
setup** before the stream opens ([example](../assets/screenshots/0.4.0/14-login-passcode.jpg)). Enter the four digits you use to log in on the
PS5. Orbit Play keeps them only until you quit, so reconnects don't ask again.

![Ready when you are screen with Start in, Start playing, and the Play away from home and Profile & connection options lines, for the fictional Player One profile](../assets/screenshots/0.8.0/24-ready.jpg)

*Your pairing is saved. Choose Start playing to open the player.*

Use **arrow keys** for menus, **Enter** to confirm and **Esc/Backspace** to go
back. Press **F1** in the player for the complete controls. See
[playback and controls](playback-and-controls.md) for controllers, picture
settings, stopping and reconnecting.

## Next time you play

Keep the PS5 awake, the helper running and the same profile logged in. Open
Orbit Play and choose **Start playing**; use **Console setup** if it needs to
find the console again. Saved pairings are kept for each console address and PS5
profile. Away from home, choose **Start playing** the same way once
[play away from home](play-away-from-home.md) is on.

**More than one PS5?** Every PS5 you connect to is saved. **Console setup** lists
them under **Saved consoles**: choose one to connect to it, or rename or remove
it. A second copy of Orbit Play is no longer needed.

![Console setup listing two saved consoles, Living room and Bedroom, with Rename and Remove](../assets/screenshots/0.8.0/26-saved-consoles.jpg)

After a PS5 reboot, reload the jailbreak and choose **Start helper on PS5**
again; this computer stays trusted, so no code is needed. To skip that step, turn
on **Start the helper by itself on the PS5** under **Console setup → Profile &
connection options**: Payload Manager then starts the helper each time the
jailbreak loads ([how it works](ps5-helper.md#start-the-helper-by-itself)). If
your PS5's IP address changes, find the new address and pair again.

**Next:** [Playback and controls](playback-and-controls.md) ·
[Switch profiles or recover a connection](troubleshooting.md)
