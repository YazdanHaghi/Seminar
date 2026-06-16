# Performance Results

## Summary

This page tracks runtime, memory usage, speedup, and correctness results for serial and parallel versions.

## Measurement Requirements

Known memory-measurement command pattern:

```bash
/usr/bin/time -v ./dght_cpp.exe \
  --ann ellipse-detection-main/annotations.json \
  --ellipses_dir Ellipses \
  --mode first \
  --n 1000 \
  --vis_dir vis_output \
  --save_vis_n 1000 \
  --out_csv batch_results_all_1000.csv
```

Important fields from `/usr/bin/time -v`:

- Elapsed wall-clock time
- User time
- System time
- Percent CPU
- Maximum resident set size
- Exit status

## Results Table

| Date | Version | Input size | Threads | Wall time | Max RSS | Output CSV | Notes |
|---|---|---:|---:|---:|---:|---|---|
| TBD | Serial | 1000 | 1 | TBD | TBD | TBD | |
| TBD | OpenMP | 1000 | TBD | TBD | TBD | TBD | |

## Correctness Checks

Track these checks for every run:

- Number of rows in CSV
- Number of processed images
- Number of skipped images
- Whether visual outputs were generated
- Whether serial and parallel results match

## Open Questions

- Why did one CSV contain only 10 rows when a larger run was expected?
- Was `--n` set correctly?
- Was the correct output file opened?
- Did the program stop early or overwrite an old CSV?

## Related Pages

- [[build-and-run-commands]]
- [[ransac-ellipse-detection]]
- [[openmp-parallelization]]
