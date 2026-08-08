Project images
==============

How project images work now (simple version):

Each project card has a FIXED image box (300 x 200 px, see .project-image-container
in style.css). Any image you point a card at is scaled DOWN to fit inside that box,
whole and uncropped (object-fit style via max-width/max-height). Different-shaped
images just get a little white space around them -- nothing is ever cut off.

So you do NOT need to pre-crop anything. To set a project's image, just point its
<img src="..."> in index.html at whatever file you want.

This folder only holds DERIVED images -- ones that couldn't be used raw:
  drone.jpg  -> a single frame pulled from Drone_visualization.gif
                (the GIF itself is ~73 MB, too big to put on the page)
  gidf.jpg   -> the Multi-Head GAT panel cropped out of the very wide
                pipeline teaser (the full banner is 3.5:1, too wide to show small)

Everything else points straight at the original figures in their own folders.

If a box ever looks too empty for a very wide/very tall image, the fix is to crop
a more square-ish region of that figure by hand and point the card at it.
