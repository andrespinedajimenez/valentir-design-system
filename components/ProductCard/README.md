# ProductCard

Linked card in the “Connected Fleet Technology” grid: 168px image, product name, a one-line description and “Learn more →”.

**What the consumer provides:** the product `href`, an image from the **Images** group (or a new one in the same style), the exact product name (ValenCam, SolarTrack Pro, ValenTrack, ValenInsights, ValenLock, ValenGuard) and a 3–7 word description.

- The whole card is the link (`<a class="vg-card">`); the inner “Learn more” is a `<span class="vg-link">`, not a nested link.
- `vg-grid` of 3 columns with a `space-xl` gap; 2 on tablet, 1 on mobile.
- Don't: shadows, price badges, descriptions longer than two lines.
