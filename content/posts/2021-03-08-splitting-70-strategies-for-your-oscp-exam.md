---
template: post
title: "Splitting 70: Strategies for your OSCP exam."
slug: strategies-for-taking-the-oscp
socialImage: https://teckk2.github.io/assets/images/offsec-logo.png
draft: false
date: 2021-03-08T01:36:04.776Z
description: Much like the ACT, the OSCP is just as much a matter of knowing how
  to take the exam as it is learning the material itself. If you understand that
  going in, you're much more likely to experience success.
category: OSCP
tags:
  - oscp
  - security
  - pentesting
---
My first OSCP test was two days ago. I ended the exam with 60 points, no certification.

I've been doing some reflecting and I wanted to share, especially since what I've realized goes against traditional advice for those taking the test. Much like the ACT, the OSCP is just as much a matter of knowing how to take the exam as it is learning the material itself. If you understand that going in, you won't make the same mistakes I did on my first attempt.

### Here's a quick summary of my exam:

I was well-prepared and qualified. I rooted both 25-pointers, as well as the 10-point box. I got all of my points in the first 9 hours, which included losing an hour to some technical issues on their side. I made some silly mistakes in my buffer overflow that pushed it from a clean, rigorously-practiced 25 minutes to a 90-minute ordeal. Despite these mishaps, I'm proud of my work on the test. I wrote a 60-line exploit for the 10-pointer that snagged me a reverse shell upon first execution with no debugging whatsoever. The difficult 25-pointer privilege escalation was a breeze, thanks to a tool I'd created prior.

### Lessons learned:

Thinking back though, I made a number of foolish mistakes that cost me the exam.

* There was a Metasploit module available for the 10-point machine, but I decided to be extra and write it from scratch to save my msf use for later. **I never ended up finding another good opportunity to use msfconsole**. Don't be extra - do what gets the task done and gets you certified; use Metasploit where it saves you time.


* I decided to take on the 10-pointer in the first place. By doing so, I went from needing to knock out three machines, to needing to knock out FOUR machines in order to pass. That's a *33% increase* in required targets for victory. The wise move is to do the overflow, the 25-pointer, and your choice of one of the 20-pointers for a clean 70 points and a pass. Taking that route, assuming you have an easy time with buffer overflows, you only have to worry about rooting two machines. That's not so bad!
* After my first 9 hours of generally successful attacks, I spent **FOURTEEN** **HOURS** stumbling back and forth between an impossibly difficult 20-pointer and a doable-but-extremely-hard-to-enumerate 20-pointer. The lesson? Pick your battles. As soon as I realized how difficult one of the 20-pointers was, I should have put all of my focus on the best chance for success. However, common /r/oscp advice is to "avoid falling into rabbit holes and switch machines every two hours!". **Don't do this.** Having taken this advice to heart, I wasted seven hours of my time on a box that I knew in the first 20 minutes of enumeration would be horrible. You have zero obligations to exam machines; spend your energy on the box that will get you to 70 points.
* At a certain point, you may lose the choice to sleep. The *"almost there!"* investment fallacy is real. Sleep makes connections in a way that nothing else does; I woke up post-exam knowing exactly what I had to do to root the busy 20-pointer, and with a novel idea worth trying for the super hard 20-pointer. **Too late.** Appreciate that sleeping is not a pause from your work, it makes mental connections and contributes to your attack in a way that no wakeful thinking can.
* Lastly, I wish I hadn't taken the seemingly universal advice to do the buffer overflow first. Stamina is paramount to success: brainpower and focus are limited. Sleep, food, getting hit with so much information at once... all of that plays a part in the downward slope of your critical thinking as the exam goes on. Your stress will climb with the minute hand on the clock. When you commit to the exam, you should be able to do the buffer overflow sleepwalking, so my advice is to save it for the last 3 hours of your exam. Why spend a completely fresh mind on the one sure win? Dive into the tough puzzles instead, then cash in the last 25 points and drop the mic.