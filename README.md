# Git Commands and Tagging Guide

## Removing Branches

### Locally:
```bash
git branch -d branch-name
```

#### Force Delete:
If the branch is not merged:
```bash
git branch -D branch-name
```

- `-d` is safe (only deletes if merged).
- `-D` is dangerous (deletes even if unmerged).

### Remotely:
This tells the remote (e.g., GitHub, GitLab) to remove the branch:
```bash
git push origin --delete branch-name
```

---

## Annotated Tags

Annotated tags are the official, full-featured type of Git tags.

- They store metadata like the tagger’s name, email, date, and a custom message.
- They are stored as full objects in Git’s database.
- Best used for marking release versions or important milestones in your project.
- Use annotated tags when you're tagging something important, especially public releases.

**Command:**
```bash
git tag -a v1.7 -m "Version 1.7 release"
```

---

## Lightweight Tags

Lightweight tags are like simple bookmarks to a commit.

- They do not store any metadata or message.
- Just a pointer — think of it like a named commit.
- Useful for local use or quick temporary tagging.
- Use lightweight tags for personal use, testing, or temporary markers that don't need metadata.

**Command:**
```bash
git tag v1.7
```

---

## When to Use Rebase?

- Before merging a feature branch into `main`.
- To clean up your branch history before merging.

---

## Listing Tags

- **List All Tags:**
    ```bash
    git tag
    ```

- **List Tags Matching a Pattern:**
    ```bash
    git tag -l "v1.*"
    ```

- **See More Info About a Tag:**
    ```bash
    git show v1.7
    ```

- **Get Remote Tags:**
    ```bash
    git fetch --tags
    ```

---

## Deleting Tags

- **Delete a Tag Locally:**
    ```bash
    git tag -d tag-name
    ```

- **Delete a Tag Remotely:**
    ```bash
    git push origin --delete tag tag-name
    ```

---

## Photo

![GitHub Logo](images/github.png)