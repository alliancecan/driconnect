# DRI Connect Website

This repo stores content for the DRI Connect website.

[Netlify](https://netlify.com) is configured to monitor this repo. Various actions trigger preview deploys for PRs, branch deploys for specific branches,
and production deploys off `main` (production deploys go to the [live website](https://driconnect.alliancecan.ca)).

When a deploy is triggered, [Hugo](https://gohugo.io/) is run against `driconnect/content`.

The resulting static HTML is used as the artifact that is deployed.
