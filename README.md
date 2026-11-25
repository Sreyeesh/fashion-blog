# Everyday with Isa – Fashion Blog

A one-page fashion blog post, "An Insider's Guide to NYFW", built with plain HTML.
It's the **Fashion Blog** project from Codecademy's *Learn HTML: Elements and Structure* module.

I used this project to practise four things at once:

- **HTML**: the elements and page structure the module teaches
- **Neovim**: I wrote every line in Neovim (LazyVim config), not in Codecademy's editor
- **Git**: one branch per group of tasks, with small commits
- **Linux**: I did all the work from the terminal in WSL2

## What the page has

- A profile picture that links down to the contact section
- A byline (`by Isabelle Rodriguez | 1 day ago`)
- A main heading, two subheadings and three paragraphs
- Three images, each with alt text
- A link to the NYFW Wikipedia page that opens in a new tab
- A "Related Content" list
- A contact section with bold labels

## HTML I practised

| Concept | Elements / attributes |
| --- | --- |
| Document skeleton | `<!DOCTYPE html>`, `<html lang="en">`, `<head>`, `<meta>`, `<title>`, `<body>` |
| Headings and text | `<h1>`–`<h4>`, `<p>`, `<strong>`, HTML entities like `&amp;` |
| Images | `<img>` with `src` and `alt` |
| Lists | `<ul>` and `<li>` |
| Links | `<a href>`, `target="_blank"`, `rel="noopener"` |
| Linking inside the page | `id="contact"` and `href="#contact"` |
| Grouping content | `<div>` |

I also added a few things the brief didn't ask for: alt text on every image, `lang` and viewport meta tags, and `rel="noopener"` on the outside link.

## How I worked

I split Codecademy's 17 tasks into steps and did each one on its own Git branch:

| Step | Tasks | What I built |
| --- | --- | --- |
| 1 | 1–3 | HTML skeleton and page title |
| 2 | 4–7 | Headings and the three paragraphs |
| 3 | 8–10 | Post images, profile image and byline |
| 4 | 11–12 | Related content list |
| 5 | 13–16 | Links, contact section and bold labels |

For each step I:

1. Made a branch (`git switch -c images`)
2. Did the tasks in Neovim and saved with `:w`
3. Checked the page in the browser
4. Committed with a message that names the task, like `feat(task8): add three post images`
5. Switched back to `main`, merged, pushed to GitHub and deleted the branch

Run `git log --oneline` to see every step.

## Commands I used

I did the whole project in the terminal, using Linux, Neovim and Git together.

### Linux (WSL2)

| Command | What I used it for |
| --- | --- |
| `cd`, `ls`, `pwd` | Moving around and finding my project folder |
| `mkdir fashion-blog` | Making the project folder |
| `cat index.html` | Reading the file without opening an editor |
| `nvim index.html` | Opening the file in Neovim |
| `explorer.exe index.html` | Opening the page in my Windows browser from WSL |
| `cat index.html \| clip.exe` | Copying my code to paste into Codecademy |

### Neovim

| Command | What I used it for |
| --- | --- |
| `:HtmlTemplate` | Filling in the HTML boilerplate from my own template, then using `Tab` to jump to the title and body |
| `i`, `Esc` | Going into insert mode to type, then back to normal mode |
| `o`, `O` | Opening a new line below or above the cursor |
| `dd`, `4dd` | Deleting one line, or four lines at once |
| `/Always` | Searching for a word to jump to that paragraph |
| `:12s/old/new/` | Replacing text on one line |
| `u` | Undoing a change |
| `:w`, `:q`, `:wq` | Saving and quitting |
| `:q!` | Quitting without saving (this is how I lost changes once) |

### Git

| Command | What I used it for |
| --- | --- |
| `git switch -c <branch>` | Starting a new branch for each step |
| `git status` | Checking what changed before committing |
| `git add index.html` | Staging my changes |
| `git commit -m "..."` | Saving a step with a message |
| `git log --oneline` | Checking my history before merging |
| `git switch main` | Going back to the main branch |
| `git merge <branch>` | Bringing a finished step into `main` |
| `git push` | Uploading to GitHub |
| `git branch -d <branch>` | Deleting a branch after merging it |

## What I learned along the way

- **Saving matters.** One time my changes were gone because I quit Neovim without saving. Now I look for the `"index.html" ... written` message.
- **Commit before you merge.** I once merged a branch before committing my last task. Now I run `git status` and `git log` before every merge.
- **Watch out for curly apostrophes.** Copying text between Windows and WSL turned `’` into garbled symbols. I switched to plain `'` apostrophes and fixed the old ones in a separate commit.
- **Small commits help.** When I put the first image in the wrong place, I fixed it in a separate `fix(task8)` commit, so the history shows what changed and why.

## View it

Clone the repo and open `index.html` in a browser:

```bash
git clone git@github.com:Sreyeesh/fashion-blog.git
cd fashion-blog
explorer.exe index.html   # on WSL; use xdg-open on Linux or open on macOS
```

## Next steps

- Publish the page with GitHub Pages
- Style it with CSS in a later Codecademy module

## Credits

The project brief, blog text and images are from [Codecademy](https://www.codecademy.com/).
I wrote the HTML.
