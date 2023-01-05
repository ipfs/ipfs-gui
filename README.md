# IPFS GUIs

[![Made by icon.](https://img.shields.io/badge/made%20by-Protocol%20Labs-blue.svg?style=flat)](https://protocol.ai/)
[![Project icon.](https://img.shields.io/badge/project-IPFS-blue.svg?style=flat)](http://ipfs.io/)
[![#ipfs](https://img.shields.io/badge/irc-%23ipfs-brightgreen.svg)](https://webchat.freenode.net/?channels=ipfs) <a href="https://www.irccloud.com/invite?channel=%23ipfs-gui&amp;hostname=irc.freenode.net&amp;port=6697&amp;ssl=1" target="_blank"><img src="https://img.shields.io/badge/irc-%23ipfs--gui-brightgreen.svg?style=flat"  height="20"></a>

The IPFS project has an ongoing, long-running ambition to **create visual and interaction standards and patterns for working with IPFS that are ...**

- **Simple**: Present the big ideas of IPFS clearly, without unnecessary complexity
- **Accessible**: Enable *everyone* to take advantage of what IPFS offers
- **Reusable**: Offer compelling standards and atomic patterns to the community of IPFS builders
- **Beautiful**: By their nature, things that are simple, accessible and reusable are also beautiful

## IPFS GUI projects

### Primary projects

At present, primary focus is on the three "helper" apps that provide a GUI for IPFS as a whole, in order to make them useful for seasoned IPFS developers while also offering a welcoming introduction to IPFS for those less experienced.

| IPFS Companion | IPFS Web UI | IPFS Desktop |
|:-:|:-:|:-:|
| [<img title="IPFS Companion" src="https://ipfs.io/images/ipfs-companion-hex.png" />][IPFS Companion] | [<img title="Web UI screenshot" src="img/webui-hex.png" />][IPFS Web UI] | [<img title="IPFS Desktop" src="https://ipfs.io/images/ipfs-desktop-hex.png" />][IPFS Desktop] |
| [Browser extension](https://github.com/ipfs/ipfs-companion) for opening ipfs:// URLs, saving/sharing files, and more| [IPFS file manager and network explorer](https://github.com/ipfs-shipyard/ipfs-webui) in your browser | Launch and manage IPFS from a friendly, intuitive [desktop app](https://www.github.com/ipfs-shipyard/ipfs-desktop) |

For a more comprehensive overview of the resources that come together to build, support, and provide education around Web UI, Desktop, and Companion, please see the [IPFS GUI Family Mental Model](https://ipfs-gui-mental-model.netlify.app/) and our [June 2020 user research report](https://docs.google.com/document/d/1V5sDSxMqhhplpcB8u8CffiGWHUvw-t4p_sn5vigdR90/edit#).

### Other IPFS GUI & Tools owned projects

- **[ipfs/ipfs-gui](https://www.github.com/ipfs/ipfs-gui)**: This repo, used for overall planning and cross-repo work
- **[ipfs/distributions/site](https://github.com/ipfs/distributions/tree/master/site)**: Visual side of https://dist.ipfs.io website
- **[ipfs/public-gateway-checker](https://www.github.com/ipfs/public-gateway-checker)**: Source code for https://ipfs.github.io/public-gateway-checker/
- **[ipfs/ipfs-companion](https://github.com/ipfs/ipfs-companion)**: Browser extension that simplifies access to IPFS resources on the Web
- **[ipfs/ipfs-webui](https://github.com/ipfs/ipfs-webui)**: Browser front-end for IPFS nodes
- **[ipfs/ipfs-desktop](https://github.com/ipfs/ipfs-desktop)**: An unobtrusive and user-friendly desktop application for IPFS on Windows, Mac and Linux
- **[ipld/explore.ipld.io](https://github.com/ipld/explore.ipld.io)**: Source code for https://explore.ipld.io
  - **[ipfs/ipld-explorer-components](https://github.com/ipfs/ipld-explorer-components)**: React components for https://explore.ipld.io and ipfs-webui
- **[ipfs-shipyard/i18n](https://github.com/ipfs-shipyard/i18n)**: Internationalization work across all IPFS projects
- **[ipfs-shipyard/ipfs-css](https://www.github.com/ipfs-shipyard/ipfs-css)**: Single-purpose CSS rules and font-face config to add the IPFS look and feel to your UI
- **[ipfs-shipyard/ipfs-share-files](https://www.github.com/ipfs-shipyard/ipfs-share-files)**: Source code for https://share.ipfs.io
- **[ipfs-shipyard/ipfs-ui-style-guide](https://www.github.com/ipfs-shipyard/ipfs-ui-style-guide)**: UI style guide for IPFS apps
- **[ipfs-shipyard/pinning-service-compliance](https://www.github.com/ipfs-shipyard/pinning-service-compliance)**: A test suite to help see which pinning service providers are correctly implementing the [pinning services spec](https://ipfs.github.io/pinning-services-api-spec/).
- **[ipfs-shipyard/js-pinning-service-http-client](https://github.com/ipfs-shipyard/js-pinning-service-http-client)**: A pinning service client for the browser and node
- **[ipfs-shipyard/ipfs-dag-builder-vis](https://github.com/ipfs-shipyard/ipfs-dag-builder-vis)**: A tool for creating & modifying IPFS DAG structures visually. See https://dag.ipfs.tech/ 

### Other GUI projects

In addition to the apps & repos above, other relevant GUI related tools/apps that are not owned by the IPFS GUI & Tools team are:

- **[kubo/dir-index-html](https://github.com/ipfs/go-ipfs/tree/master/assets/dir-index-html)**: Directory listing HTML for kubo (go-ipfs) gateways
- **[filecoin-station/filecoin-station](https://github.com/filecoin-station/filecoin-station)**: Filecoin Station connects your computer’s idle resources to the Filecoin network and rewards you with FIL. Taking part is simple, just launch the app and start earning.
- **[ipfs-shipyard/ipfs-check](https://github.com/ipfs-shipyard/ipfs-check)**: A tool for checking the accessibility of your data by IPFS peers
- **[laurentsenta/pl-diagnose](https://github.com/laurentsenta/pl-diagnose)**: Reimplementation & extension of https://github.com/aschmahmann/ipfs-check

### Visual design guidelines

[![IPFS-Brand-sheet-public](https://user-images.githubusercontent.com/157609/176955199-0f87b9bc-3a8d-4bd0-b9a3-48a9fe38f942.png)](https://www.figma.com/proto/mH0OlgikgKzLmbMNO3noBs/IPFS-Brand-sheet-public)

- [Figma IPFS brand sheet](https://www.figma.com/proto/mH0OlgikgKzLmbMNO3noBs/IPFS-Brand-sheet-public)
  - [Download PDF (2022)](https://ipfs.io/ipfs/QmcVRX6eArMmyTo2LQ5iDGD1BJ13FwFv8EB1oGaVmSwbwE?filename=ipfs-brand-sheet-2022.pdf)
  - [Download Assets (2022)](https://ipfs.io/ipfs/QmSwE3QkkQf914n3RRMtCprxS8qMTtxEWFHneYppdAukeR?filename=ipfs-brand-assets-2022.zip)

## Get involved!

### Contribute to an issue

Contributions to IPFS GUIs are more than welcome! Each of the repos listed under ["All projects"](#all-projects) above makes use of the IPFS Project's [global issue labeling scheme](https://github.com/ipfs/community/blob/master/ISSUE_LABELS.md). Good labels to look for are ...
- `help wanted`
- `good first issue`
- and there are even occasional `bounty` labels for issues with rewards as part of the [IPFS Bounty Board](https://github.com/ipfs/devgrants/projects/1)!

If you see an issue that catches your eye, leave a comment so we know you're interested, and we'll go from there!

We're an open project and a friendly group, so please be nice and **read the [contributing guidelines](https://github.com/ipfs/community/blob/master/CONTRIBUTING_JS.md)** when you're ready to jump in.

### Discuss in GitHub or chat

**For the sake of async communication, archiving, and searchability, we strongly encourage discussions to happen in the context of GitHub issue comments whenever practical.**

For casual conversation, our official chat rooms in [Matrix](https://app.element.io/#/room/#lobby:ipfs.io) and [Discord](https://discord.gg/Z4H6tdECb9) are bridged, so you can join whichever you prefer. They can be used to ask questions and discuss with the community — however, while IPFS core developers are usually in these rooms, it can be hard to keep up with the running conversation and questions can be missed or disappear due to a lack of indexing.

## Resources

If you're looking for high-level research or visual and brand info:

- [IPFS brand sheet](https://www.figma.com/proto/mH0OlgikgKzLmbMNO3noBs/IPFS-Brand-sheet-public?node-id=22%3A2)
  - see also: [Protocol Labs branding and visual design index](https://www.figma.com/proto/zwiBoppEK16FXV89bqDVgX/PL-%2B-project-branding-master-index?node-id=0%3A6&scaling=min-zoom)

Also, these historical resources may be helpful:

- [IPFS GUI Family Mental Model](https://ipfs-gui-mental-model.netlify.app/): June 2020 framework for understanding how IPFS’ various GUI-based tools work together to provide cohesive, consistent enablers to using and building on IPFS for a variety of developer and non-developer stakeholder groups
- [June 2020 user research report](https://docs.google.com/document/d/1V5sDSxMqhhplpcB8u8CffiGWHUvw-t4p_sn5vigdR90/edit#): Survey analysis offering guidance on next actions for enhancements to the IPFS GUI tool family
- [Original GUI project research](research): Spring 2018 foundational research on IPFS GUIs, including the initial definition of this group's goals
- [IPFS color palette](https://github.com/ipfs-shipyard/ipfs-css#colors): Official IPFS colors as part of [`ipfs-css`](https://github.com/ipfs-shipyard/ipfs-css)
- [IPFS logo files](https://github.com/ipfs-inactive/logo): Vector and raster logo assets
- [IPFS brand book](https://github.com/ipfs-shipyard/ipfs-ui-style-guide/files/1629262/IPFS_brandbook.pdf): IPFS-wide brand guidance, including logo guidelines
- [IPFS UI Summary](img/ipfs-ui-kit.png): Alpha-version UI style guide summary

## Maintainers

This `ipfs-gui` repo is intended primarily as a higher-order planning and discussion space, so isn't actively maintained in and of itself; however, consult the readmes of the repos listed under ["All projects"](#all-projects) above for more specific maintainer info for individual projects.



[IPFS Web UI]: https://github.com/ipfs-shipyard/ipfs-webui "Web-based IPFS file manager and network explorer"
[IPFS Desktop]: https://github.com/ipfs-shipyard/ipfs-desktop "Launch and manage IPFS from a desktop app"
[IPFS Companion]: https://github.com/ipfs/ipfs-companion "Integrate IPFS with your browser"

## Support goals

### Platforms

Due to the difficulty involved in debugging and development on platforms and versions not supported by github actions (and our CI/CD tests), we can only provide support for the [top 3 (mac, windows, ubuntu) `latest` platforms supported by github](https://docs.github.com/en/actions/using-github-hosted-runners/about-github-hosted-runners#supported-runners-and-hardware-resources). 

If there is a new platform release, we will support bug-fixes and feature enhancements for that new platform, but will prioritize bug-fixes for things we can automate (CI/CD supported bugs/features).

### Languages

Due to a large demand and lack of time, as a general rule, we aim to support the latest (or most popular) officially supported versions of languages. 

#### NodeJS

> Production applications should only use Active LTS or Maintenance LTS releases.

See https://nodejs.org/en/about/releases/ for the officially supported NodeJS Versions. We aim to support Active LTS or Maintenance LTS versions with a best-effort support for Current versions.

Support priority:

1. Active LTS
2. Maintenance LTS
