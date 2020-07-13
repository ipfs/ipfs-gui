# The IPFS GUI group
*Half of the IPFS [Web Browsers](https://github.com/ipfs/in-web-browsers) & GUI Working Group*

[![Made by icon.](https://img.shields.io/badge/made%20by-Protocol%20Labs-blue.svg?style=flat)](https://protocol.ai/)
[![Project icon.](https://img.shields.io/badge/project-IPFS-blue.svg?style=flat)](http://ipfs.io/)
[![#ipfs](https://img.shields.io/badge/irc-%23ipfs-brightgreen.svg)](https://webchat.freenode.net/?channels=ipfs) <a href="https://www.irccloud.com/invite?channel=%23ipfs-gui&amp;hostname=irc.freenode.net&amp;port=6697&amp;ssl=1" target="_blank"><img src="https://img.shields.io/badge/irc-%23ipfs--gui-brightgreen.svg?style=flat"  height="20"></a>

Our goal is to **create visual and interaction standards and patterns for working with IPFS that are ...**

- **Simple**: Present the big ideas of IPFS clearly, without unnecessary complexity
- **Accessible**: Enable *everyone* to take advantage of what IPFS offers
- **Reusable**: Offer compelling standards and atomic patterns to the community of IPFS builders
- **Beautiful**: By their nature, things that are simple, accessible and reusable are also beautiful

## IPFS GUI projects

### Primary projects

Our primary focus is on the three Protocol Labs-led "helper" apps that provide a GUI for IPFS as a whole. Our aim is to make them useful for seasoned IPFS developers while also offering a welcoming introduction to IPFS for those less experienced.

| IPFS Companion | IPFS Web UI | IPFS Desktop |
|:-:|:-:|:-:|
| [<img title="IPFS Companion" src="https://ipfs.io/images/ipfs-companion-hex.png" />][IPFS Companion] | [<img title="Web UI screenshot" src="img/webui-hex.png" />][IPFS Web UI] | [<img title="IPFS Desktop" src="https://ipfs.io/images/ipfs-desktop-hex.png" />][IPFS Desktop] |
| [Browser extension](https://github.com/ipfs/ipfs-companion) for opening ipfs:// URLs, saving/sharing files, and more| [IPFS file manager and network explorer](https://github.com/ipfs-shipyard/ipfs-webui) in your browser | Launch and manage IPFS from a friendly, intuitive [desktop app](https://www.github.com/ipfs-shipyard/ipfs-desktop) |

For a more comprehensive overview of the resources that come together to build, support, and provide education around Web UI, Desktop, and Companion, please see the [IPFS GUI Family Mental Model](https://ipfs-gui-mental-model.netlify.app/) and our [June 2020 user research report](https://docs.google.com/document/d/1V5sDSxMqhhplpcB8u8CffiGWHUvw-t4p_sn5vigdR90/edit#).

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

## Q3 2020 update

### Now half of the Web Browsers & GUI Working Group!

After a Q2 of [research](https://docs.google.com/document/d/1V5sDSxMqhhplpcB8u8CffiGWHUvw-t4p_sn5vigdR90/edit#) and [analysis](https://ipfs-gui-mental-model.netlify.app/) — as well as seeing the concrete gains provided by GUI-based work on IPFS — the IPFS core team has re-activated the **Web Browsers & GUI Working Group** as a combined team of this group and the [IPFS in-web-browsers group](https://github.com/ipfs/in-web-browsers). This larger working group operates with a focus on furthering browser adoption and integration, as well as improving the functionality and usability of our GUI-based tools as a whole, with a particular focus on benefiting the onboarding of new IPFS developers and users.

### Q3 2020 OKRs (WG-wide)

As with every team within IPFS, the Web Browsers & GUI Working Group sets and adheres to quarterly OKRs (Objectives and Key Results) in order to guide our work. (You can see [all of the IPFS Project's quarterly OKRs here](https://docs.google.com/spreadsheets/d/1KVe3JCsfB-l47-DE5gvk7bT0Yly_EAPrHCi-8kCthy4/edit#gid=2125992746).)

1. Remote (third-party) pinning services are easy to use
    - Generic pinning service API spec finalized
    - `go-ipfs`/`js-ipfs`/http-client support remote pins via HTTP API
    - User flows resulting from API are understood and implemented in IPFS Companion and IPFS Desktop/Web UI
    - 2+ collabs implement API and are included in Desktop/Web UI's pinning service settings
    - Desktop/Web UI is capable of importing a 4GB file on low-memory devices
2. Maintain and improve GUI tools as a whole (as bandwidth permits in a quarter focused on Filecoin enablement)
    - Grow IPFS usage through onboarding improvements
    - Ship libs for sharing IPFS nodes across browsing contexts (tabs) on same origin
    - Understand sharing an IPFS node across different origins
    - Understand ways of leveraging IPFS Desktop when present
3. Ongoing browser collabs and grants are supported
    - Brave integration of embedded `go-ipfs` and native URIs
    - Igalia’s work on `navigator.registerProtocolHandler` and browser extension APIs
    - Kiwix is able to host ZIM on IPFS

## Get involved!

### Join a meeting

We'd love to meet you in person at one of our open Web Browsers & GUI Working Group meetings. They're a great way to get quickly up to speed on our work, including latest developments and awesome demos.

- **When:** Every other Tuesday at 16:30 UTC (check the [IPFS Calendar](https://calendar.google.com/calendar/embed?src=ipfs.io_eal36ugu5e75s207gfjcu0ae84@group.calendar.google.com&ctz=UTC) to see exact dates!)
- **Where:** https://protocol.zoom.us/j/833247793
- **Agenda**: https://hackmd.io/QaxiCU8BQqOuK8B8Tdi36g

You can also explore [recordings](https://www.youtube.com/playlist?list=PLuhRWgmPaHtRIXVTy_ngBwvsXvWw10mR8) and [notes](https://github.com/ipfs/team-mgmt/tree/master/meeting-notes) from past meetings any time.

### Contribute to an issue

Contributions to our work are more than welcome! The easiest way to see what issues are prioritized and on deck across the GUI space is to use our [unified public ZenHub board](https://app.zenhub.com/workspaces/-ipfs-app-family-ux-5e7a3123e969e659cdebb5e6/board?repos=111841602,32695583,36580101,24483721,142161410,119716282,116711586,38799513,142181521,147528357,148369983,40225364,104770273); our work hits a lot of repos, so having them in one place offers a good birds-eye view.

If you don't want to use ZenHub, that's cool too. Each of the repos listed under ["All projects"](#all-projects) above makes use of the IPFS Project's [global issue labeling scheme](https://github.com/ipfs/community/blob/master/ISSUE_LABELS.md). Good labels to look for are ...
- `help wanted`
- `good first issue`
- and there are even occasional `bounty` labels for issues with rewards as part of the [IPFS Bounty Board](https://github.com/ipfs/devgrants/projects/1)!

If you see an issue that catches your eye, leave a comment so we know you're interested, and we'll go from there!

We're an open project and a friendly group, so please be nice and **read the [contributing guidelines](https://github.com/ipfs/community/blob/master/CONTRIBUTING_JS.md)** when you're ready to jump in.

### Discuss in GitHub or IRC

We do hang out on IRC — see the [#ipfs](https://www.irccloud.com/invite?channel=%23ipfs&amp;hostname=irc.freenode.net&amp;port=6697&amp;ssl=1") and [#ipfs-gui](https://www.irccloud.com/invite?channel=%23ipfs-gui&amp;hostname=irc.freenode.net&amp;port=6697&amp;ssl=1") channels on irc.freenode.net — but for the sake of async communication, archiving, and searchability, we encourage discussions to happen in the context of GitHub issue comments whenever practical.

## Resources

If you're looking for high-level research or visual and brand info, these resources may be helpful.

- [IPFS GUI Family Mental Model](https://ipfs-gui-mental-model.netlify.app/): June 2020 framework for understanding how IPFS’ various GUI-based tools work together to provide cohesive, consistent enablers to using and building on IPFS for a variety of developer and non-developer stakeholder groups
- [June 2020 user research report](https://docs.google.com/document/d/1V5sDSxMqhhplpcB8u8CffiGWHUvw-t4p_sn5vigdR90/edit#): Survey analysis offering guidance on next actions for enhancements to the IPFS GUI tool family
- [Original GUI project research](research): Spring 2018 foundational research on IPFS GUIs, including the initial definition of this group's goals
- [IPFS color palette](https://github.com/ipfs-shipyard/ipfs-css#colors): Official IPFS colors as part of [`ipfs-css`]((https://github.com/ipfs-shipyard/ipfs-css)
- [IPFS logo files](https://github.com/ipfs-inactive/logo): Vector and raster logo assets
- [IPFS brand book](https://github.com/ipfs-shipyard/ipfs-ui-style-guide/files/1629262/IPFS_brandbook.pdf): IPFS-wide brand guidance, including logo guidelines
- [IPFS UI Summary](img/ipfs-ui-kit.png): Alpha-version UI style guide summary

## Maintainers
- [@lidel](https://github.com/lidel): GUI/In-Web-Browsers WG lead and Companion lead dev
- [@gozala](https://github.com/gozala): Developer and researcher across all projects
- [@hacdias](https://github.com/hacdias): Desktop lead dev and WebUI dev
- [@jessicaschilling](https://github.com/jessicaschilling): UX strategist, occasional PM and front-end dev
- [@olizilla](https://github.com/olizilla): WebUI lead dev
- [@rafaelramalho19](https://github.com/rafaelramalho19): Front-end dev across all projects
- **... and you!**




[IPFS Web UI]: https://github.com/ipfs-shipyard/ipfs-webui "Web-based IPFS file manager and network explorer"
[IPFS Desktop]: https://github.com/ipfs-shipyard/ipfs-desktop "Launch and manage IPFS from a desktop app"
[IPFS Companion]: https://github.com/ipfs/ipfs-companion "Integrate IPFS with your browser"
