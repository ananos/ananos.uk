---
layout: work_item
tags: [fiction]
work: true
title: "Lightweight Apps"
icon: fa-code
---

I'm also looking into <a href="http://unikernel.org">unikernels</a>, and how this technology can facilitate
deployment of cloud-native apps, without sacrificing performance, isolation,
and security.

We are exploring various unikernel frameworks, mainly <a
href="https://github.com/rumpkernel/rumprun">Rumprun</a>, <a
href="https://github.com/Solo5/solo5">Solo5</a>, and <a
href="https://github.com/unikraft/unikraft">Unikraft</a>.

Our main goal is to make it easier for end-users to deploy their apps in a
unikernel, as well as run a unikernel efficiently, either in the Cloud or at
the Edge. To this end, we have been doing some work regarding <a
href="https://blog.cloudkernels.net/posts/nabla-containers-aarch64/">aarch64</a>
support for rumprun over solo5, optimizing container runtime support for
unikernels, while porting unikernel frameworks to lightweight VMMs.

