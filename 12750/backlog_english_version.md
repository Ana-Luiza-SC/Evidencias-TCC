# Backlog: Home screen (scenario 12750)

Single screen of an educational content app with documents and videos. Each item below is a requirement; the acceptance criteria define the expected behavior.

## Data shown on the screen (simulated)

| Type | Title | Size |
|---|---|---|
| Document | Simple Announcements | 0.2 MB |
| Document | Peace, Security & Unity | 0.7 MB |
| Video | What Happens at a Bible Study? | 18.4 MB |
| Video | Why Study the Bible? | 21.7 MB |

Initial state: no item downloaded; "ALL" tab selected.

## R01: Search content

- **Category:** Function
- **Description:** The user can search the screen's documents and videos by title.
- **Acceptance criteria:**
  1. Given the Home screen shows the 4 items, when the user taps the search icon in the top bar, then a search text field is shown.
  2. Given the search field is open, when the user types a term, then only the items whose title contains the term remain visible, case-insensitive (e.g., "bible" shows only the 2 videos).
  3. When no title contains the term, then the message "No results found" is shown.
  4. When the user clears or closes the search, then the 4 items are shown again.

## R02: Download documents and videos

- **Category:** Function
- **Description:** Each document and video can be downloaded from its card.
- **Acceptance criteria:**
  1. Given the initial state, each of the 4 cards shows a download icon and no item is downloaded.
  2. When the user taps an item's download icon, then the item changes to the downloaded state, indicated by a changed icon and the label "Downloaded" on the card.
  3. The download is simulated: no file is transferred, the page does not reload, and the downloaded state persists while the page is open.

## R03: Show the file size before downloading

- **Category:** Content
- **Description:** Each downloadable item shows its size before it is downloaded.
- **Acceptance criteria:**
  1. Without any interaction, each card shows the file size in MB: Simple Announcements 0.2 MB; Peace, Security & Unity 0.7 MB; What Happens at a Bible Study? 18.4 MB; Why Study the Bible? 21.7 MB.
  2. The size stays visible before and after the download.

## R04: View downloaded content

- **Category:** Navigation
- **Description:** Tabs switch between all content and downloaded content only.
- **Acceptance criteria:**
  1. Below the top bar there are the tabs "ALL" and "DOWNLOADED"; in the initial state "ALL" is selected and shows the 4 items.
  2. When the user selects "DOWNLOADED", then the tab is highlighted and only the items in the downloaded state (R02) are shown.
  3. If no item has been downloaded, "DOWNLOADED" shows the message "No downloaded content".
  4. When the user selects "ALL", then the 4 items are shown again.

## R05: Refresh the Home screen content

- **Category:** Function
- **Description:** The user can refresh the screen's content.
- **Acceptance criteria:**
  1. The top bar contains a refresh icon.
  2. When the user taps the icon, then a loading indicator is shown, followed by the message "Content updated" (simulated refresh, no backend).
  3. After the refresh, the same 4 items and their download states remain.

## R06: Access more content

- **Category:** Navigation
- **Description:** A section at the bottom of the screen leads to additional resources.
- **Acceptance criteria:**
  1. At the bottom of the screen there is the section "More on JW.ORG" with two links, each with an icon: "Other Publications" and "Request a Bible Study".
  2. When the user taps one of the links, then a screen or panel titled with the link's name is shown, with a control to return to the Home screen (simulated destination, no external access).

## R07: Home screen layout

- **Category:** Interface
- **Description:** The screen follows the structure of the original interface.
- **Acceptance criteria:**
  1. Top bar with, from left to right: menu icon, title "Home", refresh, search and more-options icons.
  2. Vertical order: top bar; tabs; row with the 2 document cards; title "Videos" and row with the 2 video cards; "More on JW.ORG" section.
  3. Cards in two columns. Document card: image, title, download icon and size. Video card: thumbnail with play icon, title, download icon and size.

## Out of scope

- Menu icon and more-options icon: must be present (R07), but no behavior is required.
- Playing videos and opening documents: not required; the play icon is visual only.
