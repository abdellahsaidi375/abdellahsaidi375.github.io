# OpenCode CLI Directive

**Project:** Interactive Instax Camera

**Allowed Technologies:** HTML5, CSS3, Vanilla JavaScript (The use of any external frameworks or libraries is prohibited).

**Objective:** To build a dynamic user experience based on sequential interaction, animation, and audio across 5 consecutive stages.

---

## Strict Rules
0. **serving:**
    - To browse the local .html files use command `npx http-server -p 8001` and use mcp `chrome-devtools` to browse it.

1. **Annotations:** 
    - The comment `//#explaining_the_function#` must be placed above each function clearly.

2. **Log Archiving:** 
    - When calling save or finish commands, `echo 'Generating smart compound log...'` must be executed.

3. **Continuous Consultation:** 
    - Writing all the code at once is prohibited. The code must be written in stages and reviewed after each stage is completed.

4. **Simplicity and Efficiency:** 
    - Bloated programming is prohibited. The code must be straightforward and extensible.

5. **Media:** 
    - All images, audio, and GIFs will be retrieved from a local folder. Use relative paths.

6. **Continuous Cleaning & Integrity Checking:** 
    - Patching code or leaving duplicate lines performing the same function when modifying is strictly prohibited.
    - When modifying any function or CSS rule, the entire code block must be called, rewritten cleanly, and completely replaced (Full Block Replacement).
    - Duplicate or disorganized code is a "nightmare" and will not be accepted. Accuracy and professionalism are more important than speed.

7. **ID-based Scope Isolation:** 
    - Each stage and each effect must be isolated based on a specific `id` in the HTML.
    - CSS rules and JS functions must be strictly bound to this `id` to prevent effects from overlapping between stages.

8. **Comments and Follow-up:** 
    - Continue placing `//#explaining_the_function#` above each function.
    - Continue using `echo 'Generating smart compound log...'`.

---

## Execution & Transitions

### Phase 1: The Falling Intro
* **Background:**
  - Completely pink.

* **Element (Sakura Blossom):**
  - A single blossom falls from the top of the screen to the center along a random path that simulates gravity and physics (use CSS `@keyframes` with `cubic-bezier`).

* **Stability and Interaction:**
  - When the blossom reaches the center, it stops, pulses, and rotates. The mouse pointer changes to a pointer to indicate that it is clickable.

* **Click Event:**
  - The screen gradually dims (dimming effect).
  - A sound file (calm music) begins playing.
  - A greeting appears with a typewriter animation.
  - Once the text animation finishes, a "Next" button appears.

### Phase 2: The Camera & Prank

* **Transition:**
  - When the "Next" button is pressed, the text and button disappear.

* **Appearance:**
  - The Instax camera slides from the bottom of the screen towards the center in a curved path (use `transform: translate` with the curve properties).

* **UI:** A prompt appears with a fade-in effect: "Get ready for the scene, smile for the camera."

* **Capture Button:**
  - The capture button glows in the camera interface followed by the flash (once).

* **Photo Capture Event:**
  - When pressed, a 3-second countdown timer appears on the screen.
  - When the timer finishes, the camera flashes and a capture sound is heard (repeating 3 times with short intervals).
  - The camera prints 3 photos that slide from the bottom. (The photos will be completely black - the prank).

### Phase 3: Voice Interaction & Sun Photo

* **First Audio Event:**
  - As soon as the black photos appear, an audio file (Voice 1) plays.

* **Concurrent Event:**
  - Use the `onended` event for the first audio file; once it finishes, a new 3-second countdown begins.

* **Sun Image:**
  - A single image is captured and printed from the camera showing the image of the sun.

* **Second Audio Event:**
  - As soon as the sun image appears, another audio file (Voice 2) plays.

* **Real Images:**
  - When the second audio file (`onended`) finishes, three images are captured consecutively with a flash effect, and the camera prints the real images (from the local folder).

### Stage 4: Arrangement, Floating Bars, Engraved Signature, and Glass Evaluation Box

* **Withdrawal:**
    - The camera descends and disappears from the screen.

* **Table Arrangement:**
    - The last three images are arranged aesthetically as if they were lying on a table.

* **Floating Marquees and Engraved Signature Effects:**

* **Floating Ribbons:**
    - Five animated text marquees appear in the `DaveMoris.otf` font, positioned above and below the center. Each ribbon has its own color and theme, with a prominent box shadow that makes it appear as a floating gift ribbon floating above the background (using a prominent box shadow and a z-index at the top).
       - Ribbon 1: rtl.
       - Ribbon 2: ltr.
       - Ribbon 3: rtl Diagonally {If it passes over a ribbon, it must pass under the next one (then over/under... until it ends)}. **-- (Center area for signature) --**
       - Ribbon 4: rtl.
       - Ribbon 5: ltr.

* **Engraved Name:**
  - In the exact center (between the top and bottom ribbons), the name "Batoul" appears in a signature font Uses the `ArefRuqaa-Bold.ttf`.
  - Animation: The text name appears with a bright glowing flash, then fades to a color very close to the pink background.
  - It must be programmed with a neumorphism/engraved text effect using A subtle `glow-effect` and inset `text-shadow` with subtle colors closely matching the pink background, to resemble a scar etched into the background.

* **Hovering Glass Sphere:**
  - To allow the viewer space to contemplate the signature, bars, and images, a div element first appears as a `flying, glowing glass sphere`.
  - Clicking on this sphere expands it into the Glassmorphism Window for evaluation.

* **Glass Window:**
  - A Window with a Glassmorphism effect (blurred background `backdrop-filter: blur` with a transparent overlay mimicking wet glass).

* **Evaluation Window (within the Glass Window only):**
  - The evaluation bar with emojis, memes, and GIFs (Sonic, Shack, etc.) appears **exclusively** as child elements within the Glassmorphism Window class and does not appear outside of it.

* **Rating Bar (Slider):**
  - The Window contains a `<input type="range">` slider with values ​​from 1 to 10, designed with CSS to mimic an Instagram slider with emojis.

* **Oninput Dynamics:** 
  - The value is related to the size of the central rating image.
  - Swiping right (happy): Enlarges the image.
  - Swiping left (angry): Reduces the image.

* **GIF Reactions:**
  - If the value is > 7: A GIF of Sonic dancing appears.
  - If the value is between 5 and 7: A GIF of a skeptical/hesitant character appears.
  - If the value is < 5: A GIF expressing displeasure appears.

* **Submit Button:**
    - The button is hidden by default and only appears if the rating is 8 or higher.

### Stage 5: TheFinal Scene & Language Buttons

* **The Meme (faahhhhh):**
    - A special case. Upon reaching the evaluation requirement and pressing the button, a picture of complete satisfaction appears with a fade-in/fade-out effect and zoom in (enlarge then fade out) to fill the screen before disappearing completely.

* **Language Buttons:**
    - The elements of the glass box disappear and are replaced by four buttons filling the box, labeled with the symbols: `AR`, `EN`, `DZ`, and `FR`.

* **Audio Interaction:**
    - When any button is pressed, a specific audio file plays, pronouncing the phrase "I miss you" in the dialect/language corresponding to the button.

---

**Guide's Task (OpenCode CLI):** Adhere strictly to this architecture. Begin by preparing the project structure (HTML/CSS) for the first phase, and stop immediately after you have finished programming the falling sakura and its interaction, to await confirmation and review.
