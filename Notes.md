# Initialize Git Repository

```bash
git init
```

---

# First Commit

```bash
git add .
git commit -m "Initial project setup"
```

---

# Git Commands

| Command        | Purpose                 |
| -------------- | ----------------------- |
| `git status`   | Check repository status |
| `git add .`    | Stage files             |
| `git commit`   | Save snapshot           |
| `git push`     | Upload changes          |
| `git pull`     | Download latest changes |
| `git checkout` | Switch branches         |
| `git merge`    | Merge branches          |
| `git rebase`   | Reapply commits         |

---

# Create Branch

```bash
git checkout -b feature/navbar
```

OR

```bash
git switch -c feature/navbar
```

---

# Add Feature

## Add Navbar

### index.html

```html
<nav>
  <a href="#">Home</a>
  <a href="#">About</a>
  <a href="#">Contact</a>
</nav>
```

### style.css

```css
nav {
  display: flex;
  gap: 20px;
  margin-bottom: 20px;
}

nav a {
  text-decoration: none;
  color: black;
  font-weight: bold;
}
```

---

# Commit Changes

```bash
git add .
git commit -m "Added navbar feature"
```

---

# Push Changes

```bash
git remote add origin <repo-url>
git push -u origin feature/navbar
```

---

# Local vs Remote vs Origin

| Type          | Meaning                   |
| ------------- | ------------------------- |
| Local Branch  | Exists on your computer   |
| Remote Branch | Exists on GitHub          |
| origin        | Default remote repository |
| Other Remote  | Additional repositories   |

---

# Merge Branch

```bash
git checkout main
git merge feature/navbar
```

---

# Create Merge Conflict

## In Main Branch

Change:

```html
<h1>Git Training Demo</h1>
```

To:

```html
<h1>Git Workshop Main Branch</h1>
```

Commit changes.

---

## In Feature Branch

Change same line:

```html
<h1>Git Training With VS Code</h1>
```

Commit changes.

---

# Merge Conflict Example

```text
<<<<<<< HEAD
Git Workshop Main Branch
=======
Git Training With VS Code
>>>>>>> feature/navbar
```

---

# Resolve Conflict

1. Edit conflicting file
2. Remove conflict markers
3. Save file

Then:

```bash
git add .
git commit
```

---

# Rebase

## Create New Branch

```bash
git checkout -b feature/footer
```

Add footer and commit.

---

## Rebase

```bash
git checkout feature/footer
git rebase main
```

---

# Merge vs Rebase

## Merge

```text
A---B---C main
     \
      D---E feature
           \
            M merge commit
```

## Rebase

```text
A---B---C---D'---E'
```

---

# Revert

## Undo Commit Safely

```bash
git revert <commit-id>
```

---

# Restore File

```bash
git restore index.html
```

---

# VS Code Git Features

## Source Control Panel

Features:

- Staging changes
- Commit messages
- File tracking

---

## Diff Viewer

Shows:

- Added lines
- Removed lines
- Modified lines

---

## Branch Switching

Bottom-left branch selector in VS Code.

---

## Conflict Resolution UI

VS Code options:

- Accept Current
- Accept Incoming
- Accept Both
- Compare Changes

---

# GitLens

## Install GitLens Extension

Features:

- Line blame
- Commit history
- Repository graph
- Compare changes
- Author tracking

---

# Recommended Class Flow

```text
Developer gets task
    ↓
Creates branch
    ↓
Adds feature
    ↓
Commits changes
    ↓
Pushes code
    ↓
Another developer changes same file
    ↓
Merge conflict happens
    ↓
Conflict resolved
    ↓
Rebase for clean history
```

---

# Best Practices

- Commit frequently
- Write meaningful commit messages
- Pull latest changes before starting work
- Avoid committing unnecessary files
- Use `.gitignore`
- Keep branches small and focused

---

# Practice Exercise

## Task

1. Create branch
2. Add feature
3. Commit changes
4. Push branch
5. Create merge conflict
6. Resolve conflict
7. Rebase branch
8. Merge into main

---

# Conclusion

Git helps teams:

- Collaborate efficiently
- Track code history
- Manage versions safely
- Resolve conflicts
- Maintain clean project history

Git is an essential tool for modern software development.
