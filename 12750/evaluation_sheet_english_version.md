# Evaluation sheet: Home screen (scenario 12750)

[![Português](https://img.shields.io/badge/idioma-Português-green?style=for-the-badge)](evaluation_sheet_portuguese_version.md)
[![English](https://img.shields.io/badge/language-English-blue?style=for-the-badge)](evaluation_sheet_english_version.md)

Sheet used to evaluate each prototype generated for scenario 12750. The expected result of each row is the corresponding acceptance criterion in the backlog ([`backlog_english_version.md`](backlog_english_version.md)). Each evaluator fills in their own copy, independently, for v1 and for the final version.

## 1. Identification

| Field                                        | Value                                                        |
| -------------------------------------------- | ------------------------------------------------------------ |
| Scenario                                     | 12750                                                        |
| Input configuration                          | ☐ D ☐ B ☐ W ☐ DB ☐ DW ☐ BW ☐ DBW                             |
| Model                                        | ☐ GPT-6.1 Sol ☐ Claude Opus 5.5 ☐ Qwen3.5-4B ☐ Gemma 3 4B IT |
| Repetition                                   |                                                              |
| Operator                                     |                                                              |
| Evaluator                                    |                                                              |
| Version evaluated (write the GitHub release) |                                                              |
| Evaluation date                              |                                                              |
| Figma file link                              |                                                              |

## 2. Status legend

| Code    | Status                        | When to use                                                                                       |
| ------- | ----------------------------- | ------------------------------------------------------------------------------------------------- |
| **M**   | Met                           | The prototype represents the expected result.                                                     |
| **NM**  | Not met                       | The expected result is not represented, or is represented incorrectly.                            |
| **UV**  | Unable to verify              | Something in this run prevented verification. Record the reason under "Observed".                 |
| **NAP** | Not assessable in a prototype | Defined before data collection. Not filled in by the evaluator and excluded from the calculation. |

## 3. Evaluation by criterion

### R01: Search content (Function)

| ID     | Expected result                                                                                                                                      | Verification procedure                                                                     | Observed | Evidence | Status             |
| ------ | ---------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------ | -------- | -------- | ------------------ |
| R01.1  | With the Home screen showing the 4 items, when the user taps the search icon in the top bar, a search text field is shown.                           | Find the search icon in the top bar and check the representation of the open search field. |          |          |                    |
| R01.2a | When the user types a term in the search field, only the items whose title contains the term remain visible (e.g., "bible" shows only the 2 videos). | Check the representation of the state with a typed term and the filtered list.             |          |          |                    |
| R01.2b | Filtering is case-insensitive.                                                                                                                       | —                                                                                          | —        | —        | **NAP (proposed)** |
| R01.3  | When no title contains the term, the message "No results found" is shown.                                                                            | Check the representation of the no-result state, with the exact message text.              |          |          |                    |
| R01.4  | When the user clears or closes the search, the 4 items are shown again.                                                                              | Check the representation of the return to the state with the 4 items.                      |          |          |                    |

### R02: Download documents and videos (Function)

| ID     | Expected result                                                                                                                        | Verification procedure                                                                        | Observed | Evidence | Status             |
| ------ | -------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | -------- | -------- | ------------------ |
| R02.1  | In the initial state, each of the 4 cards shows a download icon and no item is downloaded.                                             | Check, in the initial state, the download icon on the 4 cards and that no item is downloaded. |          |          |                    |
| R02.2a | When the user taps an item's download icon, the icon changes.                                                                          | Check the representation of the card after download, with the changed icon.                   |          |          |                    |
| R02.2b | When the user taps an item's download icon, the card shows the label "Downloaded".                                                     | Check the representation of the card after download, with the exact label.                    |          |          |                    |
| R02.3  | The download is simulated: no file is transferred, the page does not reload, and the downloaded state persists while the page is open. | —                                                                                             | —        | —        | **NAP (proposed)** |

### R03: Show the file size before downloading (Content)

| ID    | Expected result                                                                                                                                                                                  | Verification procedure                                              | Observed | Evidence | Status |
| ----- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------- | -------- | -------- | ------ |
| R03.1 | Without any interaction, each card shows the file size in MB: Simple Announcements 0.2 MB; Peace, Security & Unity 0.7 MB; What Happens at a Bible Study? 18.4 MB; Why Study the Bible? 21.7 MB. | Check, in the initial state, the size shown on each of the 4 cards. |          |          |        |
| R03.2 | The size stays visible before and after the download.                                                                                                                                            | Compare the card before and after download.                         |          |          |        |

### R04: View downloaded content (Navigation)

| ID    | Expected result                                                                                                             | Verification procedure                                                                     | Observed | Evidence | Status |
| ----- | --------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------ | -------- | -------- | ------ |
| R04.1 | Below the top bar there are the tabs "ALL" and "DOWNLOADED"; in the initial state, "ALL" is selected and shows the 4 items. | Check the tabs, their labels and the selection in the initial state.                       |          |          |        |
| R04.2 | When the user selects "DOWNLOADED", the tab is highlighted and only the downloaded items are shown.                         | Check the representation of the "DOWNLOADED" tab selected, with only the downloaded items. |          |          |        |
| R04.3 | If no item has been downloaded, "DOWNLOADED" shows the message "No downloaded content".                                     | Check the representation of the empty tab, with the exact message text.                    |          |          |        |
| R04.4 | When the user selects "ALL", the 4 items are shown again.                                                                   | Check the representation of the return to the "ALL" tab with the 4 items.                  |          |          |        |

### R05: Refresh the Home screen content (Function)

| ID    | Expected result                                                                                       | Verification procedure                                                                     | Observed | Evidence | Status |
| ----- | ----------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------ | -------- | -------- | ------ |
| R05.1 | The top bar contains a refresh icon.                                                                  | Find the refresh icon in the top bar.                                                      |          |          |        |
| R05.2 | When the user taps the icon, a loading indicator is shown, followed by the message "Content updated". | Check the representation of the loading indicator and of the state with the exact message. |          |          |        |
| R05.3 | After the refresh, the same 4 items and their download states remain.                                 | Check the representation of the state after the refresh.                                   |          |          |        |

### R06: Access more content (Navigation)

| ID    | Expected result                                                                                                                                        | Verification procedure                                                                      | Observed | Evidence | Status |
| ----- | ------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------- | -------- | -------- | ------ |
| R06.1 | At the bottom of the screen there is the section "More on JW.ORG" with two links, each with an icon: "Other Publications" and "Request a Bible Study". | Check the section, the two links, their texts and icons.                                    |          |          |        |
| R06.2 | When the user taps one of the links, a screen or panel titled with the link's name is shown, with a control to return to the Home screen.              | Check the representation of each link's destination screen or panel and the return control. |          |          |        |

### R07: Home screen layout (Interface)

| ID     | Expected result                                                                                                                        | Verification procedure                                              | Observed | Evidence | Status |
| ------ | -------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------- | -------- | -------- | ------ |
| R07.1  | Top bar with, from left to right: menu icon, title "Home", refresh, search and more-options icons.                                     | Check the presence and order of the top bar elements.               |          |          |        |
| R07.2  | Vertical order: top bar; tabs; row with the 2 document cards; title "Videos" and row with the 2 video cards; "More on JW.ORG" section. | Check the vertical order of the blocks in the initial state.        |          |          |        |
| R07.3a | Cards in two columns. Document card: image, title, download icon and size.                                                             | Check the two-column layout and the elements of the document cards. |          |          |        |
| R07.3b | Video card: thumbnail with play icon, title, download icon and size.                                                                   | Check the elements of the video cards.                              |          |          |        |

**Out of scope (do not evaluate):** behavior of the menu and more-options icons (they only need to be present, as in R07.1); playing videos and opening documents.

## 4. Classification by requirement

Consider only assessable criteria (exclude NAP). A requirement is **correct** when all its assessable criteria are M; **absent** when it was not implemented at all; and **present, incorrect or partial** otherwise.

| Requirement | Assessable criteria | Criteria M | Classification (Absent / Partial / Correct) |
| ----------- | ------------------- | ---------- | ------------------------------------------- |
| R01         | 4                   |            |                                             |
| R02         | 3                   |            |                                             |
| R03         | 2                   |            |                                             |
| R04         | 4                   |            |                                             |
| R05         | 3                   |            |                                             |
| R06         | 2                   |            |                                             |
| R07         | 4                   |            |                                             |

## 5. Indicators for the version evaluated

| Indicator                                   | Value |
| ------------------------------------------- | ----- |
| R (requirements considered)                 | 7     |
| R_correct                                   |       |
| R_absent                                    |       |
| Adherence: A = 100 × R_correct / R          |       |
| Coverage: C_impl = 100 × (R − R_absent) / R |       |

## 6. Nonconformities

| Criterion ID | Description | Type _(rubric to be defined)_ | Severity _(rubric to be defined)_ |
| ------------ | ----------- | ----------------------------- | --------------------------------- |
|              |             |                               |                                   |

## 7. Evaluator notes
