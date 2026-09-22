# ARC-AGI-3 Documentation
This directory contains an in-progress rewrite of documentation for ARC-AGI-3 AI reasoning benchmark. Official docs currently available at [docs.arcprize.org](https://docs.arcprize.org).

# Local Development
To preview it locally, ensure you have [mintlify](https://www.mintlify.com/docs/quickstart) installed, then run Mintlify from this directory:
```bash
cd new
mint dev
```
That will open up your browser with the preview of the new docs, that you can compare with the official ones.

# Structure Ideas - Sketchpad

- Groups of pages are neatly organized in folders for easier management with lots of doc pages.
- get-started/benchmark-overview.mdx is the docs benchmark, roughly matching the old entrypoint. Explanation of what ARC-AGI-3, the main ideas, what makes it stand out, then link to Technical Report, which is well-written, so it's good to expose it. It contains a lot of information already. Old docs linked to nonexistant page here.
- Next page from the entrypoint is how-to-participate.mdx, which should be the second thing that a newcomer sees. We got them interested by the overview, now call to action: participate, and here is how you do it. Clear steps, read kaggle competition, read our theory explanation, read about the tools available, use them and participate.
- Theory section is conceptual, it is isolated from tool-specific docs. I'm not saying frame is a FrameData object or a 3D python list or a list of numpy arrays. It depends on the tools, but the concept stays, that frames are grids of integers. This is deliberately written to be hugely independent of tool usage and tool remakes and rewrites. If we change the tools, we will mostly change tool-specific docs, not this concept explanation.
- intro-to-games.mdx aims to be an overview of what is the structure of the benchmark. 135 games, some public, most private, round-based, and how to approach solving those games.
- observations.mdx is what data you will have available, so you can start thinking of how to approach this.
- action-space.mdx so you understand the range of actions that will be possible.
- scoring.mdx of course super important to know what to prioritize. Also https://www.kaggle.com/competitions/arc-prize-2026-arc-agi-3 redirects to https://docs.arcprize.org/methodology, so will need a replace the link.
- Previous methodology description super confusing. It's not an upper median (75th percentile by action count), it's also not a median human performance, it's median among people who finished the level, picking the higher count if there were even amount of people who finished. I wrote it concisely and hopefully very clear in scoring.mdx.
- Scoring methodology compared to current official docs is much more concise, I didn't feel like it's necessary to explain what counts as an action. It seems obvious to me what counts as an action (submitting an action to the environment), but maybe we want to be explicit? I started with being concise, I'll wait for feedback.