A better "linux", a Manifesto
=============================

by Emanuel Landeholm (I'm no Torvalds, but I am a programmer and I've been using linux since 1998.)
---------------------------------------------------------------------------------------------------

In order of the random order in which they are presented, here's my solutions:
------------------------------------------------------------------------------

1. Solve dependency hell once and for all
  * Standardize and enforce! (IPC, RPC, exceptions, gettext, sudo, shells, codecs, fullscreen, touch, web, compiler, ...)
  * No more 32/64 bit crap. Provide 64 bit libs only. Code depending on crufty old 32 bit libs must be rewritten.
  * Speaking of which, realize that "unmaintained" is transitive! If your code depends on [unmaintained cruft](http://libjpeg.sourceforge.net/), your code is, effectively, unmaintained.
  * Portability... Fuck that. Target Intel/AMD.
2. No more "flat file" crap. Sqlight-type configuration with schemas only. It is INSANE that a single character error in files like
fstab or sudoers can kill the system irreparably.
3. We need a modern file system. ext4fs is essentially ext2fs with some extra fluff. [Teodore Tso](http://thunk.org/tytso/blog/) [was right in 2008](https://lkml.org/lkml/2008/8/1/217), but I don't think btrfs is a winner.
4. Let xorg crawl up in a corner and DIE. We don't need [stippled lines](http://wayland.freedesktop.org/faq.html#heading_toc_j_6), network transparency, Xresources and Athena widgets. We need one standard, simple display manager from boot to desktop. Canonical abandoned Wayland, but mayber there is still hope?
5. OpenGL... We need a better API! We need shader programming. And software rendering MUST die. It was a stupid idea in 1975 and it still sucks.
6. REAL concurrency. No more threads. No more 4711 different "synchronization primitives", all of which suck.
7. ONE "toolkit", please. Nobody likes context switching between GTK, Qt, AWT, Motif, TK. See how Apple doesn't suck? It's because the UI is consistent.
8. Kill signals and 1970:s style IPC. Exceptions are nice. Something dbus-like would be nice.
10. Enforce a modern, standardized build system. Just say no to #ifndef, m4, autotools and Makefile!
11. Some of that GNU stuff was kinda spiffy. Let's standardize the spiffy stuff and junk [the bad](http://en.wikipedia.org/wiki/Shellshock_%28software_bug%29).
12. Remove kernel dependencies on glibc and gcc. Now.
13. ELF seriously needs to be simplified.

