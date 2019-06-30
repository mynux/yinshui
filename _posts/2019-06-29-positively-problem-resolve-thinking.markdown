---
layout: post
category: memories
tags: []
title: "positively problem resolve thinking"
date: "2019-06-29 23:17:10 -0700"
---

以前在PCES里经常使用的一个思维模式就是排除思维，比如在build时发现3PF挂了，经常会首先思考是不是有别的code checkin了，或者是因为versionset过期导致的问题。近两次PCES versionset的经常性挂掉才发现，这些不是偶然因素，尤其是一些重复出现的symptom时，基本可以判断这个是由于某种确定性的原因导致了test的挂掉，这时候如果遇到的问题再是你自己不熟悉的，一种惰性思维会阻止你自己继续尝试解决这个use case。

通过其他逆向思考来解决问题往往就很难，最后需要积极正向的思考来帮助解决。比如

1. Amex Token Expired Tests Failed.
2. Wukong ion parse failure after upgrade.

所以，正向的思考问题，而不是逃避问题，往往在一些问题上有奇效。
