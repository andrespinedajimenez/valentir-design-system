# SiteHeader

Sticky top bar: the official horizontal logo (`valentir-logo-horizontal.svg`, 40px tall), five dropdown menus, a language switcher, the Fleet portal link and the primary CTA.

**What the consumer provides:** the menu routes and the portal URL (Wialon hosting). The fixed order is Products, Solutions, Industries, Resources, Company.

- Height `header-height` (56px on mobile), `divider` bottom border; add `vg-header--scrolled` on scroll.
- Below 900px the logo shrinks to the `valentir-mark.webp` mark (40×40) and the menu collapses into a 40px button with `radius-sm`.
- Don't: more than one CTA, the mark without the name on desktop, re-setting the name in Inter.
