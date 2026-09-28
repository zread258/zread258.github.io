---
layout: page
title: Experience
permalink: /experience/
nav: true
nav_order: 2
description: Research and engineering experience in compilation, GPU systems, and AI infrastructure.
_styles: |
  .experience-list { margin-top: 2rem; border-top: 1px solid var(--global-divider-color); }
  .experience-entry { display: grid; grid-template-columns: 10.5rem minmax(0, 1fr); gap: 2rem; padding: 2rem 0; border-bottom: 1px solid var(--global-divider-color); }
  .experience-date { font-size: .9rem; color: var(--global-text-color-light); }
  .experience-entry h2 { margin: 0; font-size: 1.25rem; }
  .experience-role { margin: .25rem 0 0; font-weight: 500; }
  .experience-location { margin: .1rem 0 1rem; color: var(--global-text-color-light); font-size: .92rem; }
  .experience-entry ul { margin-bottom: 0; padding-left: 1.2rem; }
  .experience-entry li { margin-bottom: .55rem; }
  @media (max-width: 700px) { .experience-entry { grid-template-columns: 1fr; gap: .55rem; } }
---

<div class="experience-list">
  <section class="experience-entry" aria-labelledby="ubiquant">
    <div class="experience-date">Aug. 2026 – Sep. 2026</div>
    <div>
      <h2 id="ubiquant">Ubiquant Technology Co.</h2>
      <p class="experience-role">Quantitative Implementation Intern</p>
      <p class="experience-location">Shanghai, China</p>
      <ul>
        <li>Evaluated multi-node, multi-GPU LLM serving with SGLang and vLLM under prefill–decode disaggregation, characterizing TTFT/TPOT trade-offs across distributed execution configurations.</li>
        <li>Investigated Mooncake-based KV-cache transfer and profiled compute, memory, and communication bottlenecks across prefill/decode placement strategies.</li>
      </ul>
    </div>
  </section>

  <section class="experience-entry" aria-labelledby="shanghai-ai-lab">
    <div class="experience-date">Jan. 2026 – Jul. 2026</div>
    <div>
      <h2 id="shanghai-ai-lab">Shanghai Artificial Intelligence Laboratory</h2>
      <p class="experience-role">Research Intern</p>
      <p class="experience-location">Shanghai, China</p>
      <ul>
        <li>Designed and implemented an MLIR-based domain-specific compiler for GPU-intensive graphics workloads, preserving high-level application semantics through optimization and CUDA lowering.</li>
        <li>Developed semantics-guided compiler optimizations that coordinate program rewriting, computation placement, and GPU memory decisions across the compilation pipeline.</li>
        <li>Evaluated the compiler across representative workloads and multiple GPU architectures against hand-written CUDA and existing high-level programming systems, demonstrating substantial performance gains while improving programmability.</li>
        <li>One manuscript resulting from this work is currently under double-blind review; identifying details will be added after the review period.</li>
      </ul>
    </div>
  </section>

  <section class="experience-entry" aria-labelledby="houmo">
    <div class="experience-date">Apr. 2025 – Jul. 2025</div>
    <div>
      <h2 id="houmo">Houmo Technology Co.</h2>
      <p class="experience-role">AI Compiler Development Intern</p>
      <p class="experience-location">Nanjing, China</p>
      <ul>
        <li>Implemented 44 ONNX operators end-to-end for a RISC-V-based compute-in-memory NPU, spanning MLIR dialect definitions, pattern rewriting, and lowering to accelerator-specific primitives.</li>
        <li>Built MLIR lowering and validation pipelines that mapped ONNX operators to backend execution constraints and regression-tested outputs against ONNX Runtime.</li>
      </ul>
    </div>
  </section>
</div>
