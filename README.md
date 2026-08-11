# asc-brand-assets

ASC Brand Assets.

## Email signature files

These are referenced **by URL** from the Nexus module *Home ▸ Email Signature*, and Outlook
fetches them when a message is **sent** — not when the signature was pasted.

**That means replacing a file here, under its existing name, updates the signature already
sitting in everybody's Outlook.** Nobody has to paste anything again. It is also why these
filenames must not change, and why a file here must never simply be deleted: a broken address
breaks the picture in every signature in the company at once.

| File | What it is |
|---|---|
| `20 Years IN.png` | Facility banner — Angola |
| `20 Years FL.png` | Facility banner — Edgewater |
| `signature-promo-current.png` | **The live promotion strip.** Replace this file to change or remove the promotion. Currently the blank. |
| `signature-promo-blank.png` | A transparent 1200×300. Copy it over `signature-promo-current.png` to take a promotion down. |
| `signature-promo-TEMPLATE.svg` | Illustrator template for building a new strip. 1200×300, ASC logo embedded, safe-area guide included. |
| `signature-promo-GIMP-background.png` | The same layout flattened, for building the strip in GIMP instead. |

### Making a new promotion strip

1. Open `signature-promo-TEMPLATE.svg` in Illustrator (**File ▸ Document Color Mode ▸ RGB**, always —
   CMYK shifts the brand orange off `#FF6400`).
2. Edit the wording. Keep the canvas at **1200 × 300** every time: the email fixes the width, so a
   different shape gives a different height and the company's signatures stop matching.
3. Export PNG at **72 ppi / Use Artboards** — that lands at exactly 1200 × 300. Keep it under ~150 KB.
4. Save it here under its own name (so the library keeps every promotion), then **copy it over
   `signature-promo-current.png`** and commit. It reaches everyone within the hour.

To take a promotion down, copy `signature-promo-blank.png` over `signature-promo-current.png`.
Do **not** switch the strip off in Nexus for this: that only affects signatures generated
afterwards, and everybody who already pasted theirs would carry on showing the old promotion.

### The address to use

    https://raw.githubusercontent.com/JNIXASC/asc-brand-assets/main/<filename>

It must be `raw.githubusercontent.com`. A `github.com/.../blob/...` address is a web page, not an
image, and will not render in Outlook — and a "Copy permalink" address is pinned to one commit,
so replacing the file would never reach anybody.
