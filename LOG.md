# Assignment 2 — Error Log
**Group Name:** Group Two
**Assignment 2:** HTML and CSS Landing Page
**Date:** 8/24/2026
**Session:** 3:00PM - 4:00PM
---
## Error 1
**What we were working on:** 
Adding an online image 
**What I was trying to do:**
We wanted to put a link to an online image to render
 on our bicycle repair shop landing page

**The exact error or problem we saw:**
The image was not showing so it was falling back to the alt texting added in the image attributes
as shown in the `images/image_load_error.png`

**Steps we took to fix it:**
1. Went back on the internet where we got the link
2. Opened the image in a new tab
3. Copied the url
4. Replaced the old one with this new url
5. Reloaded the page

**What we learned from this:**
We need to be linking to the exact image file ending with `.png` or some other format for it to actually render
on the page, not the link address of the website hosting it.

**Screenshot location:**
`images/image_load_error_fixed`

## Error 2 : Buggy Version

### Bug #5 — Missing `box-sizing: border-box`
**Owner:** Ben Chapuma
**Date:** 8/24/2026 - 8/25/2026
**Session:** 10:00PM - 1:00AM

**What the bug is:**
The global reset rule `* { box-sizing: border-box; }` was removed from the top of `buggy-version.css`.

**Why it causes this specific symptom:**
Without `border-box`, elements fall back to the default `box-sizing: content-box`, where `padding` and `border` are added *on top of* an element's declared `width` rather than being included within it. The `.card` elements inside `.services-container` (a flex row) use `padding: 30px` and `min-width: 250px`. Under `content-box`, each card's true rendered width becomes 250px + 60px (30px padding on each side) = 310px, rather than staying at 250px as intended. With three cards now wider than designed, they overflow their flex row, causing the layout to break — cards spill past the container's `max-width: 1000px`, wrap awkwardly, instead of sitting neatly in a centered row as in the working version.

**Screenshots:**
`images/bug5-box-sizing-overflow-error-intro`
`images/bug5-box-sizing-overflow.png`

**Fix:**
Restored the global rule at the top of the stylesheet:
```css
* {
    box-sizing: border-box;
}
```

