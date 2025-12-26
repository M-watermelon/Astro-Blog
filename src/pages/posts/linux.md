---
layout: ../../layouts/post.astro
title: "Another Grub Catastrophe"
date: "20 Feb 2025"
desc: " I got a pc upgrade... and my old grub config didn't like that"

---

### Getting to learn a lot about grub, ssds, and luks (again)

Long story short, I had to rewrite the grub config by hand, and while it was a painful process, I sure learned a lot. I also had to dig up and match each UUID to the multiple ssds on my pc, which was... interesting. The *best* part of all, was that my main SSD had an encrypted luks drive setup  ![reaction-emoticon](../../images/bear3.png) so that was *very* fun to sort out. Unfortunately, accessing my windows install is something I haven't fixed yet, mostly because I don't want to deal with the forced migration to Windows 11. (I also don't really care to use Windows anymore, thanks to the wonderful capabilities of Steam Proton in 2025.)