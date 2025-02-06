---
title: "WAMR 2024: A Year in Review"
description: ""
excerpt: ""
date: 2024-01-21T09:20:00+08:00
lastmod: 2024-02-06T09:41:07+08:00
draft: false
weight: 20
images: []
categories: ['summary']
tags: []
contributors: ['Liang He']
pinned: false
homepage: false
---

# WAMR 2024: A Year in Review

In 2024, the WAMR community saw many thrilling advancements, including the development of new features, increased industrial use, and an improved experience for developers. Passionate developers and industry professionals have come together to enhance and expand WAMR in ways we couldn't have imagined. From exciting new tools to a growing community, there's a lot to be proud of. Let's take a closer look at the key highlights of WAMR 2024, showcasing the community's efforts, new features, and the establishment of the Embedded Special Interest Group (ESIG).

## Community Contributions: A Year of Growth

The WAMR community has shown [incredible dedication and enthusiasm throughout 2024](https://next.ossinsight.io/analyze/bytecodealliance?period=past_12_months&repoIds=184654298#overview). Here are some impressive numbers that highlight the community's contributions:

- 707 New PRs: The community has been actively involved in enhancing WAMR, with 707 new PRs submitted this year.
- 292 New Issues: Developers have identified and reported 292 new issues, helping to improve the stability and performance of WAMR.
- 861 New Stars on GitHub: The project gained 861 new stars, reflecting its growing popularity and recognition.
- 236 Active Participants: With 236 active participants, the community has been vibrant and engaged, driving WAMR forward with their collective efforts.

Breaking down the contributions further:

- Intel and Others: Half of the PRs, 43.85%, were created by Intel, while the remaining 56.15% were created by the community, including independent contributors and customers integrating WAMR into their products.
- Community Contributions: The major driving force within the community is company contributors, who provided approximately 85% of the PRs among those created by non-Intel contributors.

The top three non-Intel organized contributors have made significant impacts:

- Midokura: Contributed 33.33% of organized PRs and helped review 35.01% of PRs.
- Amazon: Contributed 14.33% of organized PRs and helped review 19.90% of PRs.
- Xiaomi: Contributed 12.40% of organized PRs and helped review 15.11% of PRs.

These contributions have been instrumental in driving WAMR forward, and we extend our heartfelt thanks to everyone involved.

## New Features in WAMR 2024

Several exciting new features have been added to WAMR in 2024, aimed at enhancing the development experience and expanding the capabilities of WAMR. Here are some of the key features:

### Development Tools: Simplifying Wasm Development

One of the most exciting additions to WAMR in 2024 is the introduction of new development tools aimed at simplifying Wasm development. These tools include:

- Linux perf for Wasm Functions: This tool allows developers to profile Wasm functions directly, providing insights into performance bottlenecks.
- AOT Debugging: Ahead-of-time (AOT) debugging support has been added, making it easier to debug Wasm applications.
- Call Stack Dumps: Enhanced call stack dumps provide detailed information about the execution flow, aiding in troubleshooting and optimization.

Before these tools, developing a Wasm application or plugin using a host language was a complex task. Mapping Wasm functions back to the source code written in the host language required deep knowledge and was often cumbersome. Debugging information from the runtime and the host language felt like two foreign languages trying to communicate without a translator. These new development tools act as that much-needed translator, bridging the gap and making Wasm development more accessible and efficient.

### Shared Heap: Efficient Memory Sharing

Another significant feature introduced in 2024 is the shared heap. This feature addresses the challenge of sharing memory between the host and Wasm. Traditionally, copying data at the host-Wasm border was inefficient, and existing solutions like externref lacked flexibility and toolchain support.

The shared heap approach uses a pre-allocated region of linear memory as a "swap" area. Both the embedded system and Wasm can store and access shared objects here without the need for copying. However, this feature comes with its own set of challenges. Unlike memory.grow(), the new memory region isn't controlled by Wasm and may not even be aware of it. This requires runtime APIs to map the embedded-provided memory area into linear memory, making it a runtime-level solution rather than a Wasm opcode.

### Newly Implemented Features

Several features have been finalized in 2024, further enhancing WAMR's capabilities:

- GC: Garbage collection features for the interpreter, LLVM-JIT, and AOT have been finalized.
- Legacy Exception Handling: Legacy exception handling for the interpreter has been added.
- WASI-NN: Support for WASI-NN with OpenVINO and llama.cpp backends has been introduced.
- WASI Preview1 Support: Ongoing support for WASI on ESP-IDF and Zephyr.
- Memory64: Table64 support for the interpreter and AOT has been finalized.

These new features and improvements are designed to make WAMR more powerful and easier to use, catering to the needs of developers and industry professionals alike.

## Active engagement in Embedded Special Interest Group (ESIG)

In the embedding industry, the perspective on Wasm differs slightly from the cloud-centric view that the current Wasm Community Group (CG) often focuses on. To address these unique requirements, the Embedded Special Interest Group (ESIG) was established in 2024. This group aims to discover solutions that prioritize performance, footprint and stability, tailored specifically for embedding devices.

The ESIG has already achieved several accomplishments this year, thanks to the shared understanding and collaboration with customers. By focusing on the unique needs of the embedding industry, ESIG is paving the way for more specialized and efficient Wasm solutions.

## Industrial adoption

The adoption of WAMR in the industry has been remarkable, with several key players integrating WAMR into their systems to leverage its performance and flexibility. Here are some notable examples:

Alibaba's Microservice Engine (MSE) has adopted WAMR as a Wasm runtime to execute Wasm plugins in their gateways Higress. This integration has resulted in an [impressive ~50% performance improvement](https://www.alibabacloud.com/blog/higresss-new-wasm-runtime-greatly-improves-performance_601025), showcasing the efficiency and robustness of WAMR in real-world applications.

WAMR has also been integrated into Runwasi as one of the Wasm runtimes to execute Wasm in containerd. This integration allows for seamless execution of Wasm modules within containerized environments, providing a versatile and efficient solution for running Wasm applications.

For more information on industrial adoptions and other use cases, please refer to [this link](https://github.com/bytecodealliance/wasm-micro-runtime/blob/main/ADOPTERS.md).

These examples highlight the growing trust and reliance on WAMR in various industrial applications, demonstrating its capability to deliver significant performance enhancements and operational efficiencies.

## Conclusion

2024 has been a transformative year for WAMR, marked by significant community contributions, innovative features, and the establishment of the ESIG. As we look ahead, we are excited about the continued growth and evolution of WAMR, driven by the passion and dedication of our community. We invite you to join us on this journey, explore the new features, and contribute to the future of WebAssembly Micro Runtime.

Thank you for being a part of the WAMR community. Here's to an even more exciting 2025!
