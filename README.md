# The IPFS GUI group

[![Made by icon.](https://img.shields.io/badge/made%20by-Protocol%20Labs-blue.svg?style=flat)](https://protocol.ai/)
[![Project icon.](https://img.shields.io/badge/project-IPFS-blue.svg?style=flat)](http://ipfs.io/)
<a href="https://www.irccloud.com/invite?channel=%23ipfs-gui&amp;hostname=irc.freenode.net&amp;port=6697&amp;ssl=1" target="_blank"><img src="https://img.shields.io/badge/irc-%23ipfs--gui-brightgreen.svg?style=flat"  height="20"></a>

Our goal is to **create visual and interaction standards and patterns for working with IPFS that are ...**

- **Simple**: Present the big ideas of IPFS clearly, without unnecessary complexity
- **Accessible**: Enable *everyone* to take advantage of what IPFS offers
- **Reusable**: Offer compelling standards and atomic patterns to the community of IPFS builders
- **Beautiful**: By their nature, things that are simple, accessible and reusable are also beautiful

## IPFS GUI projects

### Primary projects

Our primary focus is on the suite of Protocol Labs-led "helper" apps that provide a GUI for IPFS as a whole. Our aim is to make them useful for seasoned IPFS developers while also offering a welcoming introduction to IPFS for those less experienced.

| IPFS Companion | IPFS WebUI | IPFS Desktop |
|:-:|:-:|:-:|
| [<img title="IPFS Companion" src="https://ipfs.io/images/ipfs-companion-hex.png" />][IPFS Companion] | [<img title="Web UI screenshot" src="img/webui-hex.png" />][IPFS Web UI] | [<img title="IPFS Desktop" src="https://ipfs.io/images/ipfs-desktop-hex.png" />][IPFS Desktop] |
| [Browser extension](https://github.com/ipfs/ipfs-companion) for opening ipfs:// URLs, saving/sharing files, and more| [IPFS file manager and network explorer](https://github.com/ipfs-shipyard/ipfs-webui) in your browser | Launch and manage IPFS from a friendly, intuitive [desktop app](https://www.github.com/ipfs-shipyard/ipfs-desktop) |

### All projects

In addition to the apps above, the IPFS GUI group supports work on issues in all of the following repos. You can get a birds-eye view on prioritization and progress of GUI-centric work in these repos in [our ZenHub board](https://app.zenhub.com/workspaces/-ipfs-app-family-ux-5e7a3123e969e659cdebb5e6/board?repos=111841602,32695583,36580101,24483721,142161410,119716282,116711586,38799513,142181521,147528357,148369983,40225364,104770273). *Note that our focus is primarily on UX-related work, so not all issues within all these repos may be in our group's purview.*

- **[ipfs/ipfs-gui](https://www.github.com/ipfs/ipfs-gui)**: This repo, used for overall planning and cross-repo work
- **[ipfs/dir-index-html](https://www.github.com/ipfs/dir-index-html)**: Directory listing HTML for go-ipfs gateways
- **[ipfs/distributions](https://www.github.com/ipfs/distributions)**: Source code for https://dist.ipfs.io
- **[ipfs/i18n](https://www.github.com/ipfs/i18n)**: Internationalization work across all IPFS projects
- **[ipfs/public-gateway-checker](https://www.github.com/ipfs/public-gateway-checker)**: Source code for https://ipfs.github.io/public-gateway-checker/
- **[ipfs-shipyard/ipfs-companion](https://www.github.com/ipfs-shipyard/ipfs-companion)**: Browser extension that simplifies access to IPFS resources on the Web
- **[ipfs-shipyard/ipfs-css](https://www.github.com/ipfs-shipyard/ipfs-css)**: Single-purpose CSS rules and font-face config to add the IPFS look and feel to your UI
- **[ipfs-shipyard/ipfs-desktop](https://www.github.com/ipfs-shipyard/ipfs-desktop)**: An unobtrusive and user-friendly desktop application for IPFS on Windows, Mac and Linux
- **[ipfs-shipyard/ipfs-share-files](https://www.github.com/ipfs-shipyard/ipfs-share-files)**: Source code for https://share.ipfs.io
- **[ipfs-shipyard/ipfs-ui-style-guide](https://www.github.com/ipfs-shipyard/ipfs-ui-style-guide)**: UI style guide for IPFS apps
- **[ipfs-shipyard/ipfs-webui](https://www.github.com/ipfs-shipyard/ipfs-webui)**: Browser front-end for IPFS nodes
- **[ipfs-shipyard/ipld-explorer](https://www.github.com/ipfs-shipyard/ipld-explorer)**: Source code for https://explore.ipld.io
- **[ipfs-shipyard/ipld-explorer-components](https://www.github.com/ipfs-shipyard/ipld-explorer-components)**: React components for https://explore.ipld.io

## Status

Creating a cohesive family of helper tools benefits not only our current core market (existing IPFS developers), but also impacts nearly every other key stakeholder group — from potential devs to those in adjacent industries to the “civilian” dweb-curious. This has a direct impact on our goal to increase the number of nodes in the network.
Establishing our app family as a unified “product suite” of helper tools via a consistent, feedback-driven user experience makes it easier for people to understand, use, and build on the IPFS protocol — while also making the distinction between the protocol and the tooling abundantly clear (this confusion is something that’s stood out in our Q1 2020 collabs interviews).
Establishing standards for high-quality mental models and visual metaphors for IPFS gives guidance and inspiration to our partners and collabs who are creating end-user interfaces themselves — without stealing their thunder or trying to do their job. 
Organizationally speaking, establishing a design-thinking-driven, product-design-informed approach to our IPFS app family gives us a low-cost way to test drive these design and product/project management methodologies for potential use elsewhere in PL.

This is a long-term approach — and one that will require developer cycles if it is to succeed — but in the near term, substantial inroads can be made. The following Q2 OKRs (to be undertaken by Jessica) will enable us to kick off app family efforts, with the understanding that as Q2 progresses with a project management framework in place, we can multiply effectiveness substantially by bringing on development help from Moxy as discussed.
Q2 app family OKRs
(P0) Objective: Establish a trackable, transparent home for app family work
Key results:
Repurpose the existing ipfs-gui repo as central home for family-wide UX/UI/product-strategy work; this includes consolidating any other repos that should collapse into this one
Build an issue management framework in ZenHub consistent with our other project/product management practices (including standard issue labeling); include all relevant repos
(P0) Objective: Evaluate the current state of the app family landscape by collecting, evaluating, and prioritizing existing issues
Key results: 
Issue queues for all three apps and other related repos examined, ranked, consolidated/reframed as necessary, and clearly visible in ZenHub
Issue queues used to determine short-term/long-term staffing needs in both design/UX and development
Issue queues ready for use in evaluating the existing landscape for overall UX/UI discrepancies and pain points
(P1) Objective: Fix (x) number of outstanding UX/UI-related issues in app family, where (x) is a number defined by Jessica’s skill set and overall workload
Key result: Closed issues
(P1) Objective: Create first-draft mental model of the IPFS app family, cross-referenced against core goals and identified stakeholders
If time allows, increase granularity of the model by adding basic user journeys cross-referenced against core goals and stakeholders
If time allows, expand to make room for potential future journeys for “civilian” file sharing or other non-core-dev means of increasing the number of nodes online




## Resources

#### Assets
  - IPFS Logo - [repo](https://github.com/ipfs/logo) - _vector and raster logo assets_
  - IPFS brand book - [_pdf_](https://github.com/ipfs-shipyard/ipfs-ui-style-guide/files/1629262/IPFS_brandbook.pdf) - _how to use the IPFS logo_
  - IPFS UI kit - [_png_](img/ipfs-ui-kit.png) - _wip on a UI style guide_
  - Web UI Wireframes - [_invision_](https://app.zeplin.io/project/5a32d45d1a17248135241058)
  - Design Tools Research - [google doc](https://docs.google.com/document/d/1qJyfwgcMg8l3Tk3aYxF38iyYRhkEf3nlLNqOw4ZiW_8/edit)
  - [IPFS color palette](resources/color-palette.md) in a bunch of formats
  - [Research](research) including the original definition of this project


## Get involved!

### Join our open meetings

We'd love to meet you in person at one of our open meetings. They're a great way to get quickly up to speed on our work, including latest developments and awesome demos.

- **When:** Every other Wednesday at 17:00 UTC (check the [IPFS Calendar](https://calendar.google.com/calendar/embed?src=ipfs.io_eal36ugu5e75s207gfjcu0ae84@group.calendar.google.com&ctz=UTC) to see exact dates!)
- **Where:** https://protocol.zoom.us/j/833247793
- **Agenda**: https://hackmd.io/QaxiCU8BQqOuK8B8Tdi36g

You can also explore [recordings](https://www.youtube.com/playlist?list=PLuhRWgmPaHtRIXVTy_ngBwvsXvWw10mR8) and [notes](https://github.com/ipfs/team-mgmt/tree/master/meeting-notes) from past meetings any time.

### Contribute

Contributions to our work are more than welcome! The easiest way to see what issues are prioritized and on deck is to use our [unified public ZenHub board](https://app.zenhub.com/workspaces/-ipfs-app-family-ux-5e7a3123e969e659cdebb5e6/board?repos=111841602,32695583,36580101,24483721,142161410,119716282,116711586,38799513,142181521,147528357,148369983,40225364,104770273); our work hits a lot of repos, so having them in one place offers a good birds-eye view.

If you don't want to use ZenHub, that's cool too. Each of the repos listed under ["All projects"](#all-projects) above makes use of the IPFS Project's global issue labeling scheme. Good labels to look for are ...
- `help wanted`
- `good first issue`
- and there are even occasional `bounty` labels for issues with rewards as part of the [IPFS Bounty Board](https://github.com/ipfs/devgrants/projects/1)!

If you see an issue that catches your eye, leave a comment so we know you're interested, and we'll go from there!

We're an open project and a friendly group, so please be nice and **read the [contributing guidelines](https://github.com/ipfs/community/blob/master/CONTRIBUTING_JS.md)** when you're ready to jump in.

### Discuss in GitHub or IRC

We do hang out on IRC — see the <a href="https://www.irccloud.com/invite?channel=%23ipfs-gui&amp;hostname=irc.freenode.net&amp;port=6697&amp;ssl=1"> #ipfs-gui channel on irc.freenode.net</a> — but for the sake of async communication, archiving, and searchability, we encourage discussions to happen in the context of GitHub issue comments whenever practical.

## Maintainers

- [@alanshaw](https://github.com/alanshaw): WebUI and Companion dev
- [@fsdiogo](https://github.com/fsdiogo): WebUI and Companion dev
- [@hacdias](https://github.com/hacdias): Desktop lead dev and WebUI dev
- [@jessicaschilling](https://github.com/jessicaschilling): UX strategist and sometimes-PM
- [@lidel](https://github.com/lidel): Companion lead dev
- [@olizilla](https://github.com/olizilla): WebUI lead dev
- [@rafaelramalho19](https://github.com/rafaelramalho19): Front-end dev across all GUI projects
- **... and you!**




[IPFS Web UI]: https://github.com/ipfs-shipyard/ipfs-webui "Web-based IPFS file manager and network explorer"
[IPFS Desktop]: https://github.com/ipfs-shipyard/ipfs-desktop "Launch and manage IPFS from a desktop app"
[IPFS Companion]: https://github.com/ipfs/ipfs-companion "Integrate IPFS with your browser"
