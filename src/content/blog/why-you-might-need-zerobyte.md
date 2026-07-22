---
title: 'Why you might need ZeroByte'
description: 'A short look at ZeroByte, a self-hosted backup automation tool built on top of restic, and why it might be the missing piece in your homelab.'
pubDate: 'Jul 22 2026'
---

If you self-host anything — a homelab, a media server, a few Docker containers on a VPS — you already know the uncomfortable truth: your backup strategy is probably "I'll set that up later."

[ZeroByte](https://github.com/nicotsx/zerobyte) is an open-source tool that makes "later" a lot easier to turn into "now". It's backup automation for self-hosters, built on top of [restic](https://restic.net/), one of the most trusted backup engines around.

## The problem it solves

restic itself is excellent: encrypted, deduplicated, incremental backups to almost any storage backend. But it's a CLI tool. To use it properly you end up hand-writing cron jobs, wrapper scripts, retention policies, and monitoring — and every one of those is something you can get wrong silently. A backup that fails quietly for six months is worse than no backup, because you *think* you're covered.

ZeroByte puts a web UI and a scheduler on top of restic, so you get the reliability of the engine without maintaining the glue yourself.

## What you get

- **Scheduled backups with retention policies** — define how often to back up and how many snapshots to keep, and it just runs.
- **End-to-end encryption and deduplication** — inherited from restic, so your data is safe even on storage you don't control.
- **Flexible sources and destinations** — back up local directories or network shares (NFS, SMB, SFTP, WebDAV) to local disks, S3-compatible storage like MinIO or Wasabi, and via rclone to 40+ cloud providers including Google Drive and Dropbox.
- **Simple deployment** — it ships as a Docker Compose setup, so it fits naturally into a self-hosted stack.
- **Visibility** — a dashboard that shows whether your backups actually ran, which is half the battle.

## Who is it for?

If you're comfortable writing and maintaining your own restic scripts, you may not need it. But if you want the 3-2-1 backup rule without becoming the full-time maintainer of your own backup infrastructure, ZeroByte hits a nice sweet spot: serious backup technology underneath, minimal effort on top.

Your future self — the one staring at a dead disk — will thank you.
