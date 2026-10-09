# Dataset metadata: PlantVillage (primary training data)

## Source
- Hugging Face: mohanty/PlantVillage (files used: data.zip, splits/color_train.txt, splits/color_test.txt)
- Original project: https://github.com/spMohanty/PlantVillage-Dataset
- Paper: Mohanty, Hughes and Salathe (2016), "Using deep learning for image-based plant disease detection", Frontiers in Plant Science, 7:1419
- Access date: 10 October 2026

## License
- CC BY-SA 3.0, as stated on the Hugging Face dataset card. To be re-checked against the original source before any redistribution.

## What was loaded
- The `color` configuration named in the roadmap does not exist in the current repo (error: BuilderConfig 'color' not found; only 'default' exists).
- `default` contains only text lists of file paths, not images.
- Images were therefore read from data.zip, using the official color train/test lists.

## Verified counts (my own runs)
- Train list: 43,596 images
- Test list: 10,709 images
- Total: 54,305 (the dataset card says 54,306; the 1-image difference is unexplained)
- Classes (from folder names): 38
- Listed paths missing from the zip: 0
- File paths appearing in both train and test: 0
- Smallest class: ___ 
- Largest class: ___

## Limitations
- Classes are strongly imbalanced, so accuracy alone is misleading; report macro F1 and per-class recall.
- A file-level overlap of 0 does not prove that images of the same physical leaf are kept apart; to be checked in Week 4 using leaf_grouping/leaf-map.json.
- Images come from one collection setting; performance here must not be presented as field reliability (see PlantDoc external evaluation).
- The dataset card and the repo contents disagree (card describes color/grayscale/segmented configs with image and label columns; repo has only text lists).
