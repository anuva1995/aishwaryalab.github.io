# Quantum Imaging and Sensing Lab — Website

A 6-page static site (Home, Research, People, Publications, News, Contact)
built with plain HTML/CSS — no build tools, no dependencies, free to host
on GitHub Pages.

## Files

- `index.html` — Home
- `research.html` — Research areas, with longer per-project write-ups
- `people.html` — Team
- `publications.html` — Papers, data & code
- `news.html` — Lab updates, talks, awards
- `contact.html` — Contact info + message form
- `style.css` — Shared styles for all pages (edit colors/fonts here once,
  it updates every page)

## 1. Customize the content

The lab name, PI, and publications list are now real. What's still
placeholder: grad student/alumni entries on the People page, the quotes on
the homepage, a couple of undated News items, and the PI bio paragraph
(degrees, prior positions — deliberately left blank rather than guessed).
Open each `.html` file in a text editor (VS Code is a good free option) and
search for bracketed text like `[Student name]` to find what's left to
fill in. Nothing here requires touching the CSS unless you want to change
the look.

The design takes inspiration from Squarespace's Oranssi template — bold
rounded imagery, a service-style card grid, a dark CTA band, and a quote
strip — adapted with an engineering slant (brass-toned accent, monospace
figure captions). The colored gradient blocks (`.photo-frame`) are stand-ins
for real photography: once you have lab/field photos, replace a
`<div class="photo-frame">...</div>` with `<img src="images/name.jpg" alt="...">`
and it'll drop right into the same rounded frame.

To change the color palette or fonts, edit the `:root { ... }` block at the
top of `style.css`.

## 2. Put it on GitHub Pages (free hosting)

1. Create a GitHub account if you don't have one (github.com).
2. Create a new **public** repository named exactly:
   `yourusername.github.io`
   (replace `yourusername` with your actual GitHub username — this exact
   name is what makes GitHub serve it at the root of that URL).
3. Upload these files to the repository — either drag-and-drop them in the
   GitHub web UI ("Add file" → "Upload files"), or if you're comfortable
   with git:
   ```
   git init
   git add .
   git commit -m "Initial site"
   git remote add origin https://github.com/yourusername/yourusername.github.io.git
   git push -u origin main
   ```
4. In the repo, go to **Settings → Pages**, and under "Source" select the
   `main` branch and `/ (root)` folder. Save.
5. After a minute or two, your site will be live at
   `https://yourusername.github.io`.

If you'd rather the lab live at its own URL, e.g. `yourlab.example.org`
instead of `yourusername.github.io`, you can name the repo anything you
like and set up a custom domain later under Settings → Pages → Custom
domain (you'd need to own that domain, ~$10–15/year).

## 3. The contact form

GitHub Pages only serves static files — there's no server to receive form
submissions. The form in `contact.html` currently uses a `mailto:` action,
which just opens the visitor's own email client with a pre-filled email.
It works, but it's a bit clunky (some browsers block it, and it depends on
the visitor having an email client configured).

For a proper "sends a message from a webpage" form, sign up for a free
account at **Formspree** (formspree.io) or use **Netlify Forms** if you
switch hosts, and swap the form's `action` attribute to the endpoint they
give you. Both have generous free tiers for a lab site's traffic.

## 4. Ideas for what to add next

- Photos — replace the `PHOTO`/gradient placeholder boxes with real
  `<img src="images/name.jpg" alt="...">` tags once you have headshots and
  field photos (see the note above on `.photo-frame`)
- Google Scholar / ORCID links next to each person's bio
- An RSS feed or simple archive if the News page grows long
