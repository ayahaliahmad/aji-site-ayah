---
name: add-clip
description: Add one of Ayah's published stories to the Clips section of her website from a link. Use when Ayah runs /add-clip with a story URL, or asks to add a story, clip or article to her site.
argument-hint: <link to the story>
---

# Add a clip

Ayah gives you a link to one of her stories. Add it to the Clips section of `index.html`, then publish it.

Follow the project's `CLAUDE.md` throughout. It covers using her words exactly, never adding facts, pushing straight to main, and the site style.

## 1. Open the link and read the story's details

Open the exact link Ayah gave. Use WebFetch, or the `web-fetch` agent if you have no WebFetch tool. If that can't read it, try Playwright in this container. From the published page, copy:

- **Headline.** Copy the headline exactly as published, character for character. Keep the capitalisation, punctuation, curly quotes, apostrophes and dashes as they appear.
  - Use the headline shown on the story page itself, usually the page's main `<h1>`.
  - Don't use the browser tab title or `og:title` when they differ from the visible headline. Those often add text such as " | The Washington Sun" or use a different, SEO version of the headline.
  - Never rewrite, shorten, summarise, fix or retype the headline.
- **Outlet.** The name of the publication, exactly as the site writes it, for example in its masthead, logo text or `og:site_name`.
- **Date.** The publication date shown on the page, written exactly as the page displays it. If the page shows both a published date and an updated date, use the published date. Also note that date in `YYYY-MM-DD` form, for ordering only.

**If you can't open the link, or can't find any of the three details for certain, stop.** This includes a blocked host, paywall, login page, error or missing date. Tell Ayah what went wrong and ask her for the headline, outlet and date. Never guess or fill one in from memory, from search results or from the URL. If she gives you any of them, use her words exactly.

If a blocked network host is the reason, you may also tell her which host was blocked. You can offer to allow that host in the session's environment settings, but still ask her for the details rather than waiting.

## 2. Add the clip to index.html

The Clips section is `<section id="clips">` in `index.html`.

Each clip is one `<li>` in this pattern (also kept in a comment inside the section):

```html
<li class="clip" data-date="YYYY-MM-DD">
  <a class="headline" href="STORY LINK">HEADLINE</a>
  <span class="meta"><span class="tag">OUTLET</span><span class="date">DATE</span></span>
</li>
```

- **STORY LINK:** the link Ayah gave. Strip only tracking parameters such as `utm_*`, `fbclid` and `gclid`.
- **HEADLINE, OUTLET, DATE:** the exact text from step 1. Escape only what HTML requires (`&` as `&amp;`, `<` as `&lt;`, `>` as `&gt;`). Leave every other character as it is.
- **First clip:** if the section still shows the `[Clips coming soon]` placeholder, remove that placeholder line. Add `<ul class="clips">` holding the new `<li>` in its place. Keep the pattern comment.
- **Later clips:** insert the new `<li>` as the first item in the existing `<ul class="clips">`, so the list stays newest first. If the story's date is older than clips already listed, place it where its `data-date` keeps the list in newest-first order instead. Tell Ayah where it went.
- **Duplicates:** if the same story is already listed, don't add it twice. Tell Ayah instead.

Don't change anything else on the page.

## 3. Check it

Render the page with Playwright at a desktop width and at 390px. Check the new clip shows correctly in the site style and the page doesn't scroll sideways. Fix only layout problems you caused.

## 4. Publish

Commit the change straight to `main` with a message such as `Add clip: <headline>`, and push it to `origin main`.

## 5. Tell Ayah what you added

In plain words, tell her:

- the headline, outlet and date exactly as you added them
- where the clip sits in the list
- that the live site can take a minute or two to update
