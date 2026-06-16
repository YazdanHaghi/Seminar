# Build and Run Commands

## Summary

This page stores exact commands for building, running, timing, and testing the project.

## Linux / MSYS2 Timing

Use:

```bash
/usr/bin/time -v ./program_name.exe [arguments]
```

To save output to a log:

```bash
/usr/bin/time -v ./program_name.exe [arguments] 2>&1 | tee logs/run_name.log
```

## Folder Setup

Known setup command:

```bash
mkdir -p results logs vis_output_serial vis_output_parallel
rm -f results/*.csv logs/*.log logs/*.txt
```

## RANSAC Example

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

## Common Checks

```bash
wc -l results/output.csv
ls -lh results/
ls -lh logs/
```

## Open Questions

- What are the final compile commands for serial and OpenMP versions?
- Are different executable names used for serial, parallel, and RANSAC-only versions?
- Which input path is canonical: `./annotations.json` or `ellipse-detection-main/annotations.json`?
