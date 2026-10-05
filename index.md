---
layout: home
title: AllStarLink Node [NODE NUMBER]
---

This page is maintained by {{ site.callsign }} as the off-node reference for
AllStarLink node {{ site.node_number }}. It exists so information about the node —
what it does, how it's used, and what's changed over time — stays
available even if the node itself is offline.

{% comment %}
Live Online/Offline indicator (Starter Kit v1.2). It shows whether
AllStarLink has heard from your node recently. It reads your node number
automatically from _config.yml — nothing to fill in here. To remove the
indicator, delete this whole comment block and the include line below it.
To allow longer gaps before it shows Offline, add stale="30" inside the
include tag.
{% endcomment %}
{% include node-status.html %}

- **[About This Node](about.md)** — what this node is and how it's used
- **[Disclaimers](disclaimers.md)** — policies, restrictions, and any
  courtesy notices
- **[Changelog](changelog.md)** — notable changes to the node over time

Questions about this node can be directed to {{ site.callsign }}. See qrz.com for contact details.