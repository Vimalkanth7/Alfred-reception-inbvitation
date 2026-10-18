# Alfred – Wedding Reception Invitation

A scroll-driven Christian wedding reception invitation. Static site: open `index.html`, or deploy the folder as-is (Vercel, Netlify, GitHub Pages).

## The scroll story
Ten pages, one swipe each (the scroll snaps, so a short flick glides to the next page; the "Please scroll the screen" button on page 1 does the same):

1. **Arch by the lake** – names write themselves in
2. **The rings** – the camera pushes through the arch; engagement wording, full names, Ecclesiastes 4:9
3. **The aisle** – an iris opens onto the church; "a cord of three strands…"
4. **Save the date** – date card with live countdown
5. **The engagement venue** – ivory page, watercolor church, Directions
6. **The wedding ceremony** – CSI All Saints Church, 28 Dec 10:00 AM, Directions
7. **The reception** – Maharaja Mahal, 28 Dec 12:00 PM, Directions
8. **The swing** – "Forever begins here"
9. **Families & best wishes**
10. **Contacts** (tap to call), hashtag, Share on WhatsApp

Also: "Open Invitation" gate (lets phones start the music), petals and gold dust, pointer parallax on desktop, reduced-motion fallback (plain stacked sections).

## Edit the details
Everything is in the `inv-config` JSON block near the bottom of `index.html` (names, date, venues + map links, parents, best wishes, phone numbers, hashtag, `couplePhoto`). `eventDate` is local time `YYYY-MM-DDTHH:mm` and drives the date card, countdown and WhatsApp share text. `weddingDate` and `receptionDate` drive the wedding and reception pages.

## Music (optional)
`music.mp3` ("Before the Altar") plays after the guest taps Open Invitation. Replace the file to change the song.

## Files
```
index.html            page, styles, scroll timeline
assets/*.webp         the five scene illustrations
assets/js/            gsap + ScrollTrigger (local copies)
assets/fonts/         Cormorant Garamond, Jost, Pinyon Script (self-hosted)
preview.jpg           social share image (set og:image to the full https URL once deployed)
```
