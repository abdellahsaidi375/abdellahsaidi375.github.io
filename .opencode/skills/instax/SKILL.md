---
name: instax
description: Use when working on the Instax interactive camera website project. Covers animation flow, structure, and conventions from CONTEXT.md.
---

# Instax Project

Interactive Instax camera website. Full spec: `CONTEXT.md`.

## Flow
1. Pink bg → sakura falls with physics → glows & spins → clickable
2. Click → black screen + sound + animated text
3. Button → Instax camera slides up with curved motion
4. Shutter glows → 3s countdown → 3 photos (sound, flash)
5. Black photos "print" → voice: "forgot to show teeth"
6. 3s → 1 photo → sun picture → voice again
7. 3 more photos from folder
8. 3 photos on table → "Batoul" marquee
9. Instagram-style rating slider (right=satisfaction, left=anger, 10 images)
10. Score >7: Sonic GIF. 6-7: suspicious GIF. <5: other GIF.
11. Rating 8 → "absultute" image + "fahhhhh" sound
12. Language buttons (ar, en, dz, fr) → voice says "I miss you"

## Style
- Simple direct code. No bloated frameworks.
- `//#explaining_the_function#` above each function.
- No technical stuffing. No unstructured functions.
- Scalable but not over-engineered.
