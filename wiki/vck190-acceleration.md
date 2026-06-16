# VCK190 Acceleration

## Summary

This page tracks ideas for improving the ellipse-detection/RANSAC project for the AMD/Xilinx VCK190 platform.

## Current Status

The user wants to run the project on VCK190 and evaluate how to improve it.

## Key Ideas

For VCK190, improvements should focus less on CPU-style threading and more on hardware-friendly parallelism:

- Stream pixels or edge points through kernels.
- Use deterministic memory access patterns.
- Separate host orchestration from accelerator kernels.
- Move the most expensive repeated computation to hardware.
- Avoid heavy dynamic allocation inside accelerator-oriented code.
- Avoid complex synchronization patterns that work on CPU but map poorly to FPGA/AI Engine style execution.

## Candidate Acceleration Targets

| Candidate | Why it may help | Risk |
|---|---|---|
| Inlier counting | Repeated many times and parallel over points | Needs careful memory bandwidth handling |
| Candidate evaluation | Many independent candidates | Random sampling may be hard to map cleanly |
| Edge preprocessing | Stream-friendly | May not be current bottleneck |
| Initialization search | Small fixed workload | May not justify hardware overhead |

## CPU vs VCK190 Note

An optimization can be useful on normal CPU but not ideal for VCK190. CPU OpenMP favors threads and shared memory. VCK190 acceleration favors pipelines, streaming, fixed data layout, and minimizing host-device transfers.

## Open Questions

- What part of the runtime dominates after profiling?
- Is the target implementation using Vitis HLS, AI Engine, or only ARM cores on VCK190?
- What input size and throughput target are required?
- Are results required to be bit-exact with the CPU version?

## Related Pages

- [[ransac-ellipse-detection]]
- [[openmp-parallelization]]
- [[performance-results]]

## Sources

- Project conversation notes
