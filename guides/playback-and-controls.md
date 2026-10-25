# Playback and controls

[All guides](../README.md#guides) · [First connection](getting-started.md) · [Troubleshooting](troubleshooting.md)

Choose **Start playing** after pairing. The stream opens in its own player window.
Connect your controller to the computer or click the video to use the keyboard.

## Choose your picture settings

Open **Playback** from the main menu, choose your settings and select **Save
playback settings**. They apply to the **next stream**. If you are already
playing, stop first, save the changes and start again.

![Playback settings with 720p, 60 fps, H.264 and 10 Mbps selected](../assets/screenshots/0.4.0/07-playback-settings.jpg)

*Start with the default 720p at 60 fps, H.264 and 10 Mbps. Save changes before starting your next stream.*

| Setting | Choices | How to choose |
| --- | --- | --- |
| Resolution | 360p, 540p, 720p, 1080p | Start at 720p. Try 1080p for a sharper picture; reduce it if playback is unstable. |
| Frame rate | 30 or 60 fps | 60 fps gives smoother movement; 30 fps halves the work for the PS5, the network and your computer. |
| Video codec | H.264 or HEVC | H.264 is the default. HEVC (H.265) gives a sharper picture at the same bitrate; it suits computers that decode it in hardware. |
| Bitrate | 1–50 Mbps in 0.5 Mbps steps | Start at 10 Mbps. A higher value uses more network capacity; lower it if the network struggles. |
| Hardware video decoding | On or off | Leave it on. Orbit Play decodes on your graphics hardware when it can and on the processor when it can't. Turn it off only if the picture shows glitches. |
| Reconnect | On or off | When on, Orbit Play can make up to three attempts after a network interruption. |

Hardware decoding uses VideoToolbox on a Mac, D3D11VA on Windows and Vulkan on
Linux. Press **F** in the player for the stream statistics: the frame rate, the
packet loss over about the last two seconds, the codec and whether decoding uses
the hardware. Picture quality also depends on the game, the computer and the local
connection or, away from home, your home upload speed. Change one setting at a time so you can judge the difference.

## Use a controller

Connect a DualSense to the **computer** through USB or Bluetooth before starting
the stream. Both connection methods have been tested on the 13.60 setup.
Other controllers are untested. Touchpad swipes reach the PS5 as well as the
touchpad click, and the DualSense mute button turns the
[microphone](#use-the-microphone) on and off.

Keep the PS5 logged into the profile shown in Orbit Play. If you want another
profile, stop the stream and [switch profiles](troubleshooting.md#switch-ps5-profiles)
before reconnecting.

### Rumble, triggers and haptics

Under **Playback → Controller feedback**:

![Controller feedback settings: rumble, adaptive triggers and DualSense haptics over USB](../assets/screenshots/0.4.0/12-controller-feedback.jpg)

| Setting | Choices | What it does |
| --- | --- | --- |
| Rumble | Off, Weak, Normal, Strong | How strongly the controller rumbles. Normal is the default. |
| Adaptive triggers | On or off | The game's trigger resistance on a DualSense. |
| DualSense haptics over USB | On or off | With a USB cable, haptics play on the DualSense itself. Over Bluetooth, or with this off, they become rumble. |

Your PS5's own vibration and trigger-effect settings still apply. **On a Mac**,
haptics over USB need the DualSense's audio device set to 4 channels: open
**Audio MIDI Setup** (Applications → Utilities), select the DualSense, choose
**Configure Speakers** and pick **Quadraphonic**. Otherwise haptics play as rumble.

## Use the microphone

Press **M**, choose **Mic** in the player bar, or press the DualSense mute button
to turn the microphone on or off. It starts muted in every stream and uses your
computer's default input; choose a different one in your computer's sound
settings before you start the stream. On a Mac, macOS asks for microphone access
the first time. Orbit Play doesn't cancel echo, so use headphones or a headset
if the game's sound plays through speakers.

## Keyboard and mouse

Click inside the video window first. **F1** or **Controls** opens the in-player
guide, which shows your current keys. In that guide, choose **Back to game** or
press **Esc** to return. These are the default keys:

| Computer input | PS5 control |
| --- | --- |
| Arrow keys | D-pad / menus |
| W, A, S, D | Left stick |
| I, J, K, L | Right stick / look |
| Enter or Space | Cross / confirm |
| Esc or Backspace | Circle / back |
| Z / X | Square / Triangle |
| Q / E | L1 / R1 |
| 1 / 3 | L2 / R2 |
| C / V | L3 / R3 |
| O / R | Options / Create |
| P / Tab | PS button / touchpad click |
| Left / right mouse click | Cross / Circle |
| Middle mouse click | Touchpad click |
| M | Microphone on/off |
| F | Stream statistics |
| F1 | Controls guide |
| F2 | Release the mouse when aiming |

Switching focus away from the player releases held keyboard and mouse inputs.

### Change your keys

![Controls screen with mouse aiming, sensitivity and the key for each action](../assets/screenshots/0.4.0/13-controls.jpg)

Open **Controls** from the main menu. Choose a key next to an action, then press
the new key or click a mouse button on it. Each action takes up to three keys or
mouse buttons, and choosing a key that another action uses moves it. Select
**Save controls**; the new keys apply to the next stream. **Reset to defaults**
brings back the table above. F1 and F2 can't be changed.

### Aim with the mouse

Turn on **Aim with the mouse** under **Controls**. In the player, click the video
to start: the pointer disappears and moving the mouse moves the right stick, and
moving it faster turns further. Press **F2** to release the mouse, or switch to
another window. **Mouse sensitivity** (1–10) sets how fast a movement turns
fully. On Linux under Wayland, the player opens through XWayland so it can keep
the pointer in place.

## Stop and reconnect

Choose **Stop playing** from the main menu, **Stop** in the connection screen,
or close the player window to end the stream. An intentional stop does not
trigger automatic reconnect. Pressing Esc while playing sends Circle to the
PS5; it is not the stop-stream shortcut.

For a network interruption, reconnect checks the selected PS5 user before each
attempt. If the stream does not return, keep both devices awake, confirm that
the helper is running and use **Start playing** again. If the PS5 restarted,
reload the jailbreak and helper first. Reconnect does not wake a sleeping console
or switch profiles.

## If something feels wrong

- **No keyboard input:** click the video window, then try an arrow key and Enter.
- **Controller not detected:** stop the stream, check the controller connection
  in your computer's settings, then start again.
- **An input stays held:** stop the stream and reconnect the controller before
  starting again. Export diagnostics if it repeats.
- **No haptics on a Mac:** set the DualSense to 4 channels in Audio MIDI Setup as
  described [above](#rumble-triggers-and-haptics), and connect it by USB.
- **The microphone doesn't turn on:** allow Orbit Play under your computer's
  microphone privacy settings and check its default input device.
- **Stutter or breakup:** stop, lower the bitrate or resolution in Playback,
  save, and retry. If you chose HEVC, try H.264. Check the local connection as
  well as picture settings. Press **F**: packet loss above zero means the
  network is dropping part of the stream.

For repeated failures, follow [troubleshooting](troubleshooting.md#export-diagnostics).
