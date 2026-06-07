Assessment Data Schema
This app should not calculate from the raw manuals directly. Convert each source sheet into normalized data files, then calculate from those files.

Recommended Files
data/selsi.norms.json
data/pres.norms.json
data/revt.norms.json
These normalized files can be added after confirming that repository privacy and data publication rights are appropriate.

Common Fields
Each assessment should expose these top-level fields:

{
  "assessment": "SELSI",
  "version": "source-2026-06-07",
  "ageBands": [],
  "percentiles": [],
  "ageEquivalents": [],
  "interpretationRules": []
}
Age Bands
Use month-based ranges so the UI can calculate chronological age once and reuse it.

{
  "label": "27-29개월",
  "minMonths": 27,
  "maxMonths": 29
}
Percentile Rows
{
  "ageBand": "27-29개월",
  "rawScore": 50,
  "domain": "receptive",
  "percentile": 45
}
Mean And Standard Deviation Rows
{
  "ageBand": "27-29개월",
  "domain": "receptive",
  "gender": "all",
  "mean": 50.3,
  "sd": 3.41,
  "minus1sd": 46.89,
  "minus2sd": 43.48
}
Age Equivalent Rows
{
  "domain": "receptive",
  "rawScore": 50,
  "gender": "male",
  "equivalentMonths": 27
}
Interpretation Rules
Keep rule text short and separate from copyrighted manual language.

{
  "id": "delay-by-age-gap",
  "appliesTo": "PRES",
  "condition": "combinedLanguageAgeMonths <= chronologicalAgeMonths - 24",
  "label": "language disorder range",
  "severity": "high"
}
Validation Requirements
Every row must include a test code and domain.
Every age range must parse into minMonths and maxMonths.
Every score used by the UI must be numeric or explicitly marked as a range.
Empty percentile cells must remain empty/null, not zero.
The UI should show that results are screening/support information and require expert interpretation.
