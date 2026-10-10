# PlantDoc inspection (external evaluation data)

## Source
- Repository: https://github.com/pratikkayal/PlantDoc-Dataset (Cropped-PlantDoc, classification version)
- Commit used: 5467f6012d78d1c446145d5f582da6096f852ae8
- Access date: 10 October 2026
- Paper: Singh et al. (2020), "PlantDoc: A Dataset for Visual Plant Disease Detection", CoDS-COMAD 2020
- License: CC BY 4.0 (LICENSE.txt in the repository)

## What was downloaded (my own run)
- Train: 28 class folders, 2,342 images
- Test: 27 class folders, 236 images
- Total: 2,578 images. The paper's abstract reports 2,598, a difference of 20 that I have not explained.
- Unreadable images: 0; color modes: {'RGB': 2567, 'L': 1, 'CMYK': 5, 'RGBA': 5}
- Width min/median/max: 115 / 800 / 6000; height min/median/max: 69 / 667 / 6000

## Images per class
| PlantDoc class folder | train | test |
|---|---|---|
| Apple Scab Leaf | 83 | 10 |
| Apple leaf | 82 | 9 |
| Apple rust leaf | 79 | 10 |
| Bell_pepper leaf | 53 | 8 |
| Bell_pepper leaf spot | 62 | 9 |
| Blueberry leaf | 106 | 11 |
| Cherry leaf | 47 | 10 |
| Corn Gray leaf spot | 64 | 4 |
| Corn leaf blight | 180 | 12 |
| Corn rust leaf | 106 | 10 |
| Peach leaf | 103 | 9 |
| Potato leaf early blight | 109 | 8 |
| Potato leaf late blight | 97 | 8 |
| Raspberry leaf | 112 | 7 |
| Soyabean leaf | 57 | 8 |
| Squash Powdery mildew leaf | 124 | 6 |
| Strawberry leaf | 88 | 8 |
| Tomato Early blight leaf | 79 | 9 |
| Tomato Septoria leaf spot | 140 | 11 |
| Tomato leaf | 55 | 8 |
| Tomato leaf bacterial spot | 101 | 9 |
| Tomato leaf late blight | 101 | 10 |
| Tomato leaf mosaic virus | 44 | 10 |
| Tomato leaf yellow virus | 70 | 6 |
| Tomato mold leaf | 85 | 6 |
| Tomato two spotted spider mites leaf | 2 | 0 |
| grape leaf | 57 | 12 |
| grape leaf black rot | 56 | 8 |

## Observations
- Class folder names are descriptive phrases and do not match PlantVillage class names; no folder is explicitly called "healthy".
- The test set is very small (4 to 12 images per class), so any per-class external score is coarse. Every reported score must state its image count.
- `Tomato two spotted spider mites leaf` has 2 train images and no test images, so it cannot be scored on the PlantDoc test split.
- Images are scraped from the internet (per the paper), so duplicates within PlantDoc, or overlap with PlantVillage images, are possible. Neither has been checked yet.

## Status
- No label mapping to PlantVillage has been made yet. Each mapping will be decided in Week 11 with a written rationale, after viewing images.
- PlantDoc has not been used for training, tuning or model selection.

