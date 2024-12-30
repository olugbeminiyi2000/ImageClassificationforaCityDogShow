# Citywide Dog Show Image Classification

![license](https://img.shields.io/badge/license-MIT-blue.svg)
![Status](https://img.shields.io/badge/status-active-green)
![Python](https://img.shields.io/badge/python-3.8%2B-blue)
![Deep Learning](https://img.shields.io/badge/deep_learning-CNN%20%28ResNet%2C%20AlexNet%2C%20VGG%29-ff69b4)

## Project Overview

In this project, I worked on a **Citywide Dog Show Image Classification** system using Python. The system utilizes pre-trained Convolutional Neural Networks (CNNs) such as **ResNet**, **AlexNet**, and **VGG** to classify images of dogs and determine their breeds. The goal of this project is to ensure that the images submitted by participants are indeed dogs, and if so, to identify their breeds.

### Project Features

- Classify images as **dogs** or **not dogs**.
- Identify the breed of dog in each image.
- Time the execution of different CNN models to compare **accuracy** vs **runtime**.
- Use **command-line arguments** to control input files and classifier choices.

### Key Tasks

- Implement the classification system using pre-trained CNN models: **ResNet**, **AlexNet**, **VGG**.
- Use the `argparse` library to handle user input via command-line arguments.
- Time the classification process and compare performance of the different models.
- Compare the results of the classifiers with the actual labels of the images.
- Present the results and identify the most accurate and efficient model.

## Installation

To run the project, you will need to have Python (version 3.8 or later) and the required libraries installed.

### Prerequisites

- Python 3.8 or higher

## Usage

1. Clone the repository:

```bash
git clone 
```

2. Run the `check_images.py` script with the following command line arguments:

```bash
python check_images.py --dir pet_images/ --arch vgg --dogfile dognames.txt
```

### Arguments:

- `--dir` : Path to the folder containing pet images. (Default: `pet_images/`)
- `--arch` : CNN architecture to use for classification. (Choices: `vgg`, `alexnet`, `resnet`; Default: `vgg`)
- `--dogfile` : Path to the file containing valid dog names. (Default: `dognames.txt`)

3. The script will process the images, classify them as "dogs" or "not dogs", and identify the breed if applicable. It will also provide the **execution time** and **accuracy** results.

## Code Overview

### Main Files

- `check_images.py`: Main script to run the image classification tasks.
- `classifier.py`: Contains the pre-trained classifier function to use CNN models for image classification.
- `get_input_args.py`: Handles parsing of command-line arguments using `argparse`.
- `print_functions_for_lab_checks.py`: Contains helper functions to check the results and ensure correctness.

### Functionality

1. **`get_input_args()`**: Retrieves command-line arguments for directory, CNN model, and dog names file.
2. **`get_pet_labels()`**: Creates a dictionary of pet image labels.
3. **`classifier()`**: Classifies the images using the specified CNN model.
4. **`compare_labels()`**: Compares the classifier results with the actual pet labels.
5. **`print_results()`**: Displays the classification results and compares them with the correct labels.

## Project Workflow

1. **Image Classification**: Classify images as "dogs" or "not dogs" using the CNN models.
2. **Breed Identification**: If the image is classified as a dog, identify the breed.
3. **Runtime Measurement**: Time how long each CNN model takes to classify the images.
4. **Results Comparison**: Compare classifier output with actual labels and print results.

## Example Output

The program will output the following after execution:

```bash
Directory: pet_images/
Model: vgg
Dogfile: dognames.txt
Classification Result: 85% accuracy for identifying dog breeds.
Execution Time: 120 seconds
```

## Contributing

Feel free to fork this repository, submit pull requests, or create issues. Contributions are welcome!

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
