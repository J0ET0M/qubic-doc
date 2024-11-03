# Qubic Core Technology

it seems that we currently have the proposal season, i hope we can discuss togehter another proposal.
in the past 2.5 years, qubic developement was mainly made by volunteers, enthusiasts and of course cfb.

> [!Note]
> This is a draft to be discussed. i tried to bring together all information needed to have a fact based discussion.
> I'm happy to respond to your questions.

**Content**
1. [The Hard Numbers](#the-hard-numbers-ultra-short-version)
2. [The History](#the-history)
3. [The Proposed Change](#the-proposed-change)
   1. [What are the assignments of Qubic Core Technology](#what-are-the-assignments-of-qubic-core-technology)
   2. [What changes in the structure?](#what-changes-in-the-structure)
   3. [Why should we remove **Client**?](#why-should-we-remove-client)
   4. [How will the progress be tracked?](#how-will-the-progress-be-tracked)
   5. [What is the timeline?](#what-is-the-timeline)
   6. [What will be the proposal to the Computors?](#what-will-be-the-proposal-to-the-computors)

## The Hard Numbers (Ultra Short Version)
I estimate the need of **~100'000$/month** for building the Qubic Core Tech.

~2'000$ for servers, test environment and what's currently needed to operate
~98'000$ for salaries

This amount of $ will be used to furthr build, extend and maintain the Qubic Core Technology. We will form 3 teams, `core`, `integration` and `testing & operations`.
The FTE (full time employees) of this three teams will be around `13`. Excluding cfb and me.

The Qubic Core Technology should be independent (not controlled) from steco but rather work together with other workgroups or ecosystem builders to enable others to work with qubic. (focus on tech)

## The History
during the first steco period (oct23-apr24) i tried to organize a qubic tech department which is able to deliver the qubic core technology including the needed tools to work with qubic.
this includes the qubic core (https://github.com/qubic/core) but also tools around needed to grow qubic (CLI, wallet, explorer, archive, RPC/API and some libraries). the tech team was also heavily involved in integrations for exchanges or wallets.

to achieve this, i created the following organization structure:

![Qubic dev - old-org](https://github.com/user-attachments/assets/c9950c5d-8a07-4895-9814-827e98585cb7)

this organisation was to bootrap all the needed tech to the users. while all those software was needed to ramp up qubic and to enable the community to interact with qubic easily.
it was a classical organization how one would know it from companies. at first glance it looks good. for me it turned out, that we had a big gap between the different dev departments (core, integration, client). This was mainly because all of them have a slight different focus:

- core: build qubic protocol and the base layer of qubic (very low level coding in c++)
- integration: build a generic solution that the outer world can connect easily to the core
- client: build the tools the users/community can use

as stated in the beginning, the most people in this organization has been working first only in their free time (volunteers), with some i could find an agreement to work more for qubic, others we could recruit directly. The current monthly tech budget is **~111'000$/month** (includes salaries, and operating costs). This budget is currently paid partially from CCF (12bln/month) and donators. In the time being, the demand we see from the community and potential investors has grown and i personally want to deliver the best for qubic. with the current organization this will not work out well.

## The Proposed Change
we have also seen that qubic has matured in the last months. the basic tools are working and we see new ecosystem builders joining. it is now time to also make the next step for the tech organization.

therefore i suggest to change the current structure to the new one:

![Qubic dev - new-org](https://github.com/user-attachments/assets/5d7fa2f7-db35-4cd7-a95a-f046fa5b6cba)

### What are the assignments of Qubic Core Technology
Based on the Qubic Architecture

![Qubic dev org - Architecture](https://github.com/user-attachments/assets/d363dd69-9b2b-40ab-afa7-312078e682aa)

Qubic Core Technology provides:

1. Builds the Qubic Core / Qubic Network (Protocol)
2. Dedicates ~1FTE to build Smart Contracts (Help others, review code)
3. Builds the Qubic Integration Layer (Archive, RPC/API, Event Pup/Sub)
4. Operates the Qubic Integration Layer
5. Operates the Qubic Test Net
6. Takes respnsibility to maintain the Qubic Core/Integration Release/Versioning
7. Maintains the Software created by Qubic Core Technology
8. Writes documentation how the Qubic Core Technology works (in Code and written elsewhere)
9. Supports other ecosystem builders in build on top of Qubic

> [!Note]
Qubic Core Technology **DOES NOT** build projects on top of Qubic (e.g. wallets, explorers or other UI's)

### What changes in the structure?

- Complete **Client** part will be removed from Qubic Core Technology
- The **Testing** part will be extended ans strengthed to **Testing & Operations**
- The **Integration** Team will be strengthed with additional ressources
- The **Core** Team will be strengthed
- All teams togher will do a monthly planning

### Why should we remove **Client**?
The current client team has done the basic work. What now follows is project related work. The Goal is, that each project consists out of different developers (e.g. backend, frontend) so that they can focus on their product while they con consume professional generic services from the integration and core layer.

This is similar to projects which are founded by the ecosystem fund or the grant program. Qubic Core Technology should not be in competition with other ecosystem builders.

### How will the progress be tracked?
The complete project management is online on Github. You can already check the current planing: https://github.com/orgs/qubic/projects/1/views/7 there you can see backlog items, their priority and what currently is in progress. You have full transparency what the Qubic Core Technology is working on. We are also happy to receive external inputs and if wished, i think we will also find a way to do e.g. a weekly update.

### What is the timeline?
I have the promise of the private donators, that the current team is financed until end of year. We do not block anything with the current discussion. I personally would like to send the proposal to the computors in 1-2 weeks. This depends mainly on the computors and community input.

### What will be the proposal to the Computors?
The proposal to the Computors will be to request funds from CCF. If we stick to the budget of ~100k$/month. I would request **300k$** in Qubics to secure the Qubic Core Technology operations for the next three months. This request will be repeadet then every three months.
