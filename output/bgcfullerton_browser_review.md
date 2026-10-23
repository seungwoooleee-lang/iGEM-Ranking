# bgcfullerton (Genesis iGEM 2026, MycoVela): browser review

Wiki: https://2026.igem.wiki/bgcfullerton/
Method: Playwright driving headless Chromium 153 at 1440x900. Each page was loaded, waited for network idle, scrolled top to bottom, and screenshotted. Text was read from the rendered DOM. Subpage content was read for headings and the opening text, not every paragraph.

## Earlier proxy result was wrong
The earlier static render returned 49 characters and was ranked 147 of 147. That was a render-timing failure. The page is a React/Three.js app that needs a longer wait. The proxy score should be disregarded for this team.

## Pages visited (15, all HTTP 200, no failed requests)

| Page | Rendered text (chars) | Notes |
|---|---|---|
| Home | 969 | Moon-themed hero, sponsor carousel, full nav |
| Description | 22,377 | Background, ON THIS PAGE nav, 2 tables |
| Engineering | 48,012 | Multiple DBTL cycles, 15 tables, 66 headings |
| Results | 14,629 | HPPD expression (SDS-PAGE), 3 culture screens, computational validation |
| Contribution | 9,382 | 3 iframes |
| Experiments | 3,711 | 2 of 92 images loaded at capture |
| Notebook | 963 | Short |
| Model | 18,188 | Model-03/04/05, Bayesian dose-response, sensitivity analysis, 15 tables |
| Safety and Security | 4,985 | Chapman and UCI training, E. coli risk, AMF safety |
| Human Practices | 9,714 | 15 sections, stakeholder assessment, ideas abandoned |
| Entrepreneurship | 120,753 | 113 headings, 56 tables, 13 iframes; customer discovery, market sizing, IP, regulatory |
| Education | 43,405 | 138 headings, 13 tables, 39 iframes; 10-lesson series, school and university programs |
| Diversity and Inclusion | 9,938 | |
| The Crew | 1,054 | Team roster |
| Credits and attributions | 3,983 | Labelled "Credits and attributions", not the standard Attributions page |

Screenshots: `/home/user/iGEM-Ranking/output/bgcfullerton_screenshots/`

## Observations

**Strengths (observed)**
- Full DBTL engineering documentation with lab data (SDS-PAGE, production screens).
- Model page includes equations, parameters, sensitivity and identifiability analysis, Bayesian parameter estimation, and explicit statements about how models changed the wet-lab plan (MODEL-04 "informed our changes to the initial equations").
- Education page quantifies participation and feedback (for example, 83% of Speaker Series respondents reported learning synthetic biology; 95% wanted to return; over 80% of schools in the ten-lesson programme were Title I). Coverage spans elementary, secondary, university, and public audiences.
- Entrepreneurship is the most extensive page, with customer discovery, market sizing, IP, regulatory, and a development roadmap.
- Human Practices documents ideas that were dropped after feedback, which judges look for.
- Safety page lists specific training modules and risk procedures.

**Concerns (observed)**
- The Attributions deliverable is not on a standard `/attributions` page. The nav links to "Credits and attributions." The handbook requires the standard form, so this is a Bronze criterion risk unless the form is embedded elsewhere. Needs confirmation.
- Entrepreneurship's strongest traction claim, a nursery trial, is "verbal agreement" by an anonymous production manager. Judges will weigh that lightly.
- Results report HPPD expression and culture screens, but the page states the scope of the results and no functional pathway data are shown. The engineering success claim rests on those screens.
- Some pages had unloaded images at capture (Model 104/221, Education 53/141, Entrepreneurship 109/231). This may be lazy loading below the fold. Not confirmed as broken.
- Very long pages (Entrepreneurship about 106,000 px, Education about 51,000 px). Judges may find navigation heavy, though the sticky "On this page" nav helps.

## Assessment (judge-style, not official scores)
- Wiki presentation: strong. Consistent sponsor-footer template, clear nav, readable figures, sticky table of contents.
- Engineering success: documented DBTL cycles with wet-lab data, so the Silver criterion appears met.
- Human Practices: well documented, so the Silver criterion appears met.
- Bronze Attributions: at risk until the standard form is confirmed.
- Gold: plausible on Model (general biological engineering) plus Education and Entrepreneurship (specializations). Depends on the team's judging-form selections, which are not public.

## Placement among the 147 teams
I have not browser-reviewed the other 146 teams, so I cannot give a true rank. On page depth alone, bgcfullerton would be among the strongest teams in this field for Entrepreneurship, Education, and Model. Ranks are reliable only after the top 15 are reviewed the same way.
