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

### All projects

In addition to the apps above, IPFS GUIs can be considered to include aspects of all of the following repos:

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

## Get involved!

### Contribute to an issue

Contributions to IPFS GUIs are more than welcome! Each of the repos listed under ["All projects"](#all-projects) above makes use of the IPFS Project's [global issue labeling scheme](https://github.com/ipfs/community/blob/master/ISSUE_LABELS.md). Good labels to look for are ...
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
- [IPFS color palette](https://github.com/ipfs-shipyard/ipfs-css#colors): Official IPFS colors as part of [`ipfs-css`](https://github.com/ipfs-shipyard/ipfs-css)
- [IPFS logo files](https://github.com/ipfs-inactive/logo): Vector and raster logo assets
- [IPFS brand book](https://github.com/ipfs-shipyard/ipfs-ui-style-guide/files/1629262/IPFS_brandbook.pdf): IPFS-wide brand guidance, including logo guidelines
- [IPFS UI Summary](img/ipfs-ui-kit.png): Alpha-version UI style guide summary

## Maintainers

This `ipfs-gui` repo is intended primarily as a higher-order planning and discussion space, so isn't actively maintained in and of itself; however, consult the readmes of the repos listed under ["All projects"](#all-projects) above for more specific maintainer info for individual projects.



[IPFS Web UI]: https://github.com/ipfs-shipyard/ipfs-webui "Web-based IPFS file manager and network explorer"
[IPFS Desktop]: https://github.com/ipfs-shipyard/ipfs-desktop "Launch and manage IPFS from a desktop app"
[IPFS Companion]: https://github.com/ipfs/ipfs-companion "Integrate IPFS with your browser"
