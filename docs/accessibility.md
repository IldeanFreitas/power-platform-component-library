# Accessibility decisions

The reference component is designed around these review criteria:

- Every interactive control has an `AccessibleLabel`.
- The logical tab order is brand, notifications, then profile.
- Actions use descriptive text for screen readers rather than icon-only meaning.
- Notification state is communicated with a number, not color alone.
- The consuming app is responsible for testing contrast after supplying its
  accent color and theme tokens.
- The final component must be tested in Power Apps Studio with keyboard and
  screen-reader tooling before release.
