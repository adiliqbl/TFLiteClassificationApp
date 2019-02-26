# Tensorflow Lite Classification App
[Original repo](https://github.com/tensorflow/tensorflow/tree/master/tensorflow/lite/examples/android)

## Implementation Details
This project is a little modified version of TFLite [andorid example](https://github.com/tensorflow/tensorflow/tree/master/tensorflow/lite/examples/android).

### Classifier
Custom classifer can be implemented by `Classier` abstract class and implementing `recognizeImage(Bitmap bitmap)`. Classifier needs to put labels file in `Classifier.labels`. Model (Interpretor) can be set using: 

```Classifier.tflite = new Interpreter(loadModelFile(assetManager, modelFilename));```

*Results*

`Classifier.Result` class is used to get results from model. For showing bounding boxes, model should return bounding location of object detected.

## Links
- [Tensorflow Lite Github](https://github.com/tensorflow/tensorflow/tree/master/tensorflow/lite)
- [More TFLite examples](https://github.com/tensorflow/tensorflow/tree/master/tensorflow/lite/examples)

## Requirements
### Running the app
- Place model with `.tflite` file and labels file `label.txt` in 'app/src/assets' folder.
- Reference the model file in `ClassifierActivity` or `DetectorActivity` depending on type of model.
- Build app

### Runtime
Android API > 21
