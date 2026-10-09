# Button

Valentir buttons and action links: one `green-900` primary, hero variants for use over photos, a compact outlined button, a soft button, the `rust-700` warning and the arrow link.

**What the consumer provides:** an `<a>` or `<button>` with `vg-btn` + one variant class, and a verb-led label in *Sentence case*.

| Class | When |
|---|---|
| `vg-btn--primary` | The main action of a section (Calculate your ROI; Talk to a Fleet Expert with `vg-btn--sm` in the header; Accept). One per block. |
| `vg-btn--hero` + `vg-btn--hero-outline` | Only over the hero photo: primary in `green-700`, secondary transparent with an `outline-inverse` border. |
| `vg-btn--outlined` | Secondary navigation after a grid (View all products, How products fit together). |
| `vg-btn--soft` | Shortcut row next to a primary (B.C. dashcam compliance, Solution finder, All resources). |
| `vg-btn--warning` | Only the newsletter Subscribe. Once per view. |
| `vg-link` | “Learn more →”, “Explore solution →”, “Read the guide: …” inside cards. Always with the 16px `arrow-forward` icon. |

- Do: `radius-md` (12px) except hero buttons (`radius-sm`); 44px minimum height; 3px `teal-600` focus ring.
- Don't: uppercase labels, two primaries side by side, `rust-700` for errors, icons before the label.
