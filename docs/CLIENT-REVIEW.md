# Client Review: Lab 07 Access Review and Audit

**Repository folder:** `lab-07-access-review-and-audit`
**Status:** Client review (not published)
**Purpose:** Second lab of the nine-lab portfolio, built in the same style and evidence approach as the Lab 03 sample.

This file is for internal review only. It can be removed before publication.

**How to review:** open [`preview.html`](preview.html) in any web browser. No installation or internet connection is needed: all images and styling are embedded. It is a local approximation of the README, not an exact GitHub rendering, and `README.md` remains the deliverable. Use *Expand all screenshots* at the top of the preview to open every supporting-screenshot section at once. Like this file, `preview.html` is a review aid and should be removed before publication.

---

## 1. Decisions required before publication

| # | Decision | Options / notes | Client answer |
|---|---|---|---|
| 1 | **Approve style and content** | Approve as is, or list changes (tone, length, section depth, badge set, heading emojis, diagram style). | |
| 2 | **Hands-on completion** | Did the portfolio owner personally complete this lab, including Lab 6 beforehand? | |
| 3 | **Own evidence** | Do you have your own evidence, for example your entitlement inventory, ranked findings, the questions you could not answer, or your exports (`users.json`, `groups.json`, `applications.json`, `events.json`)? If you share any of it, it will be reviewed for personal data and secrets before use. | |
| 4 | **Permission to republish source material** | The lab text and all 32 screenshots come from *Hands-On IAM Labs – Lab 7: Access Review and Audit* (V8) by Andrew, All Things Identity. Please confirm you have permission to republish them publicly, or tell us to replace them with your own screenshots. | |
| 5 | **GitHub owner** | GitHub username or organization that will own the repository. | |
| 6 | **Repository name** | Proposed: `lab-07-access-review-and-audit`. Confirm or provide an alternative. | |
| 7 | **Repository visibility** | Public or private. Nothing will be created or pushed until this is confirmed. | |

---

## 2. How the answers change the README

- **If hands-on completion is confirmed with your own evidence:** the evidence-scope note and the "source-demonstrated" wording will move to first-person, execution-based wording. Your inventory schema, findings and decisions can be summarized (with personal data removed), and the status badge will change from *Client review* to a completion status.
- **If completion is confirmed without your own evidence:** the guide screenshots and attribution stay, and the wording can say the lab was completed while still noting that the screenshots and example values are the guide's.
- **If completion is not confirmed:** the current wording stays. It describes the review method and the guide's example results without claiming personal execution, findings or certification decisions.
- **If republishing permission is not available:** guide screenshots will be removed. The README will rely on the custom diagrams, the inventory schema and the filter and export tables until your own screenshots are supplied.

---

## 3. Optional confirmations

These items are not blockers, but answers would make the README more specific:

- Did you complete the optional **Section 05 exports**? They are currently documented as proposed outputs, not included.
- Should the README link to the prerequisite labs (Labs 1, 3, 4, 5 and 6) once those repositories exist?
- Is there a preferred author name or profile link for the footer?

---

## 4. Evidence and safety decisions already applied

- All screenshots are attributed to All Things Identity, and the README states they are example screenshots from the training guide. Exact source captions are kept in [`evidence-manifest.json`](evidence-manifest.json).
- **Each selected screenshot was inspected individually** for credentials, tokens, private keys, session identifiers and personal information. None was found, so **no redaction was applied**:
  - client IP, location, ISP, ASN and lab host were already replaced by the source author with placeholders such as `<client-ip>`, `<your-location>` and `<your-lab-ip>`;
  - the user agent in Figure 7.35 was hidden by the source author;
  - people in the screenshots are fictional lab accounts using `company.com` and `example.com` addresses;
  - Figure 7.36 shows only public certificate fingerprints; no private key is displayed.
- The guide's example Authentik address is not reproduced; the README uses `YOUR_AUTHENTIK_URL` throughout.
- Values visible in the screenshots (group member counts, employee counts, export counts, account names) are labeled as **examples from the guide's environment**, not results.
- **Not included and not fabricated:** a completed inventory, user or entitlement totals, last-login dates, retention coverage, certification decisions, reviewer names, findings, severity ratings, approvals, API exports, and the clipped end of the Grafana role expression.
- Eleven figures were left out as navigation screens or near-duplicates; reasons are listed in the manifest.
- At the client's request, the architecture and workflow diagrams are **editable Mermaid diagrams** written as text in `README.md`. GitHub draws them directly; editing the `mermaid` code block changes the diagram. Only the banner remains an image.

---

## 5. Unresolved source limitations

- **Grafana role mapping is clipped** in Figure 7.11. The guide tells the reader to check the full value on their own screen, so the fallback role is not stated in the README.
- **Group-change events do not identify the member** on the open-source Authentik version. Linking a member to a date relies on time correlation with the Lab 1 dashboard run or a Lab 6 ticket.
- **`akadmin` is shared with automation.** The Lab 1 dashboard's API token belongs to `akadmin`, so events attributed to it do not identify a specific person. A `python-requests` user agent is contextual evidence only.
- **`password_set` records whose password changed, not who changed it.** The actor must be inferred from surrounding events.
- **`secret_view` covers tokens and certificates only.** The Grafana client secret copied in Lab 5 is never logged.
- **Retention is a configured limit.** The source shows `days=365`, but the evidence window starts at the oldest available event.
- **No business scenario.** The guide does not describe a specific organization, so none is invented.
- **No measured outcomes.** The guide provides no metrics or timings beyond example screenshot values, so none are reported.
