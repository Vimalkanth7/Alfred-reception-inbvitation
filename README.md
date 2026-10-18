# Alfred – Wedding Reception Invitation

A scroll-driven Christian wedding reception invitation. Static site: open `index.html`, or deploy the folder as-is (Vercel, Netlify, GitHub Pages).

## The scroll story
Seven pages, one swipe each (scrolling snaps, so a short flick glides to the next page; the "Please scroll the screen" button on page 1 does the same):

1. **Arch by the lake** – names write themselves in
2. **The rings** – the arch melts into the rings; engagement wording, full names, "Love is patient…"
3. **The aisle** – an iris opens onto the church; "What God has joined together…"
4. **Save the date** – date card with live countdown
5. **The celebrations** – ONE page listing Engagement, Wedding Ceremony and Reception (date, time, venue, map button each)
6. **The swing** – "Forever begins here"
7. **Families, best wishes, hashtag, Share on WhatsApp**

## Edit the details
Everything is in the `inv-config` JSON block near the bottom of `index.html`: names, the `events` list (name, date `YYYY-MM-DDTHH:mm`, venue, place, map link), parents, best wishes, hashtag, `couplePhoto`. The first event drives the date card and countdown.

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

## Pictures
The five scene images in `assets/` were upscaled 2x with an ESRGAN super-resolution model, then each background was extended at the top and bottom (soft, blurred continuation of its own edges) so the full width of every picture always shows on any phone; only the extension can ever be cropped. If higher-resolution originals are available, drop them in and re-run the same steps.
