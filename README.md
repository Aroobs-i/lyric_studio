# Lyric Popup Studio

A single-file web page for making vertical (9:16) lyric videos in the style of "coded lyrics" posts. Each lyric line appears in a retro error-dialog popup with an animated emoji, tilted over a filmed-monitor wall of real Java code. You screen-record it and post the clip.

No install, no build step, no internet needed. Everything, including the emoji GIFs, is inside `lyric-popup.html`.

## Quick start

1. Save `lyric-popup.html` anywhere on your computer.
2. Double-click it to open it in Chrome, Edge, Firefox or Safari.
3. Type the song title in the **Song title** box.
4. Paste your lyrics into the **Lyrics** box, one line per popup.
5. Press **Play**, or open **Record mode** and start your screen recorder.

## Controls

| Control | What it does |
| --- | --- |
| Song title | Sets the popup's title and the title string inside the code wall. Updates live. |
| Lyrics box | One line per popup. Click any row to preview that line on the stage. |
| Emoji buttons | Click one to put that emoji on the row you are editing. |
| Play / Pause | Steps through the lines automatically. |
| Next | Shows the next line. The popup's OK button and the × do the same. |
| Restart | Goes back to the first line. |
| Seconds per line | How long each line stays up (0.6 to 6 seconds). |
| Song audio | Optional. Choose an audio file from your computer and it plays when you press Play. |
| Record mode | Hides the editor and fills the screen with the 9:16 frame. |

### Keyboard shortcuts (outside the text boxes)

- **Space**: play or pause
- **Right arrow**: next line
- **Esc**: leave Record mode

## Choosing emojis

Each line gets an emoji automatically. Your 11 animated GIFs rotate with the black headphones, black butterfly and black rose. To choose one yourself, start the row with its code and a bar:

```
:3: | your lyric line here
!🦋 | another line
```

| Code | Emoji |
| --- | --- |
| `:1:` | Pensive face |
| `:2:` | Squinting face with blush |
| `:3:` | Smiling face |
| `:4:` | Black heart |
| `:5:` | Blushing face with fingers |
| `:6:` | Relieved face with sweat drop |
| `:7:` | Pixel heart |
| `:8:` | Compact disc |
| `:9:` | Pixel flame |
| `:10:` | Sparkle burst |
| `:11:` | Music notes |
| `!🎧` | Black headphones |
| `!🦋` | Black butterfly |
| `!🌹` | Black rose |

A `!` in front of a normal emoji turns it black. You can use any emoji this way, for example `!🥀 | your line`. Without the `!`, a normal emoji keeps its colors and gets a small looping animation (bounce, wiggle, spin, pulse, float or shake).

## Recording a 9:16 video

1. Click **Record mode**. The page goes full screen and shows a 9:16 frame in the middle.
2. Start your screen recorder (OBS, the Windows Game Bar, macOS screen recording, or your phone's recorder if you open the page there).
3. Press **Space** to play. Press **Space** again to pause, or **Esc** to leave.
4. Crop the recording to the centre 9:16 frame in your video editor (CapCut, DaVinci Resolve, and similar) and add your song audio there if you did not use the **Song audio** box.

Tip: to line a line up with the beat, set **Seconds per line** to match the song, or press the right arrow at each beat instead of using Play.

## Customising

Everything is plain HTML, CSS and JavaScript in one file, so you can open it in any text editor.

- **Colors of the code wall:** the `--k`, `--p`, `--s`, `--n`, `--f` values near the top of the `<style>` block.
- **Dialog size and tilt:** `.dialog` (width) and `.plane` (the `rotateZ`, `rotateY` and `rotateX` values) in the CSS.
- **The code on the wall:** the `SRC` string in the script is ordinary Java source. Replace it with any other code you like. Wrap a parameter name in `⟦ ⟧` to show it as a grey IDE hint, and write `%TITLE%` where you want the song title to appear.
- **Automatic emoji order:** the `pool` list in the script.

## Notes

- Use lyrics you have the right to show. The page ships with placeholder lines only.
- The emoji GIFs are shrunk to about 128 pixels to keep the file near 1.2 MB, so they may look slightly softer than the originals.
- If the emojis show as strange characters when you open the file, make sure it is saved as UTF-8 and opened in a modern browser.
- Audio only plays after you press Play, because browsers block sound until you interact with the page.

## Files

- `lyric-popup.html`: the whole project.
- `README.md`: this file.
