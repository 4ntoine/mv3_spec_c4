C4 model for Manifest V3 changes for ad blocking extension

## Context

**WebExt Core developers** provide a web extension SDK to **WebExt developers**. They use it in the ad blocking web extension and publish it to the **Chrome store**. **Chrome store moderators** review and approve the web extension updates. **Users** can search for an ad blocking extension and install it in desktop **Browser**. Once installed in the browser an ad blocking extension provides ad-filtered UX while navigating to the web sites. Browser extension keeps filter subscriptions up-to-date by requesting the updates from filters **Back-end** which is developed and supported by **Filter developers and Ops team**. Back-end fetches the changes from the **Public filter rules repositories** maintained by the **Filter authors**.

![Context diagram](https://www.plantuml.com/plantuml/proxy?cache=no&src=https://raw.githubusercontent.com/4ntoine/mv3_spec_c4/master/context.txt)

## Containers

### Browser container

![Browser container diagram](https://www.plantuml.com/plantuml/proxy?cache=no&src=https://raw.githubusercontent.com/4ntoine/mv3_spec_c4/master/containers_browser.txt)

## Components

## Code