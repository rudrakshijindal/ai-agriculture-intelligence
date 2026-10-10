# Data audit: PlantVillage (color)

Run date: 10 October 2026. Seed: 42. All numbers below come from my own runs.

## Integrity checks
- Listed image paths missing from data.zip: 0
- Corrupt or unreadable images: 0
- Image size: 54,305 of 54,305 images are 256x256
- Color modes: {'RGB': 54304, 'RGBA': 1}. The single RGBA image must be converted with .convert("RGB") when loading.
- Exact-duplicate groups (identical file content): 21 (42 images)
- Exact-duplicate groups present in both official train and test: 5
- Duplicate groups with conflicting class names: 0
- Near-duplicates (e.g. rotated copies) were NOT checked.

## Leaf grouping (leaf_grouping/leaf-map.json)
- Images with a leaf group from the map: 40,490
- Images matched after allowing a class-name difference (Apple___Black_rot is called Apple_Frogeye Spot in the map): 621
- Images with NO leaf information (their file-name families are absent from the map): 13,194
- Distinct leaf groups found: 7,595
- Leaf groups present in both official train and test: 2 (20 images, both Cherry_(including_sour)___healthy)
- Limitation: for the images with no leaf information, leakage between train and test cannot be checked.

## Split policy
- Test set: the official color_test.txt list, unchanged and never used for tuning: 10,709 images.
- Train exclusions (from the official train list): {'kept': 43567, 'duplicate_within_train': 14, 'leaf_in_test': 10, 'exact_duplicate_of_test': 5}
- Validation: about 10% of the remaining train images, split by leaf group (images without leaf info count as their own group), stratified by class, seed 42.
- Fix applied: Raspberry___healthy got no validation images in the first split, so 3 whole leaf groups (39 images) were moved to validation.
- Final sizes: train 39,236 | val 4,331 | test 10,709 | excluded 29 | total 54,305
- Raspberry___healthy: train 170, val 39, test 162

## Safety checks after splitting (all must be 0)
- Leaf groups in both train and val: 0
- Identical files in both train and val: 0
- Identical files in both train and test: 0
- Identical files in both val and test: 0
- Classes with no validation images: 0
- Classes with no train images: 0

## Known limitations
- Classes are strongly imbalanced (smallest: Potato___healthy, 152 images in total; largest: Orange___Haunglongbing_(Citrus_greening), 5,507).
- Smallest validation class: Potato___healthy with 16 images, so its validation metrics will be noisy.
- Validation is only as leak-free as the leaf map allows (see above).
