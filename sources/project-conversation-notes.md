# Source Summary: Project Conversation Notes

## Source

Project conversation history from Yazdan's ChatGPT project.

## Main Topics Extracted

- RANSAC ellipse detection project
- OpenMP parallelization and combined parallel mode
- Timing and memory measurement with `/usr/bin/time -v`
- CSV/log/visualization output management
- Possible VCK190 acceleration
- KiCad PCB design for table football feedback system
- LCD component: EA DOGL128L-6, 128x64 reflective LCD
- Job application/CV/cover-letter work
- German B1.1 grammar notes

## Important Commands

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

## Open Questions

- Exact current source code files are not included in this starter wiki.
- Exact benchmark values need to be filled from logs.
- Exact PCB pin mappings need to be filled from schematic/datasheet.
