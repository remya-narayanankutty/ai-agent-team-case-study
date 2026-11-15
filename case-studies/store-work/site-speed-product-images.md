# Site Speed: Every Product Image, Audited, Compressed and Re-Uploaded

Remya Narayanankutty | Founder and CEO, Belong India

## The problem
Most visitors reach the store on a phone, and the product pages were slow. The main cause was the images: many had been uploaded straight from a camera at several megabytes each, across every product and colour. Fixing hundreds of images by hand, one at a time, meant downloading each, compressing it, uploading it, deleting the old one and rewriting its image text. That was too much for a founder with limited weekly hours.

## What I built
An audit, then an automated pipeline to fix what the audit found.
- **The audit.** A scan through the store API listed every product image above a size threshold, with its product, its position (featured or additional) and its ID, sorted largest first. The target was under about 150 KB at a 1200 pixel width, in a modern compressed format.
- **The pipeline.** For each image the script downloads the original, resizes it, converts it, uploads the new file, attaches it to the same product with its original image text, and then deletes the old image. It warns if a result is still over the limit.
- **Image text.** Every image got a descriptive, consistently formatted text. The script carries the text across during replacement, so none is lost, and the multi-colour products that had only a colour name as their text were fixed to the full format.

## How it works
- **Safe to interrupt.** A progress file records every image done, so a run can stop and resume. Network errors retry automatically, and anything that still fails is logged and run again.
- **Gentle on the store.** The script limits its own rate, so it never hammers the API.
- **Checked at both ends.** Each image was measured against the threshold before the change, and the script flagged any that were still too large afterwards. The log records every success and failure.

## What went wrong and what I changed
- The first plan was to compress images by hand in a browser tool. After a first pass it was clear that the volume made that impractical, so I automated it.
- Replacing an image adds the new one at the end and drops its link to a colour variant. That changed which photo showed first and which photo showed for each colour. I wrote two follow-up scripts to restore the featured image order and re-attach each colour's image.
- A few images could not be found in the store because they had already been removed. The script logged and skipped them, rather than failing.
- A handful failed on connection errors midway. Because the run was resumable, they were simply re-run.

## How AI was used
- **Pattern:** An audit plus a resumable batch pipeline, followed by repair scripts for side effects.
- **Autonomy:** High once approved. The AI ran the whole batch unattended, under logging.
- **Guardrails:** A size threshold, a progress file so runs can resume, automatic retries, a rate limit, a warning when a result is still too large, and skip-and-log for missing images.
- **Human checkpoints:** I approved the targets and the plan before any live change.
- **How it improved:** A first manual attempt proved too slow, so I automated it. Side effects on image order and colour links led to two repair scripts.
- **My role:** I set the size, width and quality targets and the image text format.

## Results
The largest images shrank by more than 95 percent, from several megabytes to well under 200 KB. After the first pass the mobile speed score rose by roughly a third. The remaining slowness was in the homepage hero image and third-party scripts, which I identified as the next fixes.

## What I would do next
Compress images at upload time, so new products never reintroduce the problem. Then preload the hero image and defer non-critical scripts.
