# 📝 MY_WORK: Student Information, Development Log, Reflection & Answers

> This is the **only file** your instructor reads to grade Parts 3 and 4 (documentation and video). Everything you write here must be **in your own words**.

---

## 🛑 STOP: Read This Before You Do Anything Else

> ### 1️⃣ Read the whole `README.md` first
> The `README.md` in this repository contains the full instructions: how this assignment continues Assignment 1, the Chapter 5 recap, class descriptions, feature specifications, question prompts and the video script. **If you skip it, you will lose marks.**
>
> ### 2️⃣ Understand the full code before answering any question
> Open `SchedulerSimulationSync.java` and read it **from top to bottom**. You must be able to explain what `SharedStats`, `ReadyQueue`, `CpuWorker`, `RaceWindow.pause()`, `ReentrantLock` and `Semaphore` do **before** you write a single answer in Parts B and C. **Run the original starter first** (it is intentionally broken) and **save its output**: you need it for Question 1 of Part C.
>
> ### 3️⃣ Use only the code of this repository
> Work **only** on `SchedulerSimulationSync.java` from this repository. Do **not** copy or paste code from your previous assignments.
>
> ### 4️⃣ Commit many times, not once
> A single commit, or all commits made in the last hour, costs you **-0.5 mark**. See the [Commit Rules](#-commit-rules-mandatory) below.

**How to use this file:**
1. Fill in your **Student Information** (below) right now.
2. Follow the steps in the **Work Roadmap** in order.
3. Update the **Development Log** *every time* you work on the assignment, not at the end.
4. Do not delete any section header. Replace the `[...]` placeholders with your own text.

---

## 👤 Student Information

> ⚠️ **WARNING:** Fill this in first. Your name and ID must match the student ID you set in `SchedulerSimulationSync.java` (line 304) and the one you say in your video.

| Field | Your Answer |
|-------|-------------|
<<<<<<< HEAD
| **Full Name** | Almas Abdullah Almutairu |
| **Student ID** | 446051602 |
| **University Email** | 446051602@std.psau.edu.sa |
| **GitHub Username** | Almas-4 |
=======
| **Full Name** | Almas Abdullah Almutairui |
| **Student ID** | 446051602 |
| **University Email** |446051602@std.psau.edu.sa |
| **GitHub Username** | Almas-4  |
>>>>>>> 8fc189da0b88c0e9a746f71e93da74b1176491a3
| **Repository Link** | https://github.com/Almas-4/OS-Assignment3-Almas-Almutairu |
 
---

## 🎥 Video Link

**Video Link**: [Paste your video link here]

> ⚠️ **WARNING:** The video must be **publicly accessible** ("Anyone with the link can view") on **Google Drive**, **YouTube (Unlisted or Public)** or any other cloud file-sharing system. A private, restricted or broken link counts as a **missing video (-1 mark)**.
>
> 💡 **TIP:** Open the link in a **private/incognito window** before you submit. If it asks you to log in or request access, it is not public.
>
> 📌 **NOTE:** The link goes in **this file only** (`MY_WORK.md`), **not** in `README.md`. Name your video file `StudentID_Assignment3_Demo.mp4`. It must last **2 to 3 minutes**.

---

## 🗺️ Work Roadmap (follow in this order)

| Step | What to do | Where | Marks |
|:----:|------------|-------|:-----:|
| 0 | Read `README.md`, read the full code, **run the original starter and save its output** (it fails on purpose) | Your IDE | – |
| 1 | Fork, rename, keep the repo **PUBLIC**, set your student ID (line 304), **commit** | GitHub + code | Part 1 (1) |
| 2 | Feature 1: Mutex lock on the ready queue, **commit** | Code | Part 2 (0.25) |
| 3 | Feature 2: Mutex lock(s) on the shared statistics, **commit** | Code | Part 2 (0.25) |
| 4 | Feature 3: Counting semaphore instead of busy waiting, **commit** | Code | Part 2 (0.5) |
| 5 | Development Log (5+ entries, different dates) | This file, Part A | Part 3 (0.5) |
| 6 | Reflection (4 questions) | This file, Part B | Part 3 (0.5) |
| 7 | Technical Answers (4 questions) | This file, Part C | Part 3 (0.5) |
| 8 | Record the video, upload it, paste the link above | Video + this file | Part 4 (1.5) |
| 9 | Final check, then submit the repo link on Blackboard | Blackboard | – |

> 💡 **TIP:** Tick each step off as you go. Do not leave the log, the reflection or the video for the last day.

---

## 🔁 Commit Rules (MANDATORY)

> ### ⚠️ MANY COMMITS ARE REQUIRED. A single bulk commit is penalized (-0.5 mark).

**Minimum: 4 meaningful commits. Aim for 7 or more.**

| # | Commit | Example message |
|:-:|--------|-----------------|
| 1 | Student ID set | `Set my student ID: 441234567` |
| 2 | Feature 1: Ready queue lock | `Feature 1: Protected the ready queue with a ReentrantLock` |
| 3 | Feature 2: Statistics locks | `Feature 2: Added locks to the shared statistics counters` |
| 4 | Feature 3: Semaphore | `Feature 3: Replaced busy waiting with a counting semaphore` |
| 5 | Development log entries | `Docs: Added development log entries 1-3` |
| 6 | Reflection and answers | `Docs: Completed reflection and technical answers` |
| 7 | Video link | `Docs: Added demo video link` |

**Rules:**
- ✅ **One commit per feature.** Do not put all three features in one commit.
- ✅ **Commit after each work session**, and after each part of this file.
- ✅ **Spread your commits over different dates.** Not all in one day.
- ❌ **Do not make all commits in the last hour** before the deadline (November 14, 2026).
- ❌ **No vague messages** like `done`, `update` or `final version`.

> 💡 **TIP:** Your commit history is checked and you **show it in your video** (at least 4 commits visible). Your development log dates should match your commit dates.
>
> 💡 **TIP:** **Use VS Code** (see *Recommended Development Environment* in `README.md` for the full setup). Sign in to GitHub in VS Code, then commit from the Source Control panel (Ctrl+Shift+G) → stage → write a message → Commit → Sync/Push. You can edit and commit this file the same way. **Pushing** matters: commits that are not pushed to GitHub are invisible to the instructor.

---

# Part A: Development Log (0.5 mark)

> ⚠️ **WARNING:** Minimum **5 entries**, spread over **different dates**. Five entries written on the same day, or written all at once at the end, will lose marks and look like a copy. Entry dates should be **between the start of the assignment and the deadline (November 14, 2026)**.
>
> 💡 **TIP:** Write an entry at the **end of each work session**, while you still remember what happened. It takes 5 minutes.
>
> 💡 **TIP:** Be specific. "Worked on the code" is a weak entry. "Added a `ReentrantLock queueLock` to `ReadyQueue` and wrapped the body of `poll()` in `lock()` / `try` / `finally { unlock() }`" is a strong one.
>
> 📌 **NOTE:** Each entry needs: date and time, what you did, details, challenges, solution, and time spent. Real challenges are fine (and expected). Do not invent fake ones.

## Example Entry (do not copy it, write your own)

### Entry 1 - [November 2, 2026, 4:30 PM]
**What I did**: Forked the repository, set my student ID, and ran the original starter

**Details**:
- Forked the starter repository and renamed it
- Changed student ID on line 304 to my actual ID (441234567)
- Ran the original program: 4 CPUs started, three of them picked `P1`, then `IllegalThreadStateException` and the watchdog stopped the program
- Saved the output in a text file for Question 1
- Committed and pushed: `Set my student ID: 441234567`

**Challenges**: I did not understand why the same process was picked by three CPUs

**Solution**: Read `ReadyQueue.poll()` again and found the `RaceWindow.pause()` between reading the head and removing it

**Time spent**: 45 minutes



## Your Development Log

### Entry 1 - [November 9, 2026, 6:00 PM]

What I did: Forked the starter repository, renamed it, set it to public, and set my student ID.

Details:

Cloned the repository in VS Code
Changed studentID to 446051602 and committed Change student ID in SchedulerSimulationSync
Read the README and the code, and ran the original starter

Challenges: The starter crashed with IllegalThreadStateException, and the verification block still showed all ✔.

Solution: Understood that CPU-2 died and CPU-1 finished all processes alone. The real bug was poll() with RaceWindow.pause().

Time spent: 1.5 hours


### Entry 2 - [November 13, 2026, 5:00 PM]

What I did: Feature 1, the lock on the ready queue.

Details:Added ReentrantLock queueLock in ReadyQueue
Protected add(), poll(), processOf() and snapshot() with lock() / try / finally { unlock() }
Committed Feature 1: Protected ready queue

Challenges: I was not sure where unlock() goes in poll(), which has return statements.

Solution: Kept the return statements inside try, because finally still releases the lock.

Time spent: 1.5 hours


### Entry 3 - [November 13, 2026, 9:00 PM]

What I did: Feature 2, the locks on the shared statistics.

Details:Added contextSwitchLock, completedLock and serviceTimeLock in SharedStats
Protected the 3 update methods and the 3 getters
Committed Feature 2: Added locks to the shared statistics counters

Challenges: Choosing between one lock and one lock per variable.

Solution: Chose one lock per variable because the three counters are independent.

Time spent: 1.5 hours


### Entry 4 - [November 14, 2026, 12:30 AM]

What I did: Feature 3, the counting semaphore and the clean shutdown.

Details:Added Semaphore readyCount = new Semaphore(0) in ReadyQueue
release() in add() and acquire() at the start of the CpuWorker loop
Deleted the polling code and added release(SharedStats.totalCPUs) at the end
Committed Feature 3: Replaced busy waiting with a counting semaphore

Challenges: A CPU stayed blocked in acquire() at the end, and incrementContextSwitch() was missing its lock() call.

Solution: Added the shutdown signal and the exit check after acquire(), and added the missing lock(). All four verification lines became ✔.

Time spent: 2 hours



### Entry 5 - [November 14, 2026, 10:00 AM]

What I did: Completed the written parts of MY_WORK.md.

Details:Wrote the reflection (4 questions) and the technical answers (4 questions)
Pasted the starter output and my final verification block in Part C, Question 1
Ran the final program 5 times: all four lines ✔ every time
Committed and pushed Docs: Completed MY_WORK.md

Challenges: Explaining the lost update step by step with two named CPUs.

Solution: Used a small timeline with contextSwitchCount = 12: CPU-1 reads 12, CPU-2 reads 12, both write 13, one increment is lost.

Time spent: 2 hours

### Entry 6 - [November 14, 2026, 12:00 PM]

What I did: Recorded the demo video, uploaded it, and did the final check.

Details:Recorded the video from VS Code (name, ID, repository, 3 features, run with the verification block, one concept, commit history)
Uploaded it and set the link to “Anyone with the link can view”
Tested the link in an incognito window
Added the link to MY_WORK.md, pushed it, and submitted the repository link on Blackboard

Challenges: Keeping the video between 2 and 3 minutes and showing the verification block clearly.

Solution: Wrote a short script, rehearsed it with a timer, and paused on the verification block for a few seconds.

Time spent: 1.5 hours



## Development Log Summary

> 💡 **TIP:** Fill this in **last**, after all entries are written.

Total time spent on assignment: about 10 hours

Most challenging part: Feature 3, the initial value of the semaphore and the shutdown of the blocked CPUs.

Most interesting learning: A program can print correct totals while a race condition still exists, because CPU-2 crashed and CPU-1 did all the work alone.

What I would do differently next time: Start earlier, test each lock method right after writing it, and write each log entry at the end of the session.

# Part B: Reflection (0.5 mark)

> 🛑 **STOP:** Do **not** start this part until you have read the `README.md`, read the **entire** `SchedulerSimulationSync.java`, run it, and finished the three features.
>
> ⚠️ **WARNING:** Each answer must be **5 to 7 sentences**, in **your own words**. Copied or AI-generated answers without understanding get **0 marks for the whole assignment**. You may be asked to explain them in person.
>
> 💡 **TIP:** Mention concrete things you actually did: a method you wrote, an error you hit, a line of output you saw. Generic answers score low.
>
> 💡 **TIP:** Draft your answer in a few bullet points first, then turn them into sentences.

## Question 1: What did you learn about synchronization?

> 💡 **TIP:** Talk about race conditions (read-modify-write), critical sections, mutual exclusion with `ReentrantLock` and `try/finally`, the role of a counting semaphore, and what surprised you when the starter failed.

**Your Answer:** *(5-7 sentences)*

I discovered that two threads may lose an update because count++ is a read, modify, and write. When two CPUs selected P1 and CPU-2 crashed, I witnessed it in the beginning. Mutual exclusion on a critical section is provided by a ReentrantLock, and unlock() must be in a finally block. Instead of busy waiting, a counting semaphore allows a thread to block. I also learned that correct output does not always mean the code is free from race conditions.

## Question 2: What was the most challenging part of this assignment?

> 💡 **TIP:** Pick **one** specific challenge (understanding why the starter failed, choosing the lock granularity, the initial value of the semaphore, the shutdown of the CPUs, Git, the video) and say *why* it was hard.

**Your Answer:** *(5-7 sentences)*

Feature 3 was the hardest part. Since the queue begins empty, the starting value had to be 0. One CPU ultimately remained stopped in acquire() indefinitely. Because concurrency issues rely on timing, it was difficult to locate. In order to prevent a deadlock, I also had to refrain from executing acquire() while holding queueLock.The trade-off is that more locks are harder to manage, while one lock is simpler but makes unrelated updates wait. Progress holds because a free lock is given to a thread that asks for it.

## Question 3: How did you overcome the challenges you faced?

> 💡 **TIP:** Describe your method: reading the slides and the documentation, adding `System.out.println` to debug, running the program many times, re-reading the README, testing after each small change, asking for help.

**Your Answer:** *(5-7 sentences)*

I adhered to the README sequence, which is queue, statistics, and semaphore. I repeatedly ran the application and examined the verification block following each feature. I solved the problem by releasing permits for all CPU threads at shutdown, so blocked threads could wake up and exit. I went over the semaphores presentations and textbook chapters again. I fixed the missing lock() in incrementContextSwitch() after reviewing my code.


## Question 4: Where can synchronization concepts be applied in real-world applications?

> 💡 **TIP:** Use real applications you know (banking and money transfers, ticket or seat booking, a shared counter on a website, a print queue, a database) and connect each one to what you built here (shared data, critical section, lock or semaphore).

**Your Answer:** *(5-7 sentences)*

In order to prevent two transfers from updating a single balance simultaneously, banks require locks. In order to prevent a seat from being sold twice, seat reservations require mutual exclusion. Shared structures like the ready queue are safeguarded by operating system kernels. A counting semaphore can be used by a web server to restrict connections. A producer-consumer issue is a print spooler.

### Optional: What would you like to learn more about?

[Any topics related to synchronization or operating systems that you're curious about?]

### Optional: How confident do you feel about synchronization concepts now?

[Beginner / Intermediate / Confident. What do you understand well? What needs more practice?]

### Optional: Feedback on the assignment

[Any comments? Was it helpful? Too easy or hard? Suggestions?]

---

# Part C: Technical Answers (0.5 mark)

> 🛑 **STOP:** You cannot answer these questions without understanding the code. Re-read `SchedulerSimulationSync.java` and **run it** first. Your answers must reference **your own code and your own output** (your student ID makes your output and your expected values unique).
>
> ⚠️ **WARNING:** Each answer must be **3 to 5 sentences**, with specific examples from your code or output. Use correct terms: race condition, critical section, mutual exclusion, mutex lock, semaphore, busy waiting, deadlock, producer, consumer.
>
> 💡 **TIP:** Keep the output of the **original starter** and the output of your **final version** in text files or screenshots, so you can copy real snippets for Question 1.

## Question 1: Race Condition in Your Own Output

**Question**: Run the **original starter** (before any fix) and paste the **verification block** of that run. Which value was wrong (expected vs observed)? Explain **step by step**, with two named threads/CPUs, how **one lost update** happens on one of the shared variables (read, `RaceWindow.pause()`, write). Why can the same bug happen on a real machine even without `RaceWindow`, and why is it hard to detect?

> ⚠️ **WARNING:** The snippet must come from **your own run** (with your student ID), not from a classmate or from this README.
>
> 💡 **TIP:** Use a small timeline: *CPU-1 reads `contextSwitchCount` = 12 → CPU-2 reads 12 → CPU-1 writes 13 → CPU-2 writes 13 → one increment is lost.* If your starter run crashed before printing numbers, run it several times (or paste the exception and the watchdog message and explain it).

Both CPU-1 and CPU-2 printed selections P1 in my initial run. Then, an IllegalThreadStateException caused CPU-2 to crash. Since CPU-1 performed all 18 processes by itself and CPU-2 died, there was no value error in the verification block. Because count++ is read, add, and write and another core may operate in between, the identical error might occur on a real computer. Because the window is so short, it is difficult to identify, making the failure uncommon and sporadic.

Verification block of the **original starter**:
┌─ [CPU-1] picks P1
┌─ [CPU-2] picks P1
Exception in thread "CPU-2" java.lang.IllegalThreadStateException
        at java.base/java.lang.Thread.start(Unknown Source)
        at CpuWorker.run(SchedulerSimulationSync.java:283)

``┌─ [CPU-1] picks P1
┌─ [CPU-2] picks P1
Exception in thread "CPU-2" java.lang.IllegalThreadStateException
        at java.base/java.lang.Thread.start(Unknown Source)
        at CpuWorker.run(SchedulerSimulationSync.java:283)

Context switches (quanta executed)     expected 40       observed 40       ✔
Completed processes                    expected 18       observed 18       ✔
Total service time (ms)                expected 153708   observed 153708   ✔
Busy-waiting polls (must be 0)         expected 0        observed 0        ✔

Verification block of **my final version**:

```Context switches (quanta executed)     expected 40       observed 40       ✔
Completed processes                    expected 18       observed 18       ✔
Total service time (ms)                expected 153708   observed 153708   ✔
Busy-waiting polls (must be 0)         expected 0        observed 0        ✔
✔ All shared values are consistent.
```

**Explanation of the timeline:**
contextSwitchCount is 12.
CPU-1 reads tmp = 12, then RaceWindow.pause().
CPU-2 also reads tmp = 12.
CPU-1 writes 13, then CPU-2 writes 13.
The counter is 13 instead of 14, so one increment is lost.

## Question 2: Critical Sections and Lock Granularity

**Question**: List the **critical sections** you protected (variables and methods) and the lock(s) you used. **Lock granularity:** did you use **one lock** for the three statistics or **one lock per variable**? Why, and what is the trade-off? Why is the **ready queue** protected by a **different** lock than the statistics? Explain how your solution provides **mutual exclusion**, and discuss **progress** and **bounded waiting** (a default `ReentrantLock` is not fair: what does that imply?).

> 💡 **TIP:** The three counters are independent: does updating `contextSwitchCount` need to block an update of `totalServiceTime`? Also think about what could go wrong (deadlock, or long waiting) if the queue lock and the statistics lock were the **same** lock and a thread held it while doing something slow.

**Your Answer:** *(3-5 sentences)*

I used queueLock to protect the ReadyQueue methods: add(), poll(), processOf(), and snapshot(). I used three separate locks to protect the statistics counters and their getters. This allows independent counters to be updated without blocking each other. The separate queue lock protects different shared data. The default ReentrantLock is not fair, so bounded waiting is not guaranteed.

| Critical section (variable / method) | Lock used | Why it needs protection |
|---|---|---|
| `ReadyQueue` methods (`list`, `map`) | `queueLock` | shared queue changes together |
| `contextSwitchCount` updates and reads | `contextSwitchLock` | lost update |
| `completedProcessCount` updates and reads | `completedLock` | lost update |
| `totalServiceTime` updates and reads | `serviceTimeLock` | lost update |

## Question 3: Busy Waiting vs Semaphore

**Question**: Describe the **busy waiting** of the starter and its cost (give the `Busy-waiting polls` number from your **starter** run). What does the **value of your semaphore** represent? What is its **initial value** and why? What is its value right after the `numProcesses` initial `add()` calls? Why does the last CPU call `release(totalCPUs)` at the end, and what would happen if it did not?

> 💡 **TIP:** Think about what a CPU does when the queue is empty in the starter, and what a CPU does in your final version (is it running, ready or blocked?). Also check what happens to a CPU blocked in `acquire()` when no process will ever be added again.

**Your Answer:** *(3-5 sentences)*

In the starter, a CPU with an empty queue added to busyWaitPolls, slept 20 ms, and tried again. This is busy waiting, and it wastes CPU time. In my starter run Busy-waiting polls was 0, because CPU-2 had crashed. My semaphore readyCount is the number of processes waiting in the queue. Its initial value is 0 because the queue starts empty, and it is 18 after the 18 initial add() calls. The last CPU calls release(totalCPUs) to wake the blocked CPU, and without it that CPU would wait forever and the watchdog would stop the program.

## Question 4: Classical Problems and Deadlock

**Question**: The CPUs and the ready queue look like a classical synchronization problem of Chapter 5. **Name it**, and say who plays the **producer** and the **consumer** roles (careful: here the CPUs also re-enqueue processes). If the ready queue were **bounded** (capacity `K`), name the **three semaphores** you would need and their **initial values**. Describe a **deadlock scenario** that appears if a thread acquired the **mutex before** waiting on the semaphore (or if two locks were acquired in different orders), and say **which of the four necessary conditions** you would break to prevent it.

> 💡 **TIP:** Recall the bounded-buffer solution of the slides (`empty`, `full`, `mutex`) and the order of `wait()` calls in the producer and the consumer. For the deadlock, think about a producer that holds the mutex while waiting for a free slot that only a consumer (who needs the mutex) can create.

**Your Answer:** This is the producer-consumer (bounded-buffer) problem. The CPUs take processes from the queue, and main and the CPUs add processes to it. With a bounded queue, a producer that takes the mutex before waiting on empty would hold the mutex while the queue is full. A consumer needs that mutex to free a slot, so both would wait forever. I would prevent this by breaking hold and wait: wait on the semaphore first, then take the mutex.

**Classical problem and roles**:
Producer-consumer (bounded buffer). The consumers are the CPUs calling poll(). The producers are main (the initial add() calls) and the CPUs (they re-enqueue unfinished processes). So each CPU plays both roles.

**Semaphores for a bounded queue (name and initial value)**:
-mutex = 1 (mutual exclusion on the queue)
-empty = K (free slots)
-full = 0 (occupied slots)

**Deadlock scenario and prevention**:
The producer does wait(mutex) before wait(empty). The queue is full, so it holds the mutex and waits for a free slot. A consumer needs the mutex to remove an item and call signal(empty), so nobody can continue. I would break the hold and wait condition by calling wait(empty) before wait(mutex).

## Summary

**Key concepts I understood through these questions:**
1. a race condition is a lost update, 
2. a mutex lock gives mutual exclusion and unlock goes in finally, 
3. a semaphore replaces busy waiting and needs a shutdown signal.

**Concepts I need to study more:**
1. fair locks and starvation
2. deadlock detection.

---

# ✅ Final Checklist (complete before submitting)

> ⚠️ **WARNING:** Go through every line. Blackboard does not accept submissions after the deadline, which is **November 14, 2026**.

**Repository**
- [ ] Repository is **PUBLIC** (Settings → Danger Zone → Visibility)
- [ ] Repository is renamed to `OS-Assignment3-YourFirstName-YourLastName`
- [ ] GitHub account uses the university email (`@std.psau.edu.sa`)

**Code**
- [ ] Student ID is set in `SchedulerSimulationSync.java` (line 304)
- [ ] My code is based **only** on the starter of this repository (nothing copied from previous assignments)
- [ ] Code compiles and runs with no errors, and terminates by itself (no `⛔ WATCHDOG`)
- [ ] Feature 1 (ready queue lock), Feature 2 (statistics locks) and Feature 3 (semaphore, no busy waiting) all work
- [ ] **The four verification lines are ✔ in 5 consecutive runs**
- [ ] Every lock is released in a `finally` block
- [ ] `RaceWindow`, `Config`, the verification block and the watchdog are **unchanged**
- [ ] Each feature has clear comments

**Commits**
- [ ] **At least 4 meaningful commits, ideally 7 or more**
- [ ] **One commit per feature**
- [ ] Commits are spread over **different dates** (not all in the last hour)
- [ ] Everything is **pushed** to GitHub

**This file (`MY_WORK.md`)**
- [ ] Full name and student ID filled in at the top
- [ ] Development log has **5+ entries** on different dates
- [ ] Reflection: 4 questions, 5-7 sentences each
- [ ] Technical answers: 4 questions, 3-5 sentences each, with examples from **your** output (starter output **and** final output pasted in Question 1)
- [ ] No `[...]` placeholders left
- [ ] No section headers deleted

**Video**
- [ ] 2-3 minutes long, named `StudentID_Assignment3_Demo.mp4`
- [ ] Shows your name, ID, repository, 3 features (and your lock granularity choice), IDE execution with the verification block, one synchronization concept, and commit history
- [ ] Link is **public** (tested in an incognito window) and pasted in the **Video Link** section above

**Blackboard**
- [ ] Submit **only** the link to your public GitHub repository

> 🎯 **Good luck!** Start early, commit regularly, and make sure you can explain every line you submit.
