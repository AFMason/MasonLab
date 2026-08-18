# How website changes get published

A plain-language guide for Alex, and anyone else who helps maintain the SBC Lab site later. No prior git or terminal experience needed — Claude Code handles the technical parts. This is just so the words aren't a mystery when they come up.

## The big picture

The whole website is just a folder of text files (plus some photos), sitting in a free storage/hosting service called **GitHub**. There's no database, no server to restart. When the files in that folder change, the live site automatically rebuilds itself from them, usually within a couple of minutes.

## The normal way you'll make a change

Tell Claude Code what you want, in plain English — e.g. *"Add Jessica's bio to her profile"* or *"Change the announcement banner to say we're hiring."* Claude finds the right file(s), makes the edit, and should tell you what changed before doing anything that goes live.

## What "saving" and "publishing" actually mean

- **Saving** (the technical word is "commit") — records a snapshot of the changed files, with a short note describing what changed. Every snapshot is kept forever, so nothing is ever truly lost.
- **Publishing** (the technical word is "push") — sends that snapshot to GitHub, which is where the live site picks up its content from.
- For bigger changes, we'll first put them somewhere separate from the live site (a "branch") so you can look them over before they go live (a "pull request") — think of it as a review step, like a draft before it's posted. Small, low-risk text tweaks can skip that and go straight to the live site.

## How to tell if a change actually went live

- After publishing, GitHub automatically rebuilds the site — this takes roughly 1–3 minutes.
- You can watch it happen at **github.com/AFMason/MasonLab/actions** — a list of "runs," with a green tick for success or a red X if something broke.
- Or just wait a couple of minutes and refresh the live site.

## If something looks wrong

Just tell Claude *"that doesn't look right, can you undo it"* — because every change is a saved snapshot, undoing is always possible, even after something's gone live.

## Where things roughly live

A quick map, for when you're curious or want to describe where something is:

- Most page text lives in a `content/` folder, with one sub-folder per page or person.
- Team member profiles: `content/authors/<their name>/`
- Photos used around the site: `assets/media/`

A separate, more detailed walkthrough on adding your own photos is coming as its own guide.

## A few words you'll hear

You don't need to memorize these — they're here for reference if a term comes up and you want to know what it means.

| Word | Plain meaning |
|---|---|
| Git / GitHub | The free system that stores every version of the site's files and hosts the live pages. |
| Repository ("repo") | The project's folder, tracked by Git — this whole website is one repo. |
| Commit | A saved snapshot of a change, with a short description. |
| Push | Sending saved snapshots to GitHub. |
| Branch | A separate workspace for a change, kept apart from the live site until it's reviewed. |
| Pull request (PR) | A request to merge a branch's changes into the live site, with a chance to review first. |
| Build / deploy | The live site automatically rebuilding itself from the latest files after a push. |
