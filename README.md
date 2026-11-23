# Zelda's Birthday Card

A belated birthday card for my best friend Zelda, built as a single web page.

It opens as an envelope, drops tiny flowers over the screen, and holds a message, a candle to blow out, her old high school letters, and a few jokes built on one fact: she was the mastermind of every bad decision, and I was the executor.

## What's in it

- **Envelope:** tap it to open the card. Confetti and hearts go off.
- **Falling flowers:** small purple and pink flowers drift down the whole screen.
- **Sparkle trail:** sparkles follow a finger or cursor.
- **Her name:** tap "Zelda" and it wiggles and sends up hearts.
- **Birthday cake:** tap the candle to blow it out and make a wish. Tap again to relight it.
- **Message:** a short note from Poppy, the executor.
- **Letters you sent me:** eight sheets styled like her paper (pink, yellow, cream and lined), each with lines from her letter in her spelling. "See the real letter" opens the photo of the original. A Reply button on the last sheet sets off hearts.
- **Decision log:** a button that cycles through "plans" Zelda proposed and counts how many were executed.
- **Certificate:** an official "Mastermind of Bad Decisions" certificate.
- **Fortune button:** a random joke fortune for the year ahead.
- **Gift status:** "Physical gift: In progress". Remove it once the real present is ready.
- **Garden:** nine swaying flowers at the bottom of the card.

## Run it

Open `index.html` in a browser. There is nothing to install or build.

The page loads three fonts from Google Fonts (Fredoka, Kalam and Nunito), so it needs an internet connection to look right. Offline, it falls back to system fonts.

It uses Canvas and CSS grid, so it needs a current browser.

## Project files

| File | What it is |
| --- | --- |
| `index.html` | The whole project: HTML, CSS and JavaScript, plus the eight letter photos embedded as base64 (about 3 MB in total). |

No frameworks, no JavaScript libraries, no build step.

## Customize it

Open `index.html` in a text editor and search for these strings.

| To change | Search for |
| --- | --- |
| Colors (light and dark) | `:root {` (every color is a token at the top of the stylesheet) |
| The birthday message | `class="panel message"` |
| The "plans" in the decision log | `var proposals = [` |
| The fortunes | `var fortunes = [` |
| A letter sheet's text | `class="letters"` (each sheet is one `<figure class="sheet ...">`) |
| A letter photo | `data-src="data:image/jpeg` (the photo is the `data-src` of that sheet's button) |
| Flower colors | `var petalColors` |
| How many flowers fall | `var flowerCount` |
| The garden at the bottom | `for (var g = 0; g < 9; g++)` |
| The gift status line | `Physical gift` |

To swap a letter photo, put the new image in a `letters` folder and set the button's `data-src` to its path, for example `letters/1.jpg`. This keeps the HTML file small and easy to edit.

## Share it

The easiest way to get it onto her phone is to host the page and send her the link. Netlify Drop, Vercel and GitHub Pages can all serve a single `index.html`.

## Privacy

The letter photos show real handwriting and name other people (friends, family and teachers). If you put this project in a public GitHub repo or on a public site, anyone can read them. Use a private repo or an unlisted link, or remove the letter sheets and photos before publishing.

## Accessibility and motion

- The page follows the device's light or dark setting. The letters stay on paper-colored backgrounds in both.
- With "reduce motion" turned on in the system settings, the falling flowers, confetti, sparkles and idle animations are switched off.

## Credits

- Letters written by Zelda.
- Built by Eddie (Poppy), with help from Claude.
- Fonts: Fredoka, Kalam and Nunito, from Google Fonts.
