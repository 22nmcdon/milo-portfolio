# How to Customize the Portfolio Site (index.html)

Every spot that needs your input is marked in the file with square brackets, like `[Student Name]` or `[ Add photo here ]`. Open `index.html` in any text editor (or right-click → Open With → TextEdit/Notepad), use Find & Replace, and work through the list below in order.

## 1. Name and branding
- Find `[Student Name]` (appears ~6 times: page title, nav logo, hero, about, footer). Replace all with his actual name.

## 2. Hero section (top of page)
- `Dancer, Actor & Vocalist` — adjust wording if desired.
- Role line under the headline — one-sentence hook.
- `[ Add full-length ballet photo here... ]` — replace the placeholder `<div class="placeholder hero-photo">...</div>` with:
  `<img src="images/hero.jpg" alt="[Student Name] in arabesque" class="hero-photo">`
  (create an `images/` folder next to `index.html` and drop photos in it).
- "Download Resume" button — change `href="#"` to the filename of a PDF resume, e.g. `href="resume.pdf"`.

## 3. About section
- Replace the photo placeholder the same way as above.
- Write the 3–5 sentence bio in the paragraph.
- Fill in the six quick-fact boxes: grade/class year, home studio, etc.

## 4. Ballet section (primary focus)
- Opening paragraph: describe technique foundation and pointe experience.
- **Summer Intensives Attended**: duplicate the `.timeline-item` block for each intensive (program name, city/state, year, scholarship notes).
- **Repertoire & Roles**: duplicate `<li>` entries in `.rep-list` for each ballet/variation performed.
- Video reel: replace the `.video-embed` placeholder with a YouTube/Vimeo embed, e.g.:
  `<iframe width="100%" height="100%" src="https://www.youtube.com/embed/VIDEO_ID" frameborder="0" allowfullscreen></iframe>`
- Gallery grid: replace each placeholder `<div>` with an `<img>` tag pointing to a ballet photo.

## 5. Musical Theatre section
- Bio paragraph on acting/vocal training.
- Performance Highlights list and Vocal Details (voice type, range, teacher).
- Competitions & Awards list — duplicate `<li>` rows as needed, with placement/result in the `<span class="tag">`.
- Second video reel placeholder for a song or monologue clip.
- Skills strip: fill in piano and upright bass experience levels. The "Creative Writing" cell is optional — delete that `.skill-cell` block entirely if you don't want it shown (matches your note that writing is secondary).

## 6. Training & Resume section
- Formal training timeline — studio names, instructors, date ranges.
- Resume download button — same PDF link as the hero button.

## 7. Gallery section
- Replace all 8 placeholder boxes with real photos, same `<img>` pattern as above.

## 8. Contact section
- Email (use a parent/guardian email if preferred for a minor).
- Phone (optional — delete the `<li>` if skipping).
- Location, Instagram handle (optional).

## Adding photos/videos later
1. Create a folder named `images` in the same location as `index.html`.
2. Drop in JPG/PNG files.
3. Replace each `<div class="placeholder ...">...</div>` with:
   `<img src="images/your-file.jpg" alt="description" class="[keep the same class names, e.g. hero-photo or about-photo]">`

## Publishing the site
Once filled in, the single `index.html` file can be hosted for free on:
- **GitHub Pages** (github.com) — good if comfortable with GitHub
- **Netlify Drop** (app.netlify.com/drop) — drag-and-drop the folder, get a live link instantly
- **Google Sites / Wix / Squarespace** — if you'd rather rebuild visually, this file is still useful as a content outline

For college/conservatory applications, share the live link in the "portfolio/website" field, or in your resume and audition materials.
