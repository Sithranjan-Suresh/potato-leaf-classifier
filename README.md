# Potato Leaf Health Classifier

**End-to-end deep learning system to classify potato leaf health using CNNs, with web and mobile integration.**

---

## Project Overview

This project allows farmers to take a photo of a potato leaf and automatically detect whether the plant is:

* Healthy
* Early Blight
* Late Blight

The system covers the full pipeline:

1. Collecting and augmenting leaf images.
2. Training a CNN model in TensorFlow.
3. Serving the model via TensorFlow Serving and FastAPI.
4. Building a React web UI.
5. Converting the model to TensorFlow Lite with quantization.
6. Integrating it into a React Native mobile app deployed on Google Cloud Platform.

---


## Day 1: Data Preparation and Input Pipeline

**Key steps completed:**

1. **Data Collection:**

   * Evaluated three options: buy ready-made data, manually annotate, or web scrape.
   * Chose the PlantVillage Kaggle dataset.
   * Filtered to include only three classes: healthy, early blight, late blight.

2. **Project Setup:**

   * Organized project folders.
   * Launched Jupyter notebook `day1_data_preparation.ipynb`.

3. **Data Loading:**

   * Loaded images into `tf.data.Dataset` using `image_dataset_from_directory`.
   * Set shuffling, image size, and batch size 32.

4. **Data Exploration:**

   * Checked class names, image shapes, and labels.
   * Visualized sample images in a grid with class titles.

5. **Train/Validation/Test Split:**

   * Implemented an 80/10/10 split.
   * Wrapped into a reusable function with optional shuffling.

6. **Pipeline Optimization:**

   * Used `cache()`, `shuffle()`, and `prefetch()` for faster training.
   * Created preprocessing layers for resizing, rescaling, and augmentation (random flip & rotation).

---

## Next Steps

* Train initial CNN model.
* Evaluate performance on validation and test sets.
* Experiment with different augmentation and preprocessing strategies.

---

## Requirements

```
TensorFlow >= 2.12
numpy
matplotlib
pandas
scikit-learn
```

*(Full requirements will be updated as the project progresses.)*

---

## License

MIT License
