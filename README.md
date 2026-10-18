# Alfred – Wedding Reception Invitation

A scroll-driven Christian wedding reception invitation. Static site: open `index.html`, or deploy the folder as-is (Vercel, Netlify, GitHub Pages).

## The scroll story
One pinned stage; each scroll "page" opens onto the next scene:

1. **Arch by the lake** – names write themselves in, then the camera pushes through the floral arch
2. **The rings** – the doorway opens onto the rings on the Bible, with the invitation wording and Ecclesiastes 4:9
3. **The aisle** – an iris opens onto the candle-lit church; "a cord of three strands", then the date card with live countdown
4. **The church** – an ivory page sweeps in and the watercolor church rises; venue, time, directions
5. **The swing** – dissolve to the garden swing; the families, hashtag, share / RSVP

Also: an "Open Invitation" gate (lets phones start the music), falling petals and gold dust that speed up as you scroll, pointer parallax on desktop, a progress bar, and a reduced-motion fallback (plain stacked sections).

## Edit the details
Everything is in the `inv-config` JSON block near the bottom of `index.html`:

```json
{"groomName":"Alfred","brideName":"Bride","eventDate":"2026-12-19T18:00","venueName":"Venue Name",
 "venueAddress":"...","mapLink":"","dinnerTime":"07:30 PM","hashtag":"#Alfred_Weds_Bride",
 "groomFather":"...","groomMother":"...","brideFather":"...","brideMother":"...","rsvpPhone":""}
```
- `mapLink` empty → the Directions button is hidden. `rsvpPhone` empty → the RSVP button is hidden.
- `eventDate` is local time (`YYYY-MM-DDTHH:mm`) and drives the date card, countdown and WhatsApp share text.

## Music (optional)
Drop a `music.mp3` next to `index.html`. The speaker button appears automatically when the file exists.

## Files
```
index.html            page, styles, scroll timeline
assets/*.webp         the five scene illustrations
assets/js/            gsap + ScrollTrigger (local copies)
assets/fonts/         Cormorant Garamond, Jost, Pinyon Script (self-hosted)
preview.jpg           social share image (set og:image to the full https URL once deployed)
```
