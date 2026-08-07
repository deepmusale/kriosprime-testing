Times Square Showcase — static deploy bundle

Files:
  index.html          entry point (no build step, no dependencies)
  assets/city.png     1555x875 city plate (billboards blank)
  assets/blur-bg.jpg  full-viewport blurred backdrop
  assets/ai4o.png     creative -> https://ai4outcome.com/
  assets/bwa.png      creative -> https://breakfastwithagents.com/

Deploy: upload the whole folder to any static host (S3, Netlify, Vercel,
nginx, GitHub Pages). Open index.html at the web root.

Layout: the city plate is a fixed 1555x875 box, centred; the blurred image
fills any surrounding space. Ad hotspots are absolutely positioned inside
the plate, so they stay locked to their billboards.

To move or resize an ad, edit its rule in the <style> block of index.html
(#ad-ai4o / #ad-bwa) - coordinates are in plate pixels from the top-left.
To add another ad: copy an <a class="ad"> block, give it a new id, drop the
creative into assets/, and add a matching left/top/width/height rule.
