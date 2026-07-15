# Spelling Error Experiment

## Files

Required files in the same GitHub Pages folder:

- `spellingerror_final.html`
- `practice.json`
- `spellingerror_pretest.json`
- `dist/`
  - `jspsych.js`
  - `jspsych.css`
  - `plugin-fullscreen.js`
  - `plugin-html-keyboard-response.js`
  - `plugin-html-button-response.js`
  - `plugin-survey-html-form.js`

## Google Apps Script

Use `Code.gs` in the Apps Script editor linked to your Google Spreadsheet.
Deploy as a Web App:

- Execute as: Me
- Who has access: Anyone

The current HTML already contains the Web App URL you provided.

## Important note about Google Apps Script saving

The HTML uses `fetch(..., mode: "no-cors")` for GitHub Pages compatibility with Google Apps Script.
This sends the data to Apps Script, but browsers do not allow reading the response in this mode.
Therefore, the final screen says that the send request was executed. Always confirm during pilot testing that rows are appearing in the `results` sheet.

## Experiment design currently implemented

- Auto-generated participant ID
- Random assignment to list 1 or 2
- Consent screen
- Eligibility check
- Demographic questionnaire
- Handedness questionnaire
- Fullscreen experiment
- Practice trials with feedback
- Main trials: 44 target + 44 filler
- Self-paced reading by Space key
- Judgement by F/J keys
- Google Spreadsheet saving
- Metadata recording:
  - browser
  - platform
  - screen size
  - start/end time
  - duration
  - fullscreen events
  - tab visibility events
  - randomized main order

## Before running the real experiment

1. Open the experiment via Live Server or GitHub Pages.
2. Complete one full test run.
3. Confirm the `results` sheet receives rows.
4. Confirm `main_sentence_count = 88`.
5. Confirm target count is 44 and filler count is 44.
6. Confirm Japanese text is not garbled.
7. Confirm consent and questionnaire rows are saved.

