What I changed

This folder contains your gallery images. I applied a safe cleanup and normalization to make filenames consistent and to avoid duplicates interfering with the site.

Actions performed:

- Exact duplicate files (by content) were moved to `Images/_duplicates/<category>/` so nothing was permanently deleted.
- Filenames were normalized previously to remove leading `Copy of ` and trailing ` copy`, and spaces were replaced with hyphens.
- You asked to now convert filenames to lowercase and replace hyphens with underscores; that has been applied to files remaining in each `Images/<category>/` folder.

Naming conventions now used (applied automatically):
- Lowercase filenames (e.g. `Nora_Mahler.JPG` -> `nora_mahler.jpg`)
- Hyphens replaced with underscores (e.g. `my-photo.jpg` -> `my_photo.jpg`)
- Spaces replaced with underscores
- If a rename would collide with an existing filename, a numeric suffix `_1`, `_2`, etc. was appended to make the name unique.

If you want different rules (keep uppercase, use hyphens instead, etc.), tell me and I can revert or reformat names.

How to update galleries after adding or changing files:
- Run `./cleanup_and_inject.sh` from the project root to move duplicates, normalize (Copy of) names, and inject gallery HTML into `index.html`.
- Or run `./rename_lower_underscores.sh` to apply lowercase + underscore normalization and automatically re-run the injection.

Notes:
- The site references images in `Images/<category>/` where `<category>` is one of `experimental`, `traditional`, `darkroom`, `color`.
- I left moved duplicates in `Images/_duplicates/` so you can restore any file if needed.
