# 🧭 Relationship Compass · 关系罗盘

[简体中文](README.md) · **English**

**Understand where you stand. Decide what to do next.**

“How should I reply?” matters. The right words can express interest, clear up a misunderstanding, or help a relationship move forward.

But its direction depends more on where you both stand: how willing each person is, whether effort is reciprocated, and what you actually do next. A well-written reply cannot make up for persistent one-sided effort.

Relationship Compass draws on conversations, interaction history, and real-world circumstances to help you assess the relationship, choose an action, and then find the words. Separate records for each person give future discussions something concrete to build on.

**Understand the relationship → Choose an action → Draft a reply → Record and review**

[Example](#an-example) · [How it reasons](#how-does-it-analyze-a-relationship) · [Separate records](#each-relationship-has-its-own-context) · [Getting started](#getting-started) · [Privacy](#data-and-privacy)

## When to use it

| What you are wondering | How it can help |
|---|---|
| We chat well, but plans to meet never happen | Compare the conversation with actual actions, consider possible explanations, and plan a next step |
| I want to reply, but I don't want to sound too harsh | Preserve your intent and voice while making the message easier to say |
| I'm always the one reaching out. Am I investing too much? | Review initiative, responses, and recurring patterns |
| We make up after every argument, but nothing changes | Look for explanation, repair, and concrete changes after conflict |
| I'm getting to know several people and mixing up the details | Keep a separate profile and interaction history for each person |
| Has this relationship actually changed? | Compare new developments with saved records and identify what supports the assessment |

## How does it analyze a relationship?

**It starts with the material you provide: what was said, what happened, and what you want from the relationship.**

When you ask to review a particular person, Compass also uses that person's saved background, timeline, and interaction records. Missing information stays unknown.

It looks at these dimensions:

| Dimension | What it examines |
|---|---|
| **Initiative and response** | Who starts conversations, keeps them going, or suggests meeting? Do responses lead to action? |
| **Reciprocity and investment** | Do time, care, and effort go both ways? Has one person been carrying the relationship? |
| **Security and trust** | Can both people express how they feel? Are responses dependable? Is there a willingness to repair misunderstandings? |
| **Boundaries and willingness** | Are needs and refusals respected? Are expectations clear? |
| **Real-world circumstances** | How might work, distance, existing relationships, or shared social circles affect the interaction? |
| **Recurring patterns** | Do similar problems keep happening? What tends to precede a change in the interaction? |
| **Change over time** | How have effort, boundaries, and ways of relating changed compared with earlier records? |

### Which frameworks does it draw on?

The reference material translates several theoretical perspectives into questions to ask about a relationship. Some older notes contain generalizations, numbers, and practical heuristics that have not been individually verified. They should not be treated as established findings. The core instructions prioritize facts, reciprocity, and boundaries.

| Perspective | How it informs the questions |
|---|---|
| Attachment and the secure base | Look at responsiveness, trust, and patterns of approaching and withdrawing |
| Reciprocity and social exchange | Examine effort, expectations, and imbalances |
| Behavioral reinforcement | Notice whether particular responses sustain a recurring interaction pattern |
| Attribution and cognitive consistency | Compare explanations for behavior with the available facts |
| Field theory | Consider individual choices in the context of work, distance, identity, and circumstances |
| Unfinished-task effects and gain/loss reference points | Consider how unresolved situations or fear of loss may affect judgment |

**These frameworks help generate questions and compare explanations. Advice must still be grounded in the details of the situation.** Naming a theory does not establish that this skill is scientifically validated, and a few messages cannot diagnose a person.

Analysis and records distinguish three kinds of information:

- **Reported facts:** for example, “They canceled the meeting.” A user's account is labeled as reported, not independently verified.
- **Possible explanations:** for example, “They may not want to move things forward right now.” This remains an inference.
- **Unknowns:** for example, why they canceled or whether they want to reschedule.

Any scores in the compass are heuristic estimates, not statements such as “There is an 80% chance they like you.” Insufficient evidence should be marked as unknown.

## From assessment to action

“Where you stand” means how each person sees the relationship, how much each is willing to invest, and whether expectations align. Compass uses your goals and the other person's responses to help you choose a concrete next step:

- **Move forward:** when interest is mutual, make a specific, low-pressure invitation and follow through on the arrangements.
- **Clarify:** when expectations differ or you keep guessing, state your needs and ask what you need to understand.
- **Observe:** when information is missing, identify what further actions would help you assess the situation rather than repeatedly interpreting one message.
- **Repair or step back:** after conflict, discuss concrete changes; when there is a clear refusal or persistent imbalance, respect boundaries and reconsider your investment.

The reply should support the action. “I'll change” needs to be followed by real adjustments. “Let's meet again” needs arrangements both people want to follow through on.

## An example

> This is a fictional illustration of the approach, not a recorded evaluation. Actual responses depend on the information you provide and the model you use.

**You:**

“We met a month ago. I usually start our conversations, and their replies are warm. But I've suggested meeting twice, and both times they said they were busy without offering another time. Should I ask again?”

**Relationship Compass:**

“Separate chatting from making plans. They are willing to reply, but so far there hasn't been a shared effort to arrange a meeting.

Two invitations without an alternative date are worth noticing. They could genuinely be busy, unsure, or not interested in meeting. There isn't enough information to know which.

If you've already made your invitation clear, you could leave the next arrangement with them:

**‘Sure—let me know when you're free and feel like meeting up.’**

Then see whether they suggest a specific time. You can also consider how much time and energy you want to invest while things remain uncertain.”

## Each relationship has its own context

If you are getting to know A, B, and C, you can keep separate records for each. Every person has their own background, timeline, relationship compass, and detailed interaction entries.

```text
You: Create a profile for A. We met at a friend's gathering last month.
You: Save a record of today's meeting with B…
You: Review my interactions with C over the past month. Which changes are supported by the records?
```

**When discussing A, Compass reads only A's relevant records. Updating B does not update A or C.** If the person is unclear, it asks. It reads several people's records together only when you explicitly request a comparison of those people.

Records are actual files that you can inspect, correct, or delete:

```text
compass-data/
├── index.json                 # Names mapped to unique person IDs
└── people/
    ├── p-<person-A-id>/
    │   ├── profile.md         # Background and expectations
    │   ├── config.md          # Preferences
    │   ├── timeline.md        # Interaction timeline
    │   ├── compass.md         # Current assessment and its basis
    │   └── sessions/          # Facts, inferences, advice, and follow-up
    ├── p-<person-B-id>/
    └── p-<person-C-id>/
```

Files are written only when you explicitly ask to create a profile, record, save, or update the compass. Ordinary advice does not automatically create a dossier. After saving, the assistant reads the files back and reports their location. Later feedback is linked to the original event.

To continue in another conversation, the assistant must have access to the same data directory, and you must identify the person you want to discuss. Separation is implemented through directories and agent reading rules; it is not encryption or operating-system access isolation.

## Getting started

Relationship Compass runs inside an AI assistant that can read the skill and its reference files. Persistent profiles also require local file read/write capabilities.

Give the following request to an assistant that supports local skills:

```text
Download Relationship Compass from https://github.com/Minggnim-jpg/relationship-compass
and install it as compass using this tool's skill installation rules.
Preserve the structure of SKILL.md, agents/, and references/.
If a skill with that name already exists, show the differences first;
do not overwrite existing configuration or personal data.
```

You can also download the repository and place the complete skill files in your host's `compass` skill directory. Consult that host's documentation for the location and loading procedure. This repository contains skill instructions and reference material; it is not a standalone chat application.

Once `compass` is installed and loaded, start with a concrete question:

```text
Use Relationship Compass to help me understand this interaction.
The background is… My goal is… Here is the conversation…
```

```text
Use Relationship Compass to help me reply.
I want to say… Keep it natural, and don't make promises I can't keep.
```

```text
Create a separate profile for A in the data directory I specify.
Start by recording this background…
```

You do not need to fill out a complete profile before asking for advice. Start with the immediate issue and add context when it matters.

This English README covers the project and onboarding. The core skill and most reference material are currently in Chinese; you can ask the model to respond in English.

The analysis frameworks, communication references, and recordkeeping instructions are all included in the skill. No external knowledge base or additional service setup is required. You still need a capable AI assistant; persistent records require file read/write permissions.

## Data and privacy

- Use aliases and share only the conversation and context needed for the question.
- Records are saved in your chosen location, defaulting to `compass-data/` in the current working directory, separate from the skill's source files.
- Local storage does not mean offline processing. Content read by the assistant may be sent to its model provider, depending on your platform and service.
- Keep personal profiles and raw conversations out of public repositories and issues.
- This project does not automatically monitor messaging apps or send messages on your behalf.

## What has been checked

A file workflow was exercised with three fictional people: creating profiles, saving entries, and reading them back. Updating B left A's and C's files unchanged. This checks that specific workflow, not every model, host, or long-term usage scenario.

Compass provides relationship analysis and wording suggestions. It cannot guarantee another person's thoughts or the outcome of a relationship. Respect a clear refusal; analysis cannot replace communication between the people involved.

## Help improve it

Contributions can include difficult scenarios, corrections to unsupported claims or references, and feedback on wording that works in practice. Use fictional or thoroughly anonymized material when submitting examples.

If Compass helped you think through a difficult moment, leave a Star so you can find it again.

## License

This project is released under the [MIT License](LICENSE). Use, modification, distribution, and commercial use are permitted. Copies or substantial portions must retain the copyright and license notices.

Third-party material with its own copyright or license notices remains subject to those terms.
