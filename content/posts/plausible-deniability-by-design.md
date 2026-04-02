+++
date = '2026-04-02T00:00:00+02:00'
draft = false
title = 'Plausible Deniability by Design'
tags = ['AI', 'Responsibility', 'Commentary']
categories = ['Society', 'Tech']
+++

### Human in the loop is the new "I have read the Terms and Conditions."

There is a small ritual at the bottom of most software installs and web sign-ups that almost everyone has participated in, and almost no one has performed honestly. You check the box. You click Accept. Somewhere in a legal department, a box has been ticked. Responsibility has been transferred. You agreed. Whatever happens next is, in a very specific and very useful sense, your problem.

Nobody actually reads the Terms and Conditions. This is not a secret. The companies writing them know it. The regulators who accept them as valid know it. The users clicking through them know it. But the system depends on the fiction being maintained — because once you admit that the consent is hollow, you have to ask what exactly the agreement was protecting, and for whom.

I have been thinking about this lately in a different context. A different ritual, but with a recognizable shape.

---

The original idea behind "Human in the Loop" was not unreasonable. It was, in fact, sensible and modest: AI does the work, human checks the work, human decides. The machine accelerates. The person remains responsible. Judgment stays with the species that has judgment. This framing made sense, and it still sounds reasonable when you say it out loud. The trouble is that it was designed for a world where the output volume was manageable. Where a human being could actually read what they were approving. Where "review" was a real activity, not a label.

### That world is disappearing, and not slowly.

The numbers are not hard to find. AI-assisted development has pushed code output up by orders of magnitude in some teams. Where a developer might previously produce a few hundred lines of meaningful code per day, the same developer now ships pull requests of several thousand lines, often generated in minutes. The code works — or at least passes the tests that were also partly generated. The PR gets opened. Someone needs to review it.

### And here is where the ritual begins.

---

Five thousand lines is not a number a human being can review with care in the time a sprint allows. It is a number you can scroll through. You can look for obvious violations. You can check if it compiles, if the tests pass, if the naming conventions are followed. What you cannot do, not really, is understand it — in the sense that would allow you to say, with confidence, that you know what this system will do in production, in edge cases, under load, when misused. That kind of understanding requires time, and depth, and usually the kind of familiarity with the codebase that only comes from having built parts of it yourself.

So people do what people do when they are handed responsibilities they cannot fulfill within the constraints they are given. They adapt. They develop a practiced eye for the surface. They look for red flags. They trust the tests. They trust the CI pipeline. They trust the agent that reviewed the agent's output. And then they click Approve.

I am not describing negligence. I am describing a structural condition. The individual developer reviewing that PR is not being lazy. They are being rational. The amount of output has scaled. The time available for review has not. The formal requirement — that a human approve — remains. What changes is what that approval actually contains.

### The amount of output has scaled. The time available for review has not.

---

This pattern has a name, though it usually gets applied to a different industry. In 2015, Volkswagen's emissions scandal became known under the term Dieselgate -- and the interesting thing about it, the thing that made it structurally interesting and not just a story of corporate fraud, was how the wrongdoing was organized. Nobody, as far as we know, sent a memo. Nobody explicitly instructed the engineers to write defeat device software. What happened was something more ambient: an organization created goals that were mutually exclusive -- pass the emissions test, perform like a real car, hit the price point -- and then left the teams to solve for all three simultaneously. The solution found itself. The people who built it understood what it did. The people above them had plausible deniability. The structure absorbed the deception, and the structure was run by humans who, in some formal sense, had reviewed and approved the work all the way up.

I keep thinking about this structure when I see how AI development responsibility is currently being organized. The company says: you must review everything a human puts into production. The company also says: we need to ship ten times faster than last year. The tooling says: here are five thousand lines, agent-generated, agent-reviewed, ready for your approval. The AI says, in its soft and confident way: I've checked this. It looks good.

### The human is still in the loop. Formally. What loop they are actually in is a different question.

---

The liability architecture here is almost elegant, if you look at it coldly. "A human approved it" is a sentence that closes most investigations before they begin. It distributes responsibility downward to the individual, away from the system. It preserves the AI as a tool -- and tools, historically, have no liability. It allows the organization to maintain that the guidelines were clear and the process was followed, even when the guidelines were practically unenforceable and the process was a simulation of itself.

This is not new in the history of organizations. What is new is the speed and the scale at which the gap between formal and real responsibility can now open. AI scales output. It does not scale the capacity of the human reviewing that output. Responsibility does not scale at all -- it stays with the individual, exactly where it was, while everything around it grows at rates the individual cannot match.

### AI scales output. But it does not scale responsibility.

![AI scales output. But it does not scale responsibility.](/images/ai-scales-output-not-responsibility.png)

The system becomes genuinely unstable when three things align: output exceeds review capacity, time pressure exceeds the tolerance for real care, and individual responsibility stays legally intact. That combination is not a hypothetical future scenario. It is the situation many engineering organizations are building toward right now, often with enthusiasm, often with carefully written process documentation that describes a review process nobody can actually perform as written.

### Compliance becomes simulation.

---

### Human in the Loop becomes a liability illusion.

The comparison to Terms and Conditions is not a joke. It is a structural observation. The ToS regime showed us what happens when consent gets formalized but hollowed out: you create a class of agreements that are legally binding and practically meaningless, and the meaninglessness is an architectural feature rather than a bug, because it protects one party without asking anything real of the other. Click Accept and we're done here.

We are building something similar into the fabric of how software gets made. Human in the Loop, in its current deployment, is often less a safety mechanism than a liability assignment. It allows the system to point to a human at every stage — the developer approved it, the tech lead merged it, the manager signed off on the sprint — without any of those people having had a real chance to exercise the judgment they are being held responsible for.

### We sign off on responsibility for things we can no longer understand.

We sign off on responsibility for things we can no longer understand. The machine does not make the decision, exactly. But it forces us into the position of rubber-stamping it — under time pressure, at volumes we cannot handle, with review tooling that is itself automated, and with the formal requirement of approval still firmly attached to our names.

---

What is uncomfortable about this is not that it's happening. Uncomfortable things happen all the time, and organizations navigate them. What is uncomfortable is the resemblance to every pre-scandal structure in retrospect: officially, everything clean. Unofficially, everyone involved knows the process doesn't work as described. Nobody wants to be the person who says it out loud, because saying it out loud makes you responsible for the gap you've just named. So the gap stays unnamed. The ritual continues. The boxes get checked.

Plausible deniability by design is a phrase that sounds deliberately sinister, but it doesn't require deliberate sinister intent. It just requires that the incentives point in one direction and the accountability mechanisms point somewhere else, and that nobody involved has a particular interest in reconciling the two.

The original Human in the Loop idea was not wrong. Keeping humans in meaningful contact with consequential decisions is a real value, and a defensible one. The problem is that "in the loop" has quietly become a positional description rather than a functional one. The human is there. The loop exists. What the human can actually do within it — what they can realistically check, understand, catch, or refuse — that question is not being asked loudly enough.

And the thing about rituals, the thing that makes them durable even when they've lost their original meaning, is that they look exactly the same from the outside whether anyone is home or not.

### We are turning responsibility into a ritual.

---

The autonomous vehicle industry has been circling a version of this question for years. When a self-driving car causes an accident, who is responsible? The manufacturer? The software vendor? The owner? The passenger who didn't intervene? Regulators and insurers have not resolved this. What they have done, in most jurisdictions, is preserve the ambiguity — because resolving it would require someone to accept liability that nobody wants to accept. The question of who is in the loop, and what being in the loop actually requires of them, turns out to be surprisingly hard to answer when the answer has consequences.

### Who is in the loop? Ask again when something breaks.
