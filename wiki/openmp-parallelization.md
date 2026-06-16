# OpenMP Parallelization

## Summary

This page records where the C++ ellipse-detection/RANSAC code is parallelized, how it is tested, and what should be improved.

## Current Status

Known parallelization areas from project notes:

- Image-level parallelism: multiple images can be processed independently.
- Inlier-counting parallelism: candidate ellipse evaluation can count inliers in parallel.
- Combined mode: both image loop and inlier counting are parallelized.

## Important Design Notes

Parallelizing the initialization phase with five threads, where each thread handles five initial pixels and then communicates to select the best, may be possible. However, it should be evaluated carefully because thread overhead, synchronization cost, and small workload size can make it slower on normal CPU execution.

For normal CPU runs, image-level parallelism is often the safest and simplest first improvement because images are independent.

## Commands / Steps

Record compile commands here, for example:

```bash
g++ -O3 -fopenmp file.cpp -o program.exe
```

Record run commands here.

## Results / Evidence

Add measured speedup here:

| Test size | Serial time | Parallel time | Speedup | Notes |
|---:|---:|---:|---:|---|
| 10 images | TBD | TBD | TBD | |
| 1000 images | TBD | TBD | TBD | |

## Open Questions

- Which loop has the best parallel efficiency?
- Does nested OpenMP cause oversubscription?
- Is visualization included in timing?
- Are random seeds controlled for fair comparison?
- Is memory bandwidth becoming the bottleneck?

## Related Pages

- [[ransac-ellipse-detection]]
- [[performance-results]]
- [[build-and-run-commands]]
- [[vck190-acceleration]]

## Sources

- Project conversation notes
