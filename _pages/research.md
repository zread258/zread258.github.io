---
layout: page
title: Research
permalink: /research/
nav: true
nav_order: 1
description: Research interests in compiler abstractions, GPU and heterogeneous systems, and hardware–software co-design.
_styles: |
  .post-description { max-width: 72ch; }
  .research-lead { max-width: 74ch; margin-bottom: 2.6rem; font-size: 1.08rem; line-height: 1.7; }
  .research-area { display: grid; grid-template-columns: 13rem minmax(0, 1fr); gap: 2rem; padding: 1.8rem 0; border-top: 1px solid var(--global-divider-color); }
  .research-area h2 { margin: .1rem 0 0; font-size: 1.2rem; line-height: 1.35; }
  .research-area p:first-child { margin-top: 0; }
  .research-area p:last-child { margin-bottom: 0; }
  .research-keywords { color: var(--global-text-color-light); font-size: .9rem; line-height: 1.55; }
  @media (max-width: 767px) { .research-area { grid-template-columns: 1fr; gap: .65rem; } }
---

<p class="research-lead">My research sits at the intersection of compilers and computer systems. I am interested in how program representations can preserve application-level structure long enough for compiler and runtime systems to make better decisions about computation, memory, parallelism, and hardware mapping.</p>

<section class="research-area" aria-labelledby="compiler-abstractions">
  <div>
    <h2 id="compiler-abstractions">Compiler Abstractions and Optimization</h2>
    <p class="research-keywords">MLIR/LLVM · intermediate representations · program transformation · code generation</p>
  </div>
  <div>
    <p>I am interested in intermediate representations and compiler abstractions that retain information usually lost during lowering. Such information can enable transformations that are difficult to recover from low-level kernels alone, especially for structured scientific, graphics, and AI workloads.</p>

    <p>More broadly, I study how the choice and organization of compiler IRs influence where an optimization can be expressed and how reliably it can be composed with later lowering passes. This includes domain-specific languages, compiler analyses, structured program rewriting, optimization placement, and target-aware code generation. I value compiler designs that make semantic assumptions explicit and expose a clear path from high-level structure to efficient executable code.</p>

  </div>
</section>

<section class="research-area" aria-labelledby="gpu-systems">
  <div>
    <h2 id="gpu-systems">GPU and Heterogeneous Systems</h2>
    <p class="research-keywords">CUDA · memory hierarchy · profiling · parallel execution · multi-GPU systems</p>
  </div>
  <div>
    <p>I work with GPU workloads from both compiler and systems perspectives, including CUDA code generation, memory hierarchy, synchronization, occupancy, kernel profiling, and heterogeneous execution. I am particularly interested in connecting low-level performance behavior back to compiler-level optimization decisions.</p>

    <p>This perspective requires reasoning across abstraction boundaries: an apparently local transformation can change memory traffic, expose or restrict parallelism, alter synchronization requirements, and affect the runtime behavior of a larger application. My experience with GPU profiling and distributed inference systems informs how I evaluate those interactions. I am interested in compilation and runtime techniques that make such tradeoffs systematic while remaining grounded in measurements from real hardware.</p>

  </div>
</section>

<section class="research-area" aria-labelledby="architecture-codesign">
  <div>
    <h2 id="architecture-codesign">Architecture and Hardware–Software Co-design</h2>
    <p class="research-keywords">RISC-V · FPGA prototyping · memory systems · accelerators</p>
  </div>
  <div>
    <p>My architecture background includes processor implementation, FPGA prototyping, memory-system interfaces, and ISA-level validation. I am interested in using this background to study compiler and runtime techniques for increasingly heterogeneous computing systems.</p>

    <p>Building and validating a processor made the boundary between architectural intent and software-visible behavior concrete: instruction semantics, control hazards, exceptions, and memory protocols all shape the environment in which generated code executes. I want to connect that architectural understanding with compiler abstractions for accelerators and heterogeneous platforms. The long-term goal is to help software express useful structure without sacrificing the predictability and efficiency required by modern hardware.</p>

  </div>
</section>
