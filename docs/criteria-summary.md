# Scoring Criteria Summary

This file records implementation-level rules derived from the provided source documents. It is intentionally a summary, not a copy of the manuals.

## Shared App Flow

1. Calculate chronological age from test date and birth date.
2. Select the active assessment tab: SELSI, PRES, or REVT.
3. Find the matching age band.
4. Look up receptive and expressive raw scores.
5. Return age-equivalent, percentile, and interpretation labels when available.
6. Display a clear note that results require professional interpretation.

## SELSI

- Target age range: 4-35 months.
- Main domains: receptive language, expressive language, combined language.
- Use age-band norms to compare raw scores against mean, -1 SD, and -2 SD thresholds.
- Use age-equivalent tables to convert raw scores into equivalent months.
- Use percentile tables to describe the child's relative position within the age band.
- Domain-level summaries should distinguish receptive, expressive, and combined language results.

## PRES

- Target age range: preschool range, roughly 2-6 years in the source material.
- Main domains: receptive language and expressive language.
- Raw scores can be converted into language developmental age.
- Percentile scores are calculated from the age-band percentile conversion table.
- Combined language age can be calculated from receptive language age and expressive language age.
- Interpretation should compare combined language age against chronological age and flag large delays.

## REVT

- Main domains: receptive vocabulary and expressive vocabulary.
- Source sheet includes age-group mean/SD tables, raw-score equivalent age tables, and percentile tables.
- The linked PDF did not provide extractable text through the connector, so manual rules need PDF review or OCR before final implementation.

## Safety Notes

- Do not expose full manual text or full proprietary norm tables in a public repository without permission.
- Keep generated explanations short and avoid presenting the app as a standalone diagnosis tool.
- Keep raw child-identifying information out of GitHub, logs, and browser storage where possible.
