# Counting the Crowds

This notebook demonstrates several approaches to automatic counting of people using images from indoor video cameras in a shopping center.

Out-of-the-box solution: EfficientDet object detection model loaded from TensorFlow Hub. The model is capable of detecting a wide range of objects returning predicted class, bounding box coordinates and confidence score for each object. Benefits: doesn't require training, multiple models are available, could be easily deployed on various devices. Drawbacks: model is prone to errors when detecting multiple objects, objects partly accluded or located at the background, model is difficult to retrain and fine-tune.
Transfer learning: InceptionResNetV2 as feature extractor with a new regression head. Benefits: model is relatively easy to fine-tune for a new task while retaining the useful knowledge of the original classifier. Drawbacks: despite higher accuracy compared to the previous solution, this model is not perfect and could not be used in environments where high precision is important.
