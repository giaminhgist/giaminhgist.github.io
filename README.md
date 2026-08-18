# Personal Academic Website

A minimal, responsive personal academic website served with GitHub Pages at
**https://giaminhgist.github.io**.

Built with plain HTML, CSS, and JavaScript — no framework and no build step.
All assets are stored locally in this repository.

## Project Structure

```text
index.html            About page (bio, photo, news)
publications.html     Publications list
teaching.html         Teaching, supervision, and upcoming classes
cv.html               CV viewer and download

assets/
  css/style.css       Styles
  js/main.js          Active-nav highlighting + footer year
  images/
    profile-placeholder.svg
    publications/
      publication-placeholder-1.svg
      publication-placeholder-2.svg
  files/
    cv-placeholder.pdf
```

## How to Update Content

Personal content lives directly in the HTML files, each marked with
`<!-- EDIT: ... -->` comments:

| Page | File | What to edit |
| --- | --- | --- |
| About | `index.html` | Name, bio, profile photo, news items |
| Publications | `publications.html` | Each publication's title, authors, venue, year, links, and thumbnail |
| Teaching | `teaching.html` | Courses, supervision, and upcoming classes |
| CV | `cv.html` | The CV file paths in the buttons and iframe |

The site title and footer name also appear in each page's header/footer; update
all four HTML files when you change your name.

## Replacing Placeholder Assets

### Profile photo

Replace `assets/images/profile-placeholder.svg` with your real photo (for
example `assets/images/profile.jpg`), then update the `src` in `index.html`:

```html
<img src="assets/images/profile.jpg" alt="Profile photo of Your Name">
```

### Publication thumbnails

Store real thumbnails in `assets/images/publications/` and update each
publication's `<img>` in `publications.html`.

### CV PDF

Save your real CV as `assets/files/cv.pdf` and update the two links and the
`<iframe>` in `cv.html` to point at `assets/files/cv.pdf` instead of
`assets/files/cv-placeholder.pdf`.

## Run Locally

No build step is required. Open any HTML file in a browser, or serve the
folder:

```bash
python3 -m http.server
```

Then visit <http://localhost:8000>.

## Deploy with GitHub Pages

Push this repository to the `main` branch of a repository named
`<username>.github.io` (or enable Pages from Settings → Pages → Deploy from
branch). The site will be served from the repository root at:

```text
https://<username>.github.io/
```
