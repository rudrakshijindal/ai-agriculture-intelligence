# Glossary

| Term | Meaning in simple words |
|---|---|
| Pixel | One tiny dot of an image. |
| RGB | The three numbers per pixel: Red, Green, Blue (0 to 255, or 0 to 1 as a tensor). |
| Tensor | PyTorch's version of a NumPy array: a grid of numbers. |
| Label | The correct answer for an image, for example "Tomato_healthy". |
| Class | One possible label the model can choose. |
| Logits | The model's raw scores for each class, before they are turned into percentages. |
| Probability | A score from 0 to 1 for each class; all of them add up to 1. |
| Loss | A number saying how wrong the model is. Training tries to make it smaller. |
| Training set | Images the model learns from. |
| Validation set | Images used to check progress and choose settings while building. |
| Test set | Images kept untouched until the end, for the final honest score. |
| Overfitting | When the model memorises the training images and does badly on new ones. |
| Data leakage | When information from the test data sneaks into training, making scores look better than they really are. |
