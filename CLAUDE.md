# Instructions for Claude

This repository is a journalist's personal website. GitHub Pages publishes it from the main branch.

- Commit every change straight to main and push it, so the site updates. Don't open pull requests or leave work on other branches.
- Use my words exactly as I give them: my About text, headlines, outlet names and dates. Don't rewrite, shorten, summarize or add to them. If something is missing, leave a clearly marked spot and ask me.
- Never add facts about me that I didn't give you.
- Keep the site simple: one index.html with its styles inside it, and photos in an images folder. No build tools or frameworks.
- When you finish, tell me in plain words what changed, and that the live site can take a minute or two to update.

## Site style

Keep every future change in this style. It takes its colour and layout cues from washingtonsun.com: a clean news-site look. Use my name as the masthead, never the Sun's name, logo or wordmark.

- **Colours:** white background. Near-black text (#121318 for headlines, #1b1c1e for body). Grey (#51545a) for dates. Pure black (#000) for rules and label boxes. Light grey (#efefef) for thin dividers between items. One accent: yellow (#ffcf26), used sparingly, only for the Contact button and the underline when hovering over a clip headline.
- **Fonts:** the same two Google Fonts as my original site (ayahaliahmad.com). Playfair Display (700 weight) for my name in the masthead, my beat headline and every clip headline (34px for the lead clip, 20px for the rest). Inter for everything else: body text 17–18px, labels and nav 12–13px bold.
- **Masthead:** "Ayah Ali-Ahmad" centred in Playfair Display, with a yellow pill "Contact" button on the right, then a thin black rule. Below it is a centred row of small section links (About, Clips, Contact) closed off by another thin black rule. On phones my name moves to the left.
- **Section labels:** each section starts with its name in a small black box with white uppercase text, sitting on a thin black rule that runs across the column.
- **Top area:** two columns split by a thin black vertical rule. The wide left column is About: my beat as a large Playfair Display headline, then a light-grey divider, then my circular headshot (images/headshot.jpg, 200px, 180px on phones, centred on my face, no border or shadow) beside my About text. The narrow right column holds Contact (my contact line, then small Twitter and LinkedIn links) and, below it, Publications (a list with light-grey dividers). On phones everything stacks: About, Contact, Publications.
- **Clips:** the newest clip is the lead, spanning the full width with a large Playfair Display headline, closed off by a black rule. The rest sit in a grid: three columns on computers, two on tablets, one on phones. Columns are split by thin black vertical rules, with light-grey dividers between items. Each clip shows the outlet in small bold uppercase and the date in grey above the headline, which links to the story. The pattern is in a comment in the Clips section of index.html; the layout comes from CSS, so new clips need no extra markup.
- **Placeholders:** empty spots are grey italic text in square brackets, such as "[Clips coming soon]".
- **Links:** same colour as the surrounding text, underlined.
