---
title: 'Why you might need ZeroByte'
description: 'ZeroByte is a mobile-first personal storage system I''m working on: extend your phone''s storage with hardware you own, and keep using your files as if they never left.'
pubDate: 'Jul 22 2026'
---

Phones run out of storage. Photos, 4K videos, WhatsApp and Telegram media, downloads — years of personal data pile up until the "storage almost full" warning becomes a lifestyle.

The usual ways out are all unsatisfying. You can keep buying phones with more storage. You can pay Google One or iCloud rent forever. You can copy everything to an external disk and lose convenient access to it. Or you can set up Nextcloud, a Synology, or a NAS — which is powerful, but often feels like administering a server rather than extending a phone.

**ZeroByte** is a project I'm working on that tries to offer another choice: a mobile-first personal storage system that extends your phone's storage using hardware *you own*. Buy a large disk once, connect it to a small device at home, and use it from your phone almost as naturally as internal storage. Move hundreds of gigabytes off your phone — and keep browsing, searching, streaming, and restoring those files as if they never really disappeared.

## Not a cloud, not a NAS

Compared to **traditional cloud storage**, the difference is ownership. With iCloud or Dropbox, your data lives on someone else's infrastructure and you rent capacity month after month. With ZeroByte, your files live on your own disk: no subscription for gigabytes, no dependency on a provider's policies or pricing, real privacy because the originals never leave hardware you control, fast transfers over your local network, and full offline operation at home — it works even when your internet doesn't.

Compared to a **self-hosted cloud**, the difference is framing. Nextcloud and NAS apps say: "here is your private server and some cloud-like apps." ZeroByte says: "here is extra storage for your phone that happens to live in your home." No Docker, no port forwarding, no reverse proxies. Connect the device, install the app, pair the phone, move files, free up space. The server exists to serve the phone — not the other way around.

## Storage extension, not sync

Most tools in this space are built around synchronization: keeping copies aligned across devices. ZeroByte's primary action is different — *safely place a file on ZeroByte and remove the phone copy*. It's closer to storage tiering: your phone is the fast, limited tier; your disk is the large, owned tier. A 20 GB video can leave your phone entirely while remaining visible and playable from the same interface.

A few principles make that seamless:

- **One merged library.** Local and remote files appear together. Half your camera roll on the phone, the older half on ZeroByte — you see one timeline and never have to remember where each photo lives.
- **Open without downloading.** Stream a video, view a photo, or read a document straight from your disk, without needing enough free phone space to restore it first.
- **Your folder structure is preserved.** `DCIM/Camera`, `Download`, your WhatsApp media — files keep their original paths on the disk. Your backups stay readable with an ordinary file manager, and if the app disappeared tomorrow, your data would still be yours. No lock-in.
- **Deterministic by design.** You always know where a file physically is, whether it's been safely copied, and what a restore will do. Duplicates are never silently overwritten — identical content is deduplicated, conflicting content is preserved. Backing up and freeing space are explicit, separate intentions.

## The point

Cloud storage asks you to rent your own memories back. Self-hosted clouds ask you to become a sysadmin. ZeroByte's bet is that there's room for something in between: storage you own, with the polish of a consumer product — a phone that simply never feels full again.

I'll be sharing more about ZeroByte's design and internals here as the project evolves.
