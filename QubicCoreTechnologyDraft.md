# Qubic Core Technology (QCT)

it seems that we currently have the proposal season, i hope we can discuss together another proposal.
in the past 2.5 years, Qubic development was mainly made by volunteers, enthusiasts and of course cfb.

> [!Note]
> This is a draft to be discussed. i tried to bring together all information needed to have a fact based discussion.
> The draft was shared with a few people before bringing it to the community.

> [!Warning]
> This draft is heavy cost. Grab a coffee and take your time :)

This "pre-proposal" contains information about:
- changes in and a desired setup of the Qubic Core Technology team
- the setting of this team within Qubic
- the financing of this team

The Qubic Core Technology team will
- re-focus to strengthen the technological foundation of Qubic
- detached from the Steering Committee
- and be financed via CCF requests

### Re-focus to strengthen the technological foundation of Qubic
- we have done a lot of work
- even more will come
- client apps are mature enough and needs to outgrow
- we will actively support this transition phase

### Detached from the Steering Committee
- stay neutral
- open source and open mind
- active support for different initatives from the community
- form the first independent workgroup of many that can follow

### Financed via CCF requests
I estimate the need of **~100'000$/month**:  
- ~2'000$ for servers, test environment and what's currently needed to operate
- ~98'000$ for salaries (around `13` FTE, excl. cfb and me)
- to extend and maintain the Qubic Core Technology
- split among three teams (`core`, `integration` and `testing & operations`)

## The Details

**Content**
1. [The History](#the-history)
2. [New Organizational Chart](#new-organizational-chart)
3. [What are the assignments of Qubic Core Technology](#what-are-the-assignments-of-qubic-core-technology)
4. [What changes in the structure?](#what-changes-in-the-structure)
5. [Why should **Client** be organized as products?](#why-should-client-be-organized-as-products)
6. [How will the progress be tracked?](#how-will-the-progress-be-tracked)
7. [What is the timeline?](#what-is-the-timeline)
8. [What will be the proposal to the Computors?](#what-will-be-the-proposal-to-the-computors)
9. [Appendix: Open Source Software](#appendix-open-source-software)
10. [FAQ](#faq)

### The History
during the first steco period (oct23-apr24) i tried to organize a Qubic tech department which is able to deliver the Qubic core technology including the needed tools to work with Qubic.
this includes the Qubic core (https://github.com/Qubic/core) but also tools around needed to grow Qubic (CLI, wallet, explorer, archive, RPC/API and some libraries). the tech team was also heavily involved in integrations for exchanges or wallets.

to achieve this, i created the following organization structure:

![Qubic dev - old-org](https://github.com/user-attachments/assets/c9950c5d-8a07-4895-9814-827e98585cb7)

this organisation was to bootrap all the needed tech to the users. while all those software was needed to ramp up Qubic and to enable the community to interact with Qubic easily.
it was a classical organization how one would know it from companies. at first glance it looks good. for me it turned out, that due to different focus in the teams (core, integration, client) the potential output could be more productive.

- core: build Qubic protocol and the base layer of Qubic (very low level coding in c++; focus on security, performance and optimized code)
  - Build the network features like `Ticking`, `Internal processing of Transfers`, `Solution processing`
- integration: build a generic solution that the outer world can connect easily to the core (higher level coding, most in go; focus on stability, portability and functionality)
  - Build features/products like: `Archiving of Chain History`, `Public RPC/API`, `Relaying Qubic Event Information`
- client: build the tools the users/community can use (high level coding with focus on UI/UX)
  - Build products like: `Wallet`, `Explorer`, `Management UI's`

as stated in the beginning, the most people in this organization has been working first only in their free time (volunteers), with some i could find an agreement to work more for Qubic, others we could recruit directly. The current monthly tech budget is **~111'000$/month** (includes salaries, and operating costs). This budget is currently paid partially from CCF (12bln/month) and donators. In the time being, the demand we see from the community and potential investors has grown and i personally want to deliver the best for Qubic. i think with the current organization this will be hard.

### New Organizational Chart
we have also seen that Qubic has matured in the last months. the basic software is working and we see new ecosystem builders joining. it is now time to also make the next step for the tech organization.

therefore i suggest to change the current structure to the new one:

![Qubic dev - new-org](https://github.com/user-attachments/assets/5d7fa2f7-db35-4cd7-a95a-f046fa5b6cba)

### What are the assignments of Qubic Core Technology
Based on the Qubic Architecture

![Qubic dev org - Architecture](https://github.com/user-attachments/assets/d363dd69-9b2b-40ab-afa7-312078e682aa)

Qubic Core Technology provides:

1. Builds the Qubic Core / Qubic Network (Protocol)
2. Dedicates ~1FTE to build Smart Contracts (Help others, review code)
3. Builds the Qubic Integration Layer (Archive, RPC/API, Event Pup/Sub)
4. Operates the Qubic Integration Layer (RPC/API)
5. Operates the Qubic Test Net
6. Takes responsibility to maintain the Qubic Core/Integration Release/Versioning
7. Maintains the Software created by Qubic Core Technology
8. Writes documentation how the Qubic Core Technology works (in Code and written elsewhere)
9. Supports other ecosystem builders in build on top of Qubic

> [!Note]
> The above points are technology driven. The community or the business will profit from those services because they can rely on it.
> Example A: A new Ecosystem Team wants to create a DAPP: QCT, will give support on how to build the SC, it will help with testing, doing reviews and integrate it into Qubic as soon the Computors have approved the SC.
> 
> Example B: An ecosystem team would like to have a new feature in the core (e.g. reliable events for asset transfers): QCT will evaluate the feature and if applicable, take this into it's planing and code it
> 
> Example C: A Wallet developer whishes to receive more detailed information about transactions: QCT will add the needed information to the generic RPC/API interface

> [!Important]
> Qubic Core Technology **DOES NOT** build projects on top of Qubic (e.g. wallets, explorers or other UI's)
> Client products do have a specific need on how data is processed. Every ecosystem team has it's own needs. To not mess up with the different needs, it is best practice to give ecosystem builders a generic interface to work with. From this point on a product team can start building. This is the main reason why client products should be organized as project/product structures.

### What changes in the structure?
- **Client** part will be organized as individual products/projects
- The **Testing** part will be extended and strengthed to **Testing & Operations**
- The **Integration** Team (which builds an interface between Qubic Core and ecosystem builders) will be strengthed with additional ressources
- The **Core** Team will be strengthed to support the newly joining ecosystem builders (from grant program or outsourced development)
- All teams together will do a monthly priority planning to align their focus and consider new inputs

### Why should **Client** be organized as products?
With a dedicated budget and own reporting, we can create better products which can reflect the needs from the community and clients. A team focused on one product (maybe two) is normally more efficient and can release features independent of other products. The decoupling helps to grow individually and bring added value to Qubic.

For products like wallet or the explorer, the basic work has been done. What now follows is project related work. The Goal is, that each project consists out of different developers (e.g. backend, frontend) and also can have direct resources from marketing or design so that they can focus on their product.

This is similar to projects which are founded by the ecosystem fund or the grant program. Qubic Core Technology should not be in competition with other ecosystem builders. I want to see more successfull projects/products on Qubic, we can accelerate this when QCT itself focus on building the base and extended support for builders.

### How will the progress be tracked?
The complete project management is online on Github. You can already check the current planing: https://github.com/orgs/Qubic/projects/1/views/7 there you can see backlog items, their priority and what currently is in progress. You have full transparency what the Qubic Core Technology is working on. We are also happy to receive external inputs and if wished, i think we will also find a way to do e.g. a bi-weekly tech update.

Together with the marketing and/or operations workgroup the status hopefully can also be presented in a nice way.

### What is the timeline?
I have the promise of the private donators, that the current team is financed until end of year. We do not block anything with the current discussion. I personally would like to send the proposal to the computors in 1-2 weeks. This depends mainly on the computors and community input.

### What will be the proposal to the Computors?
The proposal to the Computors will be to request funds from CCF. If we stick to the budget of ~100k$/month. I would request **300k$** in Qubics to secure the Qubic Core Technology operations for the next three months. This request will be repeated then every three months. This Budget is used to pay for infrastructure (e.g. servers) and people. The calculated amount of Qubics is done by the current price. If the price rises, the period using the same budget can be extended, if the price falls, it may mean, that we need to re-request from CCF.

### Appendix: Open Source Software
Below you find an unsroted list of open source code from products/software provided by the the current Qubic Technology Team (including cfb and former contributors):

- https://github.com/qubic/wallet-app
- https://github.com/qubic/core
- https://github.com/qubic/wallet-app-dapp
- https://github.com/qubic/qx-service
- https://github.com/qubic/qx-ui
- https://github.com/qubic/go-events
- https://github.com/qubic/go-qubic
- https://github.com/qubic/org.qubic.proposal
- https://github.com/qubic/proposals-frontend
- https://github.com/qubic/wallet
- https://github.com/qubic/explorer-frontend
- https://github.com/qubic/ts-library
- https://github.com/qubic/proposal
- https://github.com/qubic/Qiner
- https://github.com/qubic/qubic-mm-snap
- https://github.com/qubic/ts-library-wrapper
- https://github.com/qubic/qubic-csharp
- https://github.com/qubic/qlogging
- https://github.com/qubic/qubic-cli
- https://github.com/qubic/go-archiver
- https://github.com/qubic/qubic-http
- https://github.com/qubic/go-node-connector
- https://github.com/qubic/go-schnorrq
- https://github.com/qubic/go-node-fetcher
- https://github.com/qubic/ts-vault-library
- https://github.com/qubic/react-ui
- https://github.com/qubic/go-qubic-nodes

## FAQ
https://discord.com/channels/768887649540243497/1301317725444116490/1303038768034611251
> **Q:** Not correct Logo and gramar errors
> 
> **A:** With time the look and feel may be optimized. For my personal view the content seems to be more important atm.
***
https://discord.com/channels/768887649540243497/1301317725444116490/1303039585747730503
> **Q:** 98k cost could be explained more in detail and also who are the 13 FTE, whats their positions, tasks and work time (hours)
> 
> **A:** Currently we have in core technology 11 active members (incl. cfb and me). they all work differente percentage. the goal is to extend the team to be able to deliver what is needed for further grow. i'm not sure if it is a must to say who earns how much for what work. i can tell you that cfb and me do not get anything. members are: @phil, @luk, @dkat, @linckode, @raika sternensucher, @fnordspace, @cyber-pc, @kavatak
if the proposal is approved, we will search for testing & operators and dev's who can join the integration team. current organization is that @luk, @dkat, @phil (lead dev), @cfb (lead protocol), @joetom form the planning and priorization team. everybody of the team has it's own role and responsibility. at least i think that there is no hierarchie, we can exchange each other on a technical level and find a rational solution when we do not agree on the first glance.
***
https://discord.com/channels/768887649540243497/1301317725444116490/1303039839029039125
> **Q:** I, personally would like to see more milestones, OKRs, deadlines, timelines, concrete comittments to what will be worked on by whom and when
> 
> **A:** let's work on that together, as the complete planning and priorization is publicly online, and we have a scheduled 1 month planing period, we are happy to receive inputs on what is more important, to that this can be considered on the next planing meeting. you cut put the milestones then on a nice roadmap. (i would not go into that much micro management)
If you visit https://github.com/orgs/qubic/projects/1/views/7 and scroll a bit down, you can alread see who is working on what atm.
***
https://discord.com/channels/768887649540243497/1301317725444116490/1303049381141807166
> **Q:** Tech % should also include grant program and incubator program.
>
> **A:** This is a very interesting view. i think it make sense to separate grant, outsourced development and core development. this let's each of them focus on their main topic.
***
https://discord.com/channels/768887649540243497/1301317725444116490/1303059283843223612
> **Q:** What mechanisms will be placed to ensure the additional resources for integration and core teams are used effectively
> 
> **A:** We have currently not enough resources to fulfil the demands on the integration layer (rpc/api, archive, event pub/sub); i think @luk can say a bit more to this. but as we identified this two teams as crucial for the further qubic growth this needs to be able to perform. i hope the effecitveness can be measured by the output and how easy the new ecosystem builders can interact/onboard with qubic.
> ***
> **Q:** How will be managed the communication between Qubic Core Tech and community projects to avoid duplication of efforts (this is very important for me)
> 
> **A:** We have already established a semi-open discord tech server where any interested developer can join. within this tech server we have channels like `integration-ama` or `core-ama` where every technical person can ask questions directly to the dev's.
due to the clear [assigment](#what-are-the-assignments-of-qubic-core-technology) what qubic core tech should build on it should not come to duplication imho. what we maybe need to learn: better communicate what our dev's are doing
> ***
> **Q:** What level of detail in transparency is expected to be presented to computors to justify continued funding? (i mention because i like steco biweekly reports)
> 
> **A:** i assume you see the same. a bi-weekly interval seems good to do the coms. Depending on how e.g. the diecord organisation looks like in the next month i could imagine, that we have e.g. an "Operations Workgroup" which will collect the information also from other workgroups or ecosystem builders and package this together for a common bi-weekly update. (just an idea...)
> ***
> **Q:** What steps will be taken to ensure products built by third parties align with the quality standard of Qubic Core Tech (this is very important for me too, in fact i think if this is properly implemented would be huge for qubic)
> 
> **A:** When it comes to SC's then every SC goes through a testing and review phase lead by the core dev's. this ensures basic quality check. with the new [contract verification tool](https://github.com/orgs/qubic/projects/1/views/7?pane=issue&itemId=85057661) which is on high prio to be developed we will have another instrument to ensure core code quality. When it comes to quality of the ecosystem products, we cannot have direct influence. but, @dkat is in the grants committee to exactly ensure also quality their. this means for projects/products financed by grants or ecosystem fund, i see a good way when core and/or integration dev's can be part of those committees.
***
https://discord.com/channels/768887649540243497/1301317725444116490/1303431599819329646
> **Q:** Considering Core Tech is the absolute backbone of the Qubic, what is the reason QTC shouldn't be under Quorum oversight at all times? Putting this outside of Quorum could lead to a single point of failure. Andre Cronje caused Phantom to almost fall over as he was the lead developer leaving. Now that you left SteCo, Quorum does not have the opportunity to hold you or the team accountable besides stopping funding. How do you see this work?
> 
> **A:** I cannot follow your argumentation. If the Computors are not happy with what is delivered and will not extend the budget i assume that they will express this. Either in chat or by not accepting code changes.
***
https://discord.com/channels/768887649540243497/1301317725444116490/1303431635345084467
> **Q:** How do you intent to hold your team members accountable and how do you intent to grow/develop them at Qubic over a longer period of time?
> 
> **A:** I'm not the type of leader to hold "my team members accountable". I prefer to lead by example (and lead by strengths) and let all participate in decicions. e.g. cfb mostly decides on protocol topics, phil as lead def mostly decides about architecture, dkat as core head decides what is gonna developed next, @luk as head of integration decides how to build the archive server and so on. this way, every individual can work where he/she has the strengths.
***
https://discord.com/channels/768887649540243497/1301317725444116490/1303431717952159824
> **Q:** How does Core tech ensure communication with other workgroups and in specifically with marketing and ecosystem?  The risk of isolation increases in a decentralized team because it assumes good and proactive behaviour from all team members.
>
> A: We had a similar Question: https://discord.com/channels/768887649540243497/1301317725444116490/1303059283843223612, the answer there was: We have already established a semi-open discord tech server where any interested developer can join. within this tech server we have channels like `integration-ama` or `core-ama` where every technical person can ask questions directly to the dev's. This tech server also already have the `marketing-tech` channel where marketing can ask tech questions directly to the techies. Additionally i see us in an open discord, everybody can see who is involed in what, asking people is the core of getting information. You can access the milestone/task/roadmap board to see who works on what, how are the priorities and you will get/create a be weekly update. 
***
https://discord.com/channels/768887649540243497/1301317725444116490/1303431740873904139
> **Q:** How will this proposal increase the reaction time of the core team?
> 
> **A:** Needs further clarification.
***
https://discord.com/channels/768887649540243497/1301317725444116490/1303431782229872710
> **Q:** How do you intend to deliver tech with speed on execution? Decentralization has a risk to slow things down. How do you make sure we execute fast enough to stay technically competitive.
> 
> **A:** In my opinion decentralization has nothing to do with speed. With this proposal i think it is the contrary, i try to set focus. QCT can focus on core development. The Project/Product teams can focus on their products.
***
https://discord.com/channels/768887649540243497/1301317725444116490/1303431816669167677
> **Q:** The proposal talks about product. How do you intent to build the best infrastructure as a product? How do you intend to stay close to what users want and what investors want? Do you intent to do a/b testing and user research?
> 
> **A:** In an open source project potentially everyone can participate. I see the QCT as the creators of the foundation. What you ask for is more on a higher layer. The Wallet, Explorer, Liquidity Pools, QX Builders needs to focus on Users. Qubic's core focus imho is on security, stability, performance. Those three topics normally are in conflict with users needs. What i would love to see, is that the interface of Qubic is well documented. And as described it is important that e.g. ecosystem builders can have direct access to core dev's, they can ask questions and we have a dedicated testing team when it e.g. comes to help for SC testing. Doing A/B testing in a blockchain is almost impossible, we can only have one truth. What is also promoted by cfb is that we are open for testing new things.
***
https://discord.com/channels/768887649540243497/1301317725444116490/1303431840245481473
> **Q:** Will QTC create their own legal entity or be part of the association? Where will employees be employed so that we can offer them a growth trajectory
> 
> **A:** A growth trajectory is given by design. A junior that starts will gain experience and can grow to a senior. A senior can grow to an architect. Normally there is also a natural fluctuation which helps. Current employees are employeed with different companies, are contractors, do not receive any salary or receive qubic.
***
https://discord.com/channels/768887649540243497/1301317725444116490/1303432917954986105
> **Q:** There's power in presenting and aligning an unified roadmap towards the community. How do you intend to work together with SteCo and other groups to deliver a cohesive strategy for core Qubic? The community might not care about different work groups and might just want to see an unified roadmap that is primed to be achieved. There's a risk with decentralized models that strategies are misaligned and lack of communication can hinder progression.
>
> **A:** My wish setup would be if we have a dedicated workgroup which is in charge of creating the roadmap. This workgroup goes to ask QCT, Marketing, Qearn and any other known ecosystem builder for their planed activities. In a dream world there is a tool provided by this workgroup where all Qubic contributors can put their initiatives and milestones in. The tool will then magically create the roadmap in a nice way.






