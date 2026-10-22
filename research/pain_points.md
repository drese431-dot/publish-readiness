# Where creators get stuck publishing UGC islands

Phase 0 research for an independent concept project. Not affiliated with Epic Games.
Based only on public sources. Nothing here claims to know how Epic's internal tools work.

Researched: October 22, 2026

## How to read this

**Every quote and claim below comes from search-engine excerpts of the linked pages.**
This research ran in a sandbox whose network policy blocks `dev.epicgames.com`,
`forums.unrealengine.com`, `fortnite.com` and the comparison sites, so no page was opened directly.
Before anything here goes into the PRD as a direct quote, open the link and confirm it
(see "Verify before quoting" at the end).

Evidence tags:
- **Official**: Epic or platform documentation, help articles, announcements
- **Community**: a creator's post on a public forum (one person's experience, not proof of a pattern)
- **Press**: games media coverage

---

## First: what Epic already does publicly

This matters more than any single pain point. An interviewer on the Fortnite Growth team
will know these features exist, so the project has to build on them, not reinvent them.

| What exists | Source |
|---|---|
| **Two-stage review.** Stage 1 reviews metadata and assets (title, description, loading-screen text, thumbnails, lobby background, screenshots, trailers). Stage 2 is an in-island gameplay review. | [Island Moderation Tips and FAQs](https://dev.epicgames.com/documentation/en-us/fortnite/island-moderation-tips-and-faqs-in-fortnite-creative) (Official) |
| **Content pre-checks (2025).** Automated checks on the **title, thumbnail and lobby background** against rule 1.13 ("Keep It Authentic") while a release is prepared. Two outcomes: a *warning* (you can still submit, but may fail review) or *blocked* (fix before you can continue). Near-identical titles/thumbnails are blocked; similar ones get a warning and may lose Discover visibility. | [Content pre-checks announcement](https://www.fortnite.com/news/introducing-content-pre-checks-and-discover-filtering-for-fortnite-islands) (Official), [Help: title or thumbnail flagged](https://www.epicgames.com/help/en-US/creator-programs-c-202300000001640/island-creator-c-202300000001741/my-title-or-thumbnail-is-flagged-during-island-publishing-a202300000014643) (Official) |
| **Rejection reasons in the Creator Portal.** Rejected releases show reasons on the Public Release tab, and an info icon opens a moderation report. A failed release does not take down the live version. | [Island Moderation Tips and FAQs](https://dev.epicgames.com/documentation/en-us/fortnite/island-moderation-tips-and-faqs-in-fortnite-creative) (Official) |
| **More detailed rejection emails**, announced as "the first of several" transparency improvements (the year isn't shown in the excerpt; it looks like 2023). | [Updates to Island Moderation and Rejection Notices](https://www.fortnite.com/news/updates-to-fortnite-island-moderation-and-rejection-notices) (Official), [DevTrackers mirror](https://devtrackers.gg/fortnite-creative/p/3c801826-updates-to-island-moderation-notices) |
| **Early moderation** (announced June 13, 2025): finish moderation before launch, get a passing status and the island code ahead of time. The post looks ahead, so I couldn't confirm exactly what shipped. | [Creator Portal Updates, June 2025](https://www.fortnite.com/news/creator-portal-updates-and-insights-for-fortnite-island-success---june-2025) (Official) |
| **Appeals** through the Safety and Security Center, reviewed by a human moderator. | [Sanctions and Appeals](https://safety.epicgames.com/sanctions-and-appeals) (Official) |

**Takeaway:** "We should check listings before review" is not a new idea, because Epic shipped a version of it.
The open question is **what is still slipping through and why**, which is what the pain points below cover.

---

## Pain points

Ranked by strength of evidence and by how well a 12–15 hour prototype could address them.

### 1. Listing (metadata) problems surface a full review cycle late

The metadata rules are spread across several documents, and a single rule miss sends the creator back through review.

**Evidence**
- (Official) Stage 1 of review covers the title, description, loading-screen text, thumbnails, lobby background, screenshots and trailers. [Moderation FAQ](https://dev.epicgames.com/documentation/en-us/fortnite/island-moderation-tips-and-faqs-in-fortnite-creative)
- (Official) Thumbnail rules alone span several pages: at least 1920x1080, 16:9, under 5 MB; must show the actual island and not mislead ("any guns or devices featured on your thumbnail must be available and interactable in your island"); no XP/AFK/coin-farm references or coin images; no platform-specific controls; suitable for a general audience. [Thumbnail Image Policies](https://dev.epicgames.com/documentation/fortnite/thumbnail-image-policies), [Thumbnail Guidelines for Discover](https://dev.epicgames.com/documentation/en-us/fortnite/thumbnail-image-guidelines-for-discover)
- (Official) Text fields have their own rules: the island name is capped at 40 characters and the description at 450 (in-editor docs), and descriptions must be specific to the island, not generic or misleading. [Game Details Screen](https://dev.epicgames.com/documentation/en-us/fortnite/game-details-screen-in-fortnite), [Overview and Tools Settings](https://dev.epicgames.com/documentation/fortnite/overview-and-tools-settings-in-fortnite-creative)
- (Official) XP and AFK terms are banned in metadata under rule 1.13 (a January 2025 update with a removal deadline). [PCGamesN coverage](https://www.pcgamesn.com/fortnite/island-changes) (Press), [Developer Rules](https://legal.epicgames.com/fortnite/developer-rules)
- (Community) Creators ask the forum to diagnose thumbnail failures, e.g. a thread titled "Can anyone tell me what about my thumbnail is cause it to fail the content review?" [Forum thread](https://forums.unrealengine.com/t/can-anyone-tell-me-what-about-my-thumbnail-is-cause-it-to-fail-the-content-review/1271847) (title only; I couldn't read the replies)

**What exists today:** pre-checks on title, thumbnail and lobby image for originality and misleading content (see above).

**Gap I can see from public sources:** I found **no public documentation** of pre-submission checks on the
**description, tags, or consistency between the listing and the age rating**, nor a single checklist that
explains *why* each rule matters and *how to fix* a miss. That doesn't prove such checks don't exist, only that I found no public evidence of them.

**Confidence:** High that metadata is a major failure surface. Medium on what the gap is.

---

### 2. Rejection feedback often doesn't point to the exact fix

When a rejection doesn't name the field or asset, creators guess, resubmit, and wait again.

**Evidence**
- (Community) Rule 1.7 (IP) rejection: "The screenshot does not clearly identify the specific asset or content responsible for the violation." After removing likely content, "subsequent releases have received additional Rule 1.7 / 1.7.1 enforcement actions." [Forum thread](https://forums.unrealengine.com/t/repeated-rule-1-7-1-7-1-enforcement-suspensions-request-for-manual-review/2742408)
- (Community) A rejection named a texture file that the creator says is "simply a decorative poster on a wall inside the island." [Forum thread](https://forums.unrealengine.com/t/why-would-this-in-game-poster-be-flagged-for-lego-ip-violation/2744550)
- (Community) In the IARC thread, creators describe generic rejection emails and argue the emails should name the specific issue; one rejection was attributed to the word "survive" in an island image. [Forum thread](https://forums.unrealengine.com/t/iarc/1336929)
- (Community, other platform) The same pattern on Roblox: a creator's maturity label was rejected for "Crude Humour" they couldn't find in their game, and they ask moderators to attach evidence. [Roblox DevForum](https://devforum.roblox.com/t/forcing-maturity-label-moderators-to-upload-an-image/4069374)

**What exists today:** Creator Portal moderation report and more detailed emails (see above).

**Gap:** creators still report being unable to connect a rejection to a specific field or asset.

**Confidence:** Medium. The posts are vivid but anecdotal, and I can't measure how common this is.

---

### 3. The age-rating questionnaire is confusing and interacts with the listing

The rating questionnaire is required, and creators are unsure how to answer it. A rating that doesn't match the title or thumbnail can lead to rejection.

**Evidence**
- (Official) The IARC questionnaire must be completed before you can move forward in publishing. [Publishing from the Creator Portal](https://dev.epicgames.com/documentation/en-us/fortnite/publishing-from-the-creator-portal-in-fortnite-creative)
- (Community) Creators report "no guidance from Epic on how to fill it out for things like chat"; one commenter *speculates* that implied violence in the name, thumbnail or description with a rating below Teen gets rejected; another reports that the same answers produced E10+ once and Teen later. [Forum thread](https://forums.unrealengine.com/t/iarc/1336929)
- (Community) A bug report says IARC ratings changed after submission, "even past submissions." [Forum thread](https://forums.unrealengine.com/t/iarc-ratings-are-changing-after-submission-even-past-submissions/2738408)
- (Official, other platform) Roblox restricts an experience "if it lacks accurate or complete maturity information" and warns that repeatedly answering the questionnaire incorrectly can lead to moderation. [Roblox Content Maturity](https://create.roblox.com/docs/production/promotion/content-maturity)

**Gap:** no public tool flags a mismatch between listing content (for example, violent words in the title) and the declared rating before submission.

**Confidence:** Medium. A real problem, but modeling IARC accurately would require knowledge I can't verify.

---

### 4. Review status and timing are opaque

Creators don't know how long review should take, and some see errors without a clear status.

**Evidence**
- (Community) An update "failing content review after ~24 hours, resulting with an Error message"; sent to review three times. [Forum thread](https://forums.unrealengine.com/t/creator-portal-content-review-processing-takes-too-long-and-fails-in-an-error/2753821)
- (Community) A first-ever release showed "Publishing Error," then the approval email arrived anyway. [Forum thread](https://forums.unrealengine.com/t/publishing-error-in-creator-portal-on-a-first-ever-release/2739763)
- (Community) A submission failed "approximately 2 seconds after pressing 'Submit for Review'" with an HTTP 400 error. [Forum thread](https://forums.unrealengine.com/t/creator-portal-returns-creator-portal-api-http-400-immediately-when-submitting-first-creative-1-0-island-for-review/2732802)
- (Official, other platform, for contrast) Steam publishes an expectation: store review "typically takes 3-5 business days," submit at least 7 business days ahead. [Steamworks Review Process](https://partner.steamgames.com/doc/store/review_process)
- I found **no official Fortnite review-time figure.**

**Gap:** a clear status plus an expected wait. Some of these reports are backend bugs, which a prototype can't fix.

**Confidence:** Medium.

---

### 5. Rules change, and content that was approved can stop complying

Rules are updated often, and some updates apply retroactively to content that was already approved.

**Evidence**
- (Official) The Developer Rules change log shows frequent updates (entries in Dec 2025, Mar 2026, Apr 16 2026, Apr 29 2026). [Change log](https://legal.epicgames.com/fortnite/developer-rules-change-log)
- (Official, via search excerpt) A 2025 update to rule 1.15 says images approved under the previous rule must conform to the update; later, pre-checks were made stricter, and previously published thumbnails "may now receive warnings." [Island Creator Rules news](https://www.fortnite.com/news/fortnite-island-creator-rules?lang=en-US), [Pre-checks announcement](https://www.fortnite.com/news/introducing-content-pre-checks-and-discover-filtering-for-fortnite-islands)
- (Press) A creator's map that had passed review failed moderation on a later bug-fix update and was delisted under rule 1.15. [Prima Games](https://primagames.com/gaming/fortnites-creative-islands-have-a-serious-content-moderation-issue-uefn)

**Gap:** I found no public tool that tells a creator "this rule changed, and these live islands of yours may now be at risk."

**Confidence:** Medium. A novel angle, but harder to demo in 3 minutes.

---

### 6. Review decisions and appeals feel inconsistent (operator side)

**Evidence**
- (Community) One appeal was lifted within a day; a later batch of six "were upheld with no reasoning given." [Forum thread](https://forums.unrealengine.com/t/inconsistent-sanction-appeal-process/2776004)
- (Official) Epic acknowledged an island "was mistakenly flagged" and said it is "actively working on our Island Moderation process, training and documentation" (January 2024). [FNCreate on X](https://x.com/FNCreate/status/1748536305229738294)
- (Press) "Epic Games denies maps based on certain parameters, but others manage to make it through." [Prima Games](https://primagames.com/gaming/fortnites-creative-islands-have-a-serious-content-moderation-issue-uefn)

**Gap:** standardized reason codes and a consistent checklist help reviewers decide the same way. This fits the operator side of the app.

**Confidence:** Medium-low on how common it is; high that consistency matters to both sides.

---

### 7. Only some of the team gets the rejection notice

**Evidence**
- (Official) Rejection emails go to the team owner and publisher, not to all team members. [Help article](https://www.epicgames.com/help/en-US/c-Category_CreatorPrograms/c-IslandCreator/my-creative-island-got-rejected-and-i-did-not-receive-an-email-or-sanction-id-a000091031)

**Gap:** small and concrete; could be a "Not in v1" item (team notifications).

**Confidence:** High that it's true, low on how much it hurts.

---

## How other platforms handle this (pattern evidence)

| Platform | What they do | Why it matters for us | Source |
|---|---|---|---|
| **Google Play** | "Pre-review checks" run automatically on changes before review. Some issues **must be fixed**; others can be deferred with "Proceed anyway." Since Jan 2026, issues limited to one track can be "saved for later." | Strong precedent for splitting **blocking vs. warning** checks, as Epic's pre-checks also do. | [Play Console Help](https://support.google.com/googleplay/android-developer/answer/14807773) (Official), [Android Developers Blog, Jan 2026](https://android-developers.googleblog.com/2026/01/ready-to-review-some-changes-but-not.html) (Official) |
| **Apple App Store** | 2024: ~7.77M submissions reviewed, ~1.93M rejected (about 1 in 4); 295,109 were approved after revision. | Shows how large the reject-fix-resubmit loop is at platform scale. Useful for framing, **not** a stand-in for Fortnite numbers. | [9to5Mac](https://9to5mac.com/2025/05/30/apple-shares-full-app-store-transparency-report-for-2024/), [AppleInsider](https://appleinsider.com/articles/25/05/30/millions-of-apps-were-denied-by-apple-in-2024-amid-fraud-crackdown) (Press, citing Apple's report) |
| **Steam** | Separate store-page and build checklists; "Mark as ready for review"; publishes a 3–5 business-day expectation. | A published wait expectation plus an explicit checklist before review. | [Steamworks Review Process](https://partner.steamgames.com/doc/store/review_process) (Official) |
| **Roblox** | A required maturity questionnaire sets the label; inaccurate info restricts playability. | Rating accuracy is a common pain across UGC platforms (see pain point 3). | [Roblox Content Maturity](https://create.roblox.com/docs/production/promotion/content-maturity) (Official) |

**Patterns:** (a) automated checks before human review, (b) blocking vs. warning severity,
(c) explaining the fix at the moment of failure, (d) publishing expected wait times.

---

## Recommendation for Checkpoint 1

**Solve pain point 1, framed honestly against what already exists:**

> Creators learn about listing problems a full review cycle too late, and when they're rejected,
> the feedback doesn't always point to the field to fix.

The concept extends the pre-check idea from *originality of three assets* to the *whole listing*
(title, description, tags, rating vs. content, version notes, thumbnail specs), and every failed check
says **why it matters and how to fix it**. On the operator side, standardized reason codes tied to
specific fields make rejections point to the fix (part of pain points 2 and 6).

Why this one:
- Strongest evidence, and stage 1 (metadata) is officially a separate review step.
- Fits the original plan (creator check + operator queue + dashboard) without stretching scope.
- It's an interview story: *"Epic already ships pre-checks for originality. I looked at what's still
  failing and designed for the gap."* That's more convincing than claiming a new idea.

The other candidates, and why I'd rank them lower for v1:
- **Pain point 5 (rule-change re-check of live islands):** most original idea, but it needs live-island
  data and rule versioning, which is harder to demo in 3 minutes. Good "what I'd build next" answer.
- **Pain point 3 (rating vs. listing mismatch):** interesting, but modeling IARC credibly needs
  knowledge I can't verify. A *simple* version of it can be one check inside pain point 1.
- **Pain point 4 (status/timing):** partly caused by backend bugs a prototype can't fix; the status
  timeline is already in the build plan anyway.

---

## What I could not verify

- **No public Fortnite numbers** on rejection rates, top rejection reasons, or review times.
  All sizing in the PRD will use **synthetic** data, labeled as synthetic everywhere.
- The **full scope of Epic's pre-checks** (e.g., whether they cover descriptions or tags) isn't
  stated in the excerpts I could see.
- **Dates:** the "detailed rejection emails" announcement year is inferred (~2023). The pre-checks
  announcement appears to be July 2025.
- Forum posts are **individual reports**. They show the problem exists, not how often it happens.

## Verify before quoting (Diego: about 10 minutes, click each)

1. [Content pre-checks announcement](https://www.fortnite.com/news/introducing-content-pre-checks-and-discover-filtering-for-fortnite-islands): what exactly is checked, and the date
2. [Island Moderation Tips and FAQs](https://dev.epicgames.com/documentation/en-us/fortnite/island-moderation-tips-and-faqs-in-fortnite-creative): two-stage review, common failures
3. [Thumbnail Image Policies](https://dev.epicgames.com/documentation/fortnite/thumbnail-image-policies): specs and banned content
4. [Game Details Screen](https://dev.epicgames.com/documentation/en-us/fortnite/game-details-screen-in-fortnite): title/description rules and limits
5. [IARC forum thread](https://forums.unrealengine.com/t/iarc/1336929): the generic-email and rating quotes
6. [Rule 1.7 forum thread](https://forums.unrealengine.com/t/repeated-rule-1-7-1-7-1-enforcement-suspensions-request-for-manual-review/2742408): the "does not clearly identify" quote

If anything differs from what's written here, tell me and I'll correct it before the PRD.
