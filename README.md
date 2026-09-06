# GitHub Contribution Practice — Movie Watchlist

Welcome! 👋

In this exercise you will practice a **real GitHub contribution workflow** using a small HTML, CSS and Vanilla JavaScript application.

The goal is not only to write code. The goal is to learn:

**Fork → Clone → Branch → Code → Commit → Push → Pull Request → Review → Update**

You will work on the `trainxdummy/todo` repository and submit your work through a Pull Request.

## 1. What are we building?

You will work on a small **Movie Watchlist** application. It is similar to a Todo app, but is intentionally not a Todo app.

The application should allow users to:

- Create a movie entry
- View movie entries
- Update/edit a movie
- Delete a movie
- Mark a movie as `Watched` or `Planned`
- Search/filter movies

### Technologies

Use only:

- HTML
- CSS
- Vanilla JavaScript

Do not use React, Next.js, Bootstrap, Tailwind, jQuery, a backend, or an external database.

## 2. Your Task

Complete/improve the Movie Watchlist application.

### Create
Add a movie with:

- Movie title
- Genre
- Release year
- Status: `Planned` or `Watched`

### Read
Display all movies as cards/list items showing:

- Title
- Genre
- Release year
- Status

### Update
Every movie must have an **Edit** button. Clicking it should allow the user to modify the movie.

### Delete
Every movie must have a **Delete** button. Ask for confirmation before deleting.

### Additional requirements

Implement:

- Search by movie title
- Filter by status
- Responsive UI
- Empty-state message
- Proper form reset
- Meaningful validation
- Clean JavaScript structure

### Bonus

You may additionally implement:

- `localStorage`
- Dark mode
- Sorting
- Movie statistics
- Better animations/UI
- Keyboard accessibility

# 3. Before You Start

Check Git:

```bash
git --version
```

Check your Git identity:

```bash
git config --global user.name
git config --global user.email
```

If needed:

```bash
git config --global user.name "Your Name"
git config --global user.email "your-email@example.com"
```

# 4. Step 1 — Fork the Repository

Open:

https://github.com/trainxdummy/todo

Click:

**Fork → Create fork**

Your fork will look like:

```text
Original:
https://github.com/trainxdummy/todo

Your fork:
https://github.com/YOUR_USERNAME/todo
```

You will work on **your fork**, not directly on the instructor's repository.

# 5. Step 2 — Clone Your Fork

Copy the HTTPS URL of your fork and run:

```bash
git clone https://github.com/YOUR_USERNAME/todo.git
cd todo
```

Check:

```bash
git remote -v
```

`origin` should point to your fork.

# 6. Step 3 — Add the Original Repository as upstream

```bash
git remote add upstream https://github.com/trainxdummy/todo.git
```

Verify:

```bash
git remote -v
```

You should have:

```text
origin    https://github.com/YOUR_USERNAME/todo.git
upstream  https://github.com/trainxdummy/todo.git
```

Remember:

```text
origin   = YOUR fork
upstream = ORIGINAL repository
```

# 7. Step 4 — Update main

```bash
git checkout main
git pull upstream main
```

Always start your work from the latest `main`.

# 8. Step 5 — Create Your Feature Branch

**Never do the assignment directly on `main`.**

Required branch format:

```text
feature/<first-name>-<last-name>-<roll-number>
```

Example:

```text
feature/rahul-sharma-23cs101
```

Create it:

```bash
git checkout -b feature/rahul-sharma-23cs101
```

Verify:

```bash
git branch
```

# 9. Step 6 — Start Coding

Open the project:

```bash
code .
```

Test every feature before submitting.

Check:

- Create
- Read/display
- Edit/update
- Delete
- Search
- Filter
- Validation
- Responsive layout

# 10. Step 7 — Check Git Status

```bash
git status
```

Do not commit unnecessary files such as:

```text
node_modules/
.env
.DS_Store
.idea/
```

# 11. Step 8 — Stage Changes

```bash
git add .
git status
```

Review the staged files before committing.

# 12. Step 9 — Commit

Use meaningful commit messages.

Good:

```bash
git commit -m "feat: add movie CRUD functionality"
```

```bash
git commit -m "feat: implement movie search and filtering"
```

Avoid:

```bash
git commit -m "done"
git commit -m "final"
git commit -m "changes"
```

# 13. Step 10 — Push Your Branch

```bash
git push -u origin feature/rahul-sharma-23cs101
```

Replace the branch with your own.

# 14. Step 11 — Create the Pull Request

Open your fork on GitHub and click **Compare & pull request**.

The PR must be:

```text
FROM:
YOUR_USERNAME:feature/your-name-your-roll-number

TO:
trainxdummy:main
```

Do **not** target your own fork and do not submit `main → main`.

# 15. Pull Request Title

Use exactly:

```text
[FEATURE] First Name Last Name - Roll Number
```

Example:

```text
[FEATURE] Rahul Sharma - 23CS101
```

Do not use vague titles such as:

```text
My PR
Final submission
Assignment
Please check
```

# 16. Pull Request Description

Use this structure:

```markdown
## What did I build?

Implemented the Movie Watchlist application using HTML, CSS and Vanilla JavaScript.

## Features

- Create movie
- Display movies
- Edit movie
- Delete movie
- Search movies
- Filter by status
- Form validation
- Responsive UI

## Bonus Features

- localStorage
- Dark mode

## Testing

I manually tested:

- [x] Create
- [x] Read
- [x] Update
- [x] Delete
- [x] Search
- [x] Filter
- [x] Validation
- [x] Responsive layout

## Screenshots

Add screenshots here.

## Notes

Mention known limitations or anything the reviewer should know.
```

# 17. Add Screenshots

Add screenshots showing useful parts of your application, for example:

1. Initial UI
2. Movie added
3. Edit/update
4. Search/filter
5. Mobile/responsive UI

Drag screenshots into the GitHub PR description.

# 18. Before Creating the PR

Verify:

### Branch

```text
feature/first-name-last-name-roll-number
```

### PR title

```text
[FEATURE] First Name Last Name - Roll Number
```

### Target repository

```text
trainxdummy/todo
```

### Target branch

```text
main
```

### Source

```text
YOUR_USERNAME/your-feature-branch
```

### Description

It should explain:

- What you built
- Features
- Testing
- Screenshots
- Limitations

# 19. After Creating the PR

Do **not** delete your branch.

The instructor may review your PR and leave comments.

If you receive:

> Please fix the delete functionality.

Fix the code on the **same branch**:

```bash
git add .
git commit -m "fix: improve delete functionality"
git push
```

The existing PR updates automatically.

You do not need to create another PR.

# 20. Handling Review Comments

Example:

> Search is not working correctly.

Fix it, then:

```bash
git add .
git commit -m "fix: correct movie search"
git push
```

Then reply to the review:

```text
Fixed. Search now performs case-insensitive matching by movie title.
```

This is the normal code-review workflow.

# 21. Keeping Your Branch Updated

If the original repository changes:

```bash
git checkout main
git pull upstream main
git checkout feature/rahul-sharma-23cs101
git merge main
```

Resolve conflicts if required, then:

```bash
git add .
git commit -m "chore: sync with upstream main"
git push
```

# 22. Common Mistakes

### Do not work directly on main

Bad:

```text
main
```

Good:

```text
feature/rahul-sharma-23cs101
```

### Do not push directly to the instructor repository

Do not use:

```bash
git push upstream main
```

Your normal workflow is:

```text
Original repository
       ↓
     Fork
       ↓
   Your fork
       ↓
 Feature branch
       ↓
     Commit
       ↓
      Push
       ↓
 Pull Request
       ↓
trainxdummy/todo
```

### Do not create multiple PRs for review changes

Use the same branch:

```text
Fix → Commit → Push → Existing PR updates
```

### Do not use meaningless branch names

Avoid:

```text
test
new
changes
final
```

Use:

```text
feature/first-name-last-name-roll-number
```

### Do not use meaningless commit messages

Avoid:

```text
update
done
final
```

Prefer:

```text
feat: add movie CRUD functionality
fix: validate movie release year
```

### Do not include unnecessary files

Avoid:

```text
node_modules/
.env
.idea/
.DS_Store
```

# 23. What You Are Actually Learning

This exercise is bigger than a JavaScript application.

You are learning the basic collaborative development workflow used in professional software teams and open-source projects:

```text
Fork
  ↓
Clone
  ↓
Create Branch
  ↓
Write Code
  ↓
Commit
  ↓
Push
  ↓
Pull Request
  ↓
Review
  ↓
Fix
  ↓
Push Again
  ↓
Approval / Merge
```

A Pull Request is not simply:

> "I uploaded my assignment."

Think of it as:

> "I am proposing a change to someone else's codebase, and I am giving the maintainer enough information to review my change."

# 24. Git Commands Cheat Sheet

```bash
# Clone
git clone <your-fork-url>

# Enter project
cd todo

# Add original repository
git remote add upstream https://github.com/trainxdummy/todo.git

# Check remotes
git remote -v

# Update main
git checkout main
git pull upstream main

# Create branch
git checkout -b feature/first-name-last-name-roll-number

# Check status
git status

# Stage
git add .

# Commit
git commit -m "feat: add movie CRUD functionality"

# Push
git push -u origin feature/first-name-last-name-roll-number

# Check branches
git branch
```

# 25. Final Submission Checklist

- [ ] Repository was forked
- [ ] Repository was cloned
- [ ] `upstream` remote was added
- [ ] Work was done on a feature branch
- [ ] Branch follows the required naming format
- [ ] Nothing was committed directly to `main`
- [ ] Movie can be created
- [ ] Movies can be displayed
- [ ] Movie can be edited
- [ ] Movie can be deleted
- [ ] Search works
- [ ] Filter works
- [ ] Validation works
- [ ] UI is responsive
- [ ] Code is clean
- [ ] No unnecessary files are included
- [ ] Commit messages are meaningful
- [ ] Branch was pushed to your fork
- [ ] PR targets `trainxdummy/todo`
- [ ] PR targets `main`
- [ ] PR title follows the required format
- [ ] PR description is complete
- [ ] Screenshots are included
- [ ] Application was tested before submission

## Happy coding and happy contributing! 🚀
