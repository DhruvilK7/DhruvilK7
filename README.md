<h1 align="center">Hi, I'm Dhruvil 👋</h1>

<p align="center">
  <a href="https://git.io/typing-svg">
    <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=20&pause=1000&color=58A6FF&center=true&vCenter=true&width=600&lines=SDE+II+%40+Zomato;Go+%7C+Distributed+Systems+%7C+Data+Structures;Currently+deep+in+Valkey%2FRedis+internals" alt="Typing SVG" />
  </a>
</p>

I work on Zomato's Infra team — cloud architecture across every service, AWS, and the shared Go libraries (logging, config, gRPC, caching, messaging) that other teams build on without thinking about.

I like taking a systems paper and turning it into working, benchmarked Go code — that's where most of my open-source time goes.

### Open Source

**[RibbonFilter/ribbonGo](https://github.com/RibbonFilter/ribbonGo)** · Creator & Maintainer

First pure Go implementation of the Ribbon filter (Dillinger & Walzer, 2021). 4.7% overhead above the information-theoretic minimum, 12.7% more space-efficient than Bloom filters at equivalent FPR. SoA memory layout, software-pipelined prefetching, zero heap allocations on build and query hot paths.

**[RoaringBitmap/roaring](https://github.com/RoaringBitmap/roaring)** · Contributor (2.9K+ stars, used by InfluxDB, Bleve, DataDog)

- [feature: `CardinalityInRange`](https://github.com/RoaringBitmap/roaring/pull/513) - binary search based range counting, up to 99% faster than full-scan Rank approach on narrow ranges
- [perf: In-place XOR](https://github.com/RoaringBitmap/roaring/pull/509) - across array, bitmap, and run containers; 44% speedup, 100% fewer allocations
- [perf: Galloping intersects2by2](https://github.com/RoaringBitmap/roaring/pull/512) - skip-ahead for skewed set sizes (64x ratio)

**[valkey-io/valkey-glide](https://github.com/valkey-io/valkey-glide)** · Contributor (Go client)

- [perf: Dropped FFI call from response type checks](https://github.com/valkey-io/valkey-glide/pull/6899) - perf optimization in the Go client hot path
- [feature: AzAffinityAllNodes read strategy](https://github.com/valkey-io/valkey-glide/pull/6927)

**[valkey-io/valkey-go](https://github.com/valkey-io/valkey-go)** · Contributor (fast Valkey/Redis client with auto-pipelining and client-side caching)

- [bug: Re-pick unfinished commands between retry iterations](https://github.com/valkey-io/valkey-go/pull/151) - fixed an unbounded retry loop in `DoMulti`/`DoMultiCache` when a replica drops mid-flight; rebuckets against the refreshed slot map, preserves ASK routing, keeps transaction spans coherent. Regression tests for replica removal, mixed ASK/transport errors, and response ordering.
- [perf: Consolidate keyless commands onto one conn on retry](https://github.com/valkey-io/valkey-go/pull/180) - stops fanning out keyless commands across arbitrary picks during retries
- [feature: Opt-in `PreferClusterShards`](https://github.com/valkey-io/valkey-go/pull/181) - use `CLUSTER SHARDS` ahead of version 8 on patched servers, avoids routing to nodes still loading during rolling upgrades



### Elsewhere
<p align="left">
  <a href="mailto:kakadiyadhruvil3006@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=flat&logo=gmail&logoColor=white" /></a>
  <a href="linkedin.com/in/dhruvil-kakadiya-6aa45b31b/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white" /></a>
</p>
