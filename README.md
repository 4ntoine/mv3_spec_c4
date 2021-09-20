C4 model for Manifest V3 changes for ad blocking extension

# Architecture

## Context

**WebExt Core developers** provide a web extension SDK to **WebExt developers**. They use it in the ad blocking web extension and publish it to the **Chrome store**. **Chrome store moderators** review and approve the web extension updates. **Users** can search for an ad blocking extension and install it in desktop **Browser**. Once installed in the browser an ad blocking extension provides ad-filtered UX while navigating to the web sites. Browser extension keeps filter subscriptions up-to-date by requesting the updates from filters **Back-end** which is developed and supported by **Filter developers and Ops team**. Back-end fetches the changes from the **Public filter rules repositories** maintained by the **Filter authors**.

![Context diagram](https://www.plantuml.com/plantuml/proxy?cache=no&src=https://raw.githubusercontent.com/4ntoine/mv3_spec_c4/master/context.txt)

## Containers

### Browser containers

As a deplayable thing a web extension is a single file. As a runnable thing a web extension is separated into *Content script* and *webext Background script* which are hosted in separate processes. Once installed a background script is executed as a *Service worker*. One a new page (tab) is loaded, a content script is injected into its context. Both scripts are able to communicate with Browser via public APIs (that are different for script type) and together via messages. Web extension (background script) fetches the changes from filters back-end.

![Browser containers diagram](https://www.plantuml.com/plantuml/proxy?cache=no&src=https://raw.githubusercontent.com/4ntoine/mv3_spec_c4/master/containers_browser.txt)

### Back-end containers

![Back-end containers diagram](https://www.plantuml.com/plantuml/proxy?cache=no&src=https://raw.githubusercontent.com/4ntoine/mv3_spec_c4/master/containers_backend.txt)

## Components

TBD later.

## Code

TBD later.

# Open questions

* Snippets?
* WebExt on Containers diagram: split into separate containers (runnable things - Content/Background ) or keep single (single deployable thing)?
* Browser on Containers diagram: keep Browser detailed (components)? Describe Chrome processes (main, child, extension)?
* Filters origin server: show processes?

# TODO

* Close open questions
* Review and discuss together with teams
* Describe Components and Code as we go.