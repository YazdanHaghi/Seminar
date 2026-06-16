# RANSAC Ellipse Detection

## Summary

This page tracks the RANSAC-based ellipse detection project, including batch execution, visual output generation, CSV result files, and comparison between serial and parallel versions.

## Current Status

Known command pattern:

```bash
/usr/bin/time -v ./ransac_only.exe \
  --ann ./annotations.json \
  --ellipses_dir ./Ellipses \
  --mode first \
  --n 10 \
  --vis_dir vis_output_ransac \
  --save_vis_n 10 \
  --out_csv results/ransac_results_10.csv \
  2>&1 | tee logs/ransac_10.log
```

Observed settings from project notes:

- Method: RANSAC ellipse fitting + peeling
- OpenMP enabled in at least one run
- Parallel mode: combined image loop + inlier counting
- `boundary_tol=0.5`
- `max_ellipses=3`

## Key Details

The project processes annotation data and ellipse image files, then writes per-image results to CSV and optional visual comparison images.

## Commands / Steps

Add commands here whenever a new run is performed.

## Results / Evidence

Add runtime, memory, CSV row count, image count, and quality metrics here.

## Open Questions

- What is the exact serial baseline runtime for 10, 1000, and all images?
- What is the exact parallel runtime for the same inputs?
- Are the serial and parallel outputs numerically identical or only visually similar?
- Which phase dominates runtime: initialization, RANSAC sampling, inlier counting, fitting, or visualization?

## Related Pages

- [[openmp-parallelization]]
- [[performance-results]]
- [[build-and-run-commands]]
- [[vck190-acceleration]]

## Sources

- Project conversation notes
