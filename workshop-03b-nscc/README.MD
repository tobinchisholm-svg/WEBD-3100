# WS03B Typography Worksheet

---

## A1

**Site:** stjoeph.net

### Heading

| Property | Value |
| --- | --- |
| Font family | `Georgia, "Times New Roman", serif` |
| Font size | 80px |
| Font weight | 700 |
| Line height | 88px |

### Body text

| Property | Value |
| --- | --- |
| Font family | `Georgia, "Times New Roman", serif` |
| Font size | 17.6px |
| Font weight | 400 |
| Line height | 29.92px |

---

## A2

**Font stack:** `"Inter", system-ui, -apple-system, "Segoe UI", Arial, sans-serif` for both headings and body.

**Why:** I tried Inter next to the system fonts in Figma and liked Inter better. It's clean and easy to read, even on small stuff like buttons and labels. It's free on Google Fonts, and if it doesn't load the system fonts kick in.

**Weights:**

- **400:** body text
- **500:** navigation and labels
- **600:** buttons and card titles
- **700:** headings

---

## A4 — Step 6

i think my imrovement on trying to convince people to drop out and become drunks is a really intresting way for people to go out and exporle diffrent carrers before they fully settle on a job and with my updated suggestion it will open new people to alot of new learning experinces

*(this is all a joke i dont mean a word that i just said im tired and have a midterm tmr so this just had me laughing again this is a joke. this in no way is a good suggestion or is anything that nscc agrees with. please dont kick me out of school pleae and thank you)*

---

## A5 — Accessibility Audit

| Test | Result | Pass? |
| --- | --- | --- |
| Light body contrast (`#0f172a` on `#ffffff`) | 17.85:1 | Pass |
| Dark body contrast (`#f1f5f9` on `#0b1220`) | 17.09:1 | Pass |
| Mobile / reflow (375px) | Nav wrapped, cards stacked, no sideways scroll | Pass |
| 200% zoom | Text readable, nothing cut off | Pass |

---

## B1 — FuelFare Typography Strategy

**Purpose and audience:** FuelFare tells drivers what a trip from point A to point B will cost in gas, based on their car and local gas prices. It's for everyday drivers checking costs before a trip, mostly on their phone. The content is mostly numbers like distance, fuel and dollars.

**Tone:** Sleek and bold like a car dashboard at night, but still clear and easy to read.

**Fonts:** `"Inter", system-ui, -apple-system, "Segoe UI", Arial, sans-serif` for headings and body. Inter's numbers are clear, which matters for prices and trip costs.

**Weights:** 400 body, 600 buttons and labels, 700 headings.

**System vs web font:** Inter is free from Google Fonts. I'm only loading 3 weights so it stays fast on a phone. If it doesn't load, the system fonts take over.

---

## B4

**Issue and response:** After adding Inter, my headings were still showing Arial. The Studio tokens set `--font-heading` to Arial and that rule won. I changed `--font-heading` and `--font-body` to `var(--font-sans)` so the whole page uses Inter.

**Figma:** [WEBD3100 — WS2 — Tobin Chisholm](https://www.figma.com/design/fdAypIZgA1dhU7rqwSGiqj/WEBD3100--WS2---Tobin-Chisholm?node-id=61-53&t=FT9JJpKKgMOGxLcS-1)

---

## Reflection

### 1. How does typography establish hierarchy without relying only on colour?

Its mostly the size and the weight. Headings are big and bold, body text is smaller, so you know whats important without needing colour. Spacing groups things too.

### 2. Why did you select your project's heading and body fonts? What are their fallback fonts?

Inter. It's clean and the numbers are easy to read and FuelFare is basically all numbers. If it doesnt load it goes to system-ui, Segoe UI, Arial, then just sans-serif.

### 3. What is the difference between rem, ch and clamp() in your design?

rem is based on whatever font size the user has their browser set to. ch I used for line length so paragraphs dont go too wide. clamp() makes the headings bigger on a bigger screen but stops them at a max and a min.

### 4. Which responsive or accessibility test caused you to change your typography system?

I added Inter and my headings were still Arial. Turned out the Studio tokens had the heading font set to Arial and it was beating mine. Pointed it at --font-sans and that fixed it.

### 5. How do Typography System V1 and Colour System V1 work together?

Colour tells you what stuff means, red = something you click. Type tells you whats most important. They're in the same tokens.css so I change one thing and it changes everywhere.

### 6. What will you refine before the next formal project milestone?

Fix the Figma sample text so its FuelFare stuff and not gas stations, try some long trip names, check zoom on my phone.

# this should be all the same info that is in the txt i used ai to pretty it all up so you didnt have to look at just plaing text. hope thats okay 