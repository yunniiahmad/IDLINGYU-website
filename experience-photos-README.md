# Adding Classroom Capture Photos

The Experience section on the website (`docs/index.html`) currently ships with
placeholder cards instead of real classroom photos, because the screenshots in
`~/Documents/IDLINGYU/Classroom Captures/` have not been cleared for public
posting yet (they may show children's faces and need parental consent).

## To add a real photo

1. Confirm the photo is cleared for public use (parental consent obtained, or
   faces cropped/blurred as needed).
2. Export/crop it to a reasonable web size (under ~500KB, roughly 1200px on
   the long edge is plenty).
3. Save it into `docs/assets/experience/` with a short descriptive filename,
   e.g. `docs/assets/experience/efk-level-1-speaking-task.jpg`.
4. In `docs/index.html`, find the `<!-- EXPERIENCE PLACEHOLDER -->` cards in
   the Experience section and replace one placeholder `<div class="photo-placeholder">`
   block with:

   ```html
   <figure class="photo-card">
     <img src="assets/experience/efk-level-1-speaking-task.jpg" alt="Short description of what's happening in the photo" loading="lazy">
     <figcaption>Short caption, e.g. "EFK Level I — speaking task"</figcaption>
   </figure>
   ```

5. Commit and push. GitHub Pages redeploys automatically.

Repeat for as many photos as you'd like to feature.
