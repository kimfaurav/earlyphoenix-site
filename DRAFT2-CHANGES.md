# index-draft2.html: what changed from draft 1, and why (2026-09-10)

Brief: `04-Projects/Early_Phoenix_Website_Brief.md` (v2). Nothing live.

1. The page is now a credibility check, not a lead generator. 30 of 46 sourced relationships are referrals, 0 came through the site, so it is built to be forwarded upward.
2. Two-pillar grid, "AI transformation" section, "Live in 24 hours" process and every "competitive intelligence" line are gone. Shelf Signal is gone from the homepage (never paid for).
3. New spine: hero, coverage strip, built-by band, the work (3 live decks + the breeder register + case study link), 6 published findings, the method (reconciliation, Demand Signal, provenance), 3 cleared names, advisory band, newsletter, contact.
4. No prices and no free/paid line anywhere, per Kim 19:43.
5. Names on the page are exactly the 3 Kim cleared at 20:00: Battersea, NatureWatch, Nutrition & Santé (Lactalis). Defra, Scottish Government, RSPCA, Cats Protection, RKC, CFSG and the rest are OFF (they are rooms, not clients).
6. Every number traces to the live case-study page, the decks, or Strategy v1: 75%, ~10%, 57%, 3 of 5, 6 months, 6 species, 20 markets, 150,000+, 100+ retailers, 140 species. No absolute listing counts (percentage rule, 2026-07-26).
7. Advisory: ruling A closed 12 Sep ("Yes, let's have advisory appearing on the Early Phoenix side as well"). One titled band after the client strip: who it is for (owner-managed businesses and scale-ups, the AI-native transition), the operator CV behind it, links to LinkedIn (https://www.linkedin.com/in/kimfaura/, verified by Dex) and contact. No prices, not a pillar.
8. Newsletter box: Kim's copy verbatim, LIVE Buttondown embed (account `faura`, field name="email"). TESTED 20:12 from the rendered page with kimfaurav@gmail.com: Buttondown returned "You've successfully subscribed to Kim Faura!". Kim to confirm the subscriber shows in the Buttondown dashboard. "Powered by Buttondown" kept, styled quiet, pending Dex's check of the free-tier terms. PDF linked, never attached.
9. Hero DECIDED 12 Sep 07:14 (Kim: "the main one, I agree"): A's headline kept, both credential lines cut as irrelevant, no vertical named; body is the broad framing (marketplaces and retail pricing at scale, what is listed, who lists it, what it costs, how it moves). Option B deleted. The operator CV lives in the built-by band and the advisory band instead.
10. Checks passed: 0 em dashes, 0 spelled-out numbers, 0 "not a" constructions, no horizontal scroll at 400px, all fade-ins render.

Numbers CONFIRMED by Kim 12 Sep: "6 species" ("definitely, six species we're tracking"; Ireland runs all 6, snapshot 6 Sep) and the councils count is OFF the homepage entirely (Kim 07:21: "definitely not... it needs to be in a case study, not in a headline message"). The register card describes what the register is, no count. The number belongs on the register page, stated against its denominator. Coverage is UK AND IRELAND, reflected in the species label. Kim may still move the coverage-strip specifics; the hero is agreed.

## 17 Sep: 4 changes for go-live (Dex brief, Kim-approved; target Tue 22 Sep after sign-off)

11. Marketplaces tile under The Work: a 5th, full-width card, "Has Vinted won Europe? Listing velocity across 4 markets" (Vinted against the local classifieds leaders in France, Germany, Italy and Spain; with Tom Pandolfo for AIM Group, April 2026; source `04-Projects/Vinted_EU_Analysis/Narrative_Draft_v2.md`). Described, NOT linked, until Kim clears the AIM link. Section subtitle reworded so it no longer promises every tile opens. For the RecommerceBuzz traffic from 17 Sep.
12. Rooms line, new: one muted line under the 3-name client strip, "Speaking at RecommerceBuzz, Berlin, October 2026." No rooms line existed on draft 2 before this (the 10 Sep ruling left Defra, Scottish Government, RSPCA, Cats Protection, RKC, CFSG OFF the page); it now carries only what the 17 Sep brief named. Whether the older rooms join it is Kim's call.
13. Ireland: "Presented to the Advisory Council on Companion Animal Welfare, Department of Agriculture, Food and the Marine, Ireland" is written into the rooms line as an HTML comment, to be uncommented ONLY once Kim confirms the 17 Sep 14:30 session happened. Not rendered.
14. Battersea unchanged on the strip. Nothing about the Desirability Index.
15. Mobile menu: hamburger below 900px (44px button, aria-expanded/aria-controls), stacked links, closes on tap of any link. Tested at 400px: opens, closes, anchors land, no horizontal scroll. Hidden at desktop.
16. Not touched: prices, free/paid, SalesAPE, advisory scope, hero, coverage strip, findings, newsletter.

## 5 Oct: Feeds (Dex brief `04-Projects/Early_Phoenix_Website_Feeds_Brief_2026-10-05.md`, Kim-approved direction)

17. Hero, option A applied for preview (Dex's recommendation, smallest change): "What is being sold, what is being built, and by whom." Body now names public registers: "Early Phoenix reads online marketplaces, retail prices and public registers at scale. What is listed, what is planned, who is behind it, what it costs, and how all of that moves. We build the systems, run them continuously, and turn what changes into intelligence or action." Alternatives for Kim: B "What is being sold, what is being planned, and by whom." C "What is listed, what is planned, and by whom." Recommendation A: it keeps the 12 Sep line intact and "built" is the plain word a builder uses.
18. Feeds band after The Work, built on the advisory-band style so it carries the same weight. Says what a feed is and how it arrives (weekly, into your CRM, letter sent for you), with planning as the first. Links to contact. No client name, no prices, no results, no council count. Nav unchanged at 5 items (Kim's 12 Sep cut).
19. /planning drafted at `planning/index.html`: noindex, not linked from the nav, the homepage or sitemap.xml. For a trade buyer: what arrives each week, what lands in the CRM (fields taken from the live loader, `weekly/load.py`), what the letter does (owner or occupier at the property, plus the design firm's office, per `weekly/send.py`), a direct call to action. Outcome slot marked as a dashed box plus an HTML comment; remove if still empty at release.
20. Figures: none added. The feed's 59 councils is sourced (`config/councils.json`, sef-referrers) but left off both pages: it is one client's territory, and the 3 Oct read was not clean (Wandsworth and 1 Agile council failed), so 59 is attempted, not read.
21. Checks: 0 em dashes, 0 spelled-out data numbers, no X-not-Y lines, no horizontal scroll at 400px on either page.

## 5 Oct 09:14: Kim's rulings (via Dex)

22. Hero REVERTED to the 12 Sep text (title, meta description, h1, body). Kim rejected A, B and C. Planning is carried by the Feeds band and /planning, both kept as built.
23. Ireland confirmed: the Advisory Council line is now rendered in the rooms block.
24. Rooms block now reads, in order: "Presented to the Advisory Council on Companion Animal Welfare, Department of Agriculture, Food and the Marine, Ireland." / "Supporting local councils." / "Speaking at RecommerceBuzz, Berlin, October 2026." No Defra, no council count.
25. 09:17 correction (Dex): Kim meant the LIVE hero. h1 and body now match master index.html verbatim: "Competitive intelligence for complex markets" / "We build data infrastructure that tracks what's happening across markets others can't see. Retail pricing, animal welfare, marketplace dynamics, and more. Across Europe, updated daily." Eyebrow unchanged. Title and meta description still carry the 12 Sep wording (not in Dex's instruction; flagged).

## 5 Oct 09:22 to 09:30: v3, 4 products as in the 30 Sep AI Roundtable deck (brief `04-Projects/Early_Phoenix_Website_v3_Brief_2026-10-05.md`)

26. Hero: live wording kept; eyebrow dropped; tab title and meta description matched to the hero.
27. The Work = 4 product cards in deck order, wording verbatim from slides 23 to 26 (read from the deck itself): Shelf Signal (back on the homepage, reverses 10 Sep), Pet welfare intelligence (one card, all 6 species, decks and case study inside it as evidence), Builder's Sales Pipeline, Dog Breeder Registry ("Commissioned by Naturewatch Foundation", register link kept). Section title "4 products, one engine".
28. Removed: Newsletter section and nav item, "Built by an operator" band, the Feeds band (the Builder's Sales Pipeline card replaces it), the Vinted card from The Work.
29. /planning kept unlinked and noindex, renamed in title and eyebrow to Builder's Sales Pipeline. Path unchanged.
30. Clients: 5 names (Battersea, NatureWatch, Nutrition & Santé (Lactalis), South East Formwork, AIM Group). Rooms block unchanged.
31. New Talks and writing section: the AIM Group Vinted piece (described, not linked) and the RecommerceBuzz Berlin panel.
32. Method reworded to cover all 4 products, same 3 rules. "Nothing is estimated" dropped, since it was a pet-deck claim.
33. CTA adds builders.
34. Findings rebuilt from the September decks (pet-markets check; I opened each deck on the mini, all dated 2 Oct): 6.1% French Bulldog share (dog deck), 56.9% of horses under £5,000 (horse deck), rabbits with no welfare fields on most platforms (small mammals deck), town hotspots kept as "suggest" (dog deck). REMOVED as unsupported: 75% of puppy sales, 6 months+, 3 of 5 platforms. HELD: CITES (deck now says 36%, base ambiguous). Bird Article 10 figure not used (no published bird PDF). Plus 2 marked placeholders, Shelf Signal and builder pipeline, no numbers.
35. UNVERIFIED, unchanged: coverage strip "20 European grocery markets" and "150,000+ products priced daily" (March audit), "6 species, UK & Ireland", "Monthly since February 2026". Product text figures (59 councils, over 254 council registers, 5am) are Kim's published slide text, used as written. 59 is what the feed attempts; the 3 Oct read had 2 council failures. Hero "updated daily" open with Kim (pet data is monthly).

## 5 Oct 09:32: v4, Kim's review in this session

36. Coverage strip removed entirely ("delete that whole line and go straight to the work"). Hero shortened so The Work starts above the fold at 1280x800.
37. Method, the rooms line (Ireland, councils, Berlin) and Talks and writing removed (Kim: not of much relevance).
38. Clients: + Rabbit Welfare Association & Fund (Rae) and REPTA. Now 7 names.
39. 4 product detail pages, each linked from its card: shelf-signal/, pet-welfare/, builders-sales-pipeline/ (was planning/, now linked and indexable), dog-breeder-registry/. Each carries who commissions it: South East Formwork (pipeline) and Naturewatch Foundation (registry) confirmed; Shelf Signal and Pet welfare show a dashed "to be confirmed" slot pending Kim.
40. Shelf Signal markets: UK, France, Spain, Portugal (Kim, 5 Oct). "20 European grocery markets" and "150,000+" are gone from the site with the strip.
41. All page text comes from Kim's deck slides 23 to 26 and their notes, the live loader (pipeline), and earlier sourced copy. No new figures.
42. Hero DECIDED by Kim 11:39: h1 "We read entire markets and tell you what just changed." Body: "Supermarket shelves, pet-selling platforms, planning registers and council licence lists. Read continuously, delivered daily, weekly or monthly." Title and meta matched. Replaces the live "Competitive intelligence" hero and its "updated daily" claim.
43. Hero body: no orphan words (Kim, 12:08). text-wrap: balance on headings and lead lines, pretty on body copy, site-wide incl. the 4 product pages; the second hero sentence kept on one line from 601px up. Checked at 1280, 768 and 400.
44. Work cards (Kim, 12:10): every card carries a "Commissioned by" line. Pet welfare card cut to the slide's one line: species line and published-decks links removed from the homepage (the decks stay on the pet-welfare detail page). Shelf Signal and Pet welfare commissioners pending Kim, shown as dashed "to be confirmed".
45. Commissioners confirmed by Kim 12:12: Shelf Signal = Nutrition & Santé (Lactalis), Pet welfare = Battersea. Applied to the cards and both detail pages; no slots left.
