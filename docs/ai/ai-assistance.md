# AI assistance record

## Summary
This project used WordPress AI features to assist with content and UI suggestions. A small CSS suggestion used to make instructor columns responsive on mobile was adapted from AI suggestions and reviewed/edited by the developer (Osian Richards). All AI outputs were manually reviewed and tested before deployment.

## Tools used
- WordPress AI (WordPress.com editor features)
- Chrome DevTools (Lighthouse)
- axe DevTools (accessibility checks)

## What the AI assisted with
- Suggested initial layout and CSS adjustments for the instructor columns (switching vertical separators to horizontal on mobile). This suggestion was adapted into the responsive CSS used on the live site.
- Suggested short card copy for the “Why Train With Us?” section which was reviewed and edited.

## Specific AI-assisted code (adapted and reviewed)
The responsive CSS used to switch column vertical separators to horizontal on mobile was adapted from AI suggestions and then adjusted by the developer for correct spacing and visual appearance:

/* Instructor columns: switch vertical separators to horizontal on mobile */
@media (max-width: 781px) {
  .wpcom-ai-instructor-columns .wp-block-column {
    border-right: none !important;
    border-bottom: 2px solid #000000 !important;
    border-left: none !important;
    margin-left: 0 !important;
    margin-right: 0 !important;
    padding-left: 24px !important;
    padding-right: 24px !important;
    margin-top: 16px !important;
    margin-bottom: 16px !important;
  }

  .wpcom-ai-instructor-columns .wp-block-column:last-child {
    border-bottom: none !important;
  }
}

## Human verification and edits
- The AI-suggested CSS was manually reviewed and adjusted for spacing, specificity, and to avoid unintended overrides where possible.
- All AI-generated copy was edited for tone, accuracy, and consistency with the client requirements.
- Accessibility and performance checks were performed after edits (Lighthouse Accessibility = 98).

## Artifacts and provenance
- Save the original AI prompts and outputs in `docs/ai/prompts-and-outputs.md` (not yet added). Consider adding this file if you want full reproducibility.
- Place any code samples adapted from AI suggestions in `docs/code-samples/` or in the theme folder under version control.

## Licensing and responsibility
AI outputs may incorporate patterns from their training data. By adapting and publishing these outputs, the developer assumes responsibility for correctness and license compliance.

## Contact
If you have questions about the AI assistance or want to see original prompts/outputs, contact: https://github.com/Oshwebs23
