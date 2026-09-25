# Code-First-Context

Code-First-Context is a lightweight framework for keeping project context inside the code repository and treating the repo as the core, single source of truth.

Instead of spreading business requirements, ADRs, working notes, and delivery decisions across disconnected note-taking tools, this approach moves them into the medium where delivery teams already work every day: the codebase.

By storing context next to the implementation, teams can use familiar engineering workflows such as pull requests, reviews, version history, and traceable change discussions to keep project knowledge current, reviewable, and actionable.

## Why code-first context?

Traditional project knowledge often lives in places that are easy to forget, hard to maintain, and disconnected from actual delivery work. That usually leads to:

- outdated requirements
- design decisions without history
- important notes hidden in private or disconnected tools
- weak traceability between decisions and implementation

Code-First-Context addresses this by making the repository the default home for project context.

## Core idea

The framework promotes a simple principle:

> If the information is important for building, evolving, or operating the project, it should live in the repository.

That includes content such as:

- business requirements
- architecture decision records (ADRs)
- product and technical notes
- delivery conventions
- operational context
- change rationale

## Benefits

Using the repository as the source of truth gives teams access to built-in DevOps guardrails:

- **Pull request reviews** to challenge, refine, and approve context updates
- **Version history** to understand when and why a requirement or decision changed
- **Diffs** to make updates explicit and reviewable
- **Branching workflows** to evolve ideas safely before merging them
- **Collaboration in one place** where engineers, tech leads, and other contributors already work

## What this framework encourages

Code-First-Context encourages teams to:

1. write context as close as possible to the code it affects
2. keep important decisions in text files tracked by Git
3. review context changes with the same care as implementation changes
4. maintain a transparent history of requirements and decisions
5. reduce dependency on external note silos for delivery-critical information

## Challenges and drawbacks

Code-First-Context introduces challenges:

1. Requirements are provided by Business and Product teams, which usually do NOT use Repos and code.
   Implications:
   -  this makes it difficult (if not impossible) for them to read and maintain the context
   -  they are hesitant to use this approach, making the Delivery team responsible for maintenance based on other sources
   Solutions:
   - introduce Business and Product to tools allowing them to read, review and comment the context
   - implement automations that provide a way to update the context repo (e.g. AI tools with integration to GH)
  
2. Delivery team becomes the owner of the context
   Implications:
   -  Delivery team has additional admin work to update and review the context
   Solutions:
   - accept the admin work - it would be done anyway through notes, meetings scattered across other tools - we believe this extra mile is already covered elsewhere but covering it in this approach would actually make it more efficient
   - automate updates with AI
  
3. Two sources of truth
   - for this to work, the repo should be the single source of truth for the context
   - if maintenance of the repo by both Tech and non-Tech teams is not possible, you either drop this approach, or use two sources

## Intended outcome

The outcome is a project repository that contains not only source code, but also the context needed to understand why the code exists, how it should evolve, and what constraints guide delivery.

In short, this framework treats the codebase as both:

- the home of implementation
- the home of project knowledge

## Summary

Code-First-Context is a framework for moving project context into the repository so delivery teams can manage requirements, ADRs, and notes with the same workflows they already use for software delivery.
