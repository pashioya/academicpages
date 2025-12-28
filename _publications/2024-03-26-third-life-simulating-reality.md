---
title: "Third Life: Simulating Reality"
collection: publications
category: manuscripts
permalink: /publication/2009-10-01-paper-title-number-1
excerpt: 'Built by our three-person team, “Third Life” is a large-scale civilisation simulation (Rust + Bevy ECS) that can replay centuries across thousands of citizens, with results stored in Postgres and visualised in Grafana.'
date: 2024-03-26
venue: 'Dev-To'
slidesurl: ""
paperurl: 'https://dev.to/tomellm/third-life-simulating-reality-41if'
bibtexurl: ""
itation: 'Paul Ashioya, You. (2009). &quot;Paper Title Number 1.&quot; <i>Journal 1</i>. 1(1).'
---
We built “Third Life,” a large-scale civilisation simulation that models thousands of citizens across multiple worlds, letting centuries of social, agricultural, and economic change unfold quickly while we rerun scenarios under different starting conditions to see how histories diverge. To handle the computational load, the three of us chose Rust with the Bevy game engine and an ECS architecture, which let us represent citizens and their relationships as components and run highly parallel systems efficiently; we also used bevy_egui for UI/plots, serde for configuration, and async/task tooling to keep iteration fast. For data collection and visualisation, we initially tried InfluxDB because the simulation outputs are time-series-like, but we hit practical limits (timestamp range and slow large queries), so we moved to PostgreSQL for reliable long-range timestamps and smoother analytics, then surfaced results in Grafana dashboards. Overall, Bevy’s speed and flexibility made rapid feature work possible once we adapted to the ECS paradigm, and if we restarted we’d push Rust’s abstractions further to make our systems more generic and expand the simulation’s breadth for richer emergent behaviour.
