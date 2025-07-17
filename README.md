# 🧠 Image Classification with Keras

This project demonstrates how to use a pre-trained Keras model to classify an input image. It loads a `.h5` model file and corresponding class labels, preprocesses an input image, and outputs the predicted class along with the confidence score.

---

## 📁 Project Structure

```
.
├── keras_model.h5       # Trained Keras model
├── labels.txt           # Class labels corresponding to model output
├── example.jpg          # Example image to classify
├── classify.py          # Python script for classification
└── README.md            # Project documentation
```

---

## 🚀 Getting Started

### 1. **Clone the repository**

```bash
git clone https://github.com/yourusername/keras-image-classifier.git
cd keras-image-classifier
```

### 2. **Install dependencies**

Make sure you have Python 3.7+ installed.

Install the required Python libraries:

```bash
pip install tensorflow pillow numpy
```

---

## 🖼️ How It Works

The script does the following:

1. Loads a pre-trained Keras model (`keras_model.h5`)
2. Reads class labels from `labels.txt`
3. Loads and preprocesses an image (`example.jpg`)
4. Predicts the class of the image
5. Outputs the predicted class and confidence score

---

## 🔧 Usage

Run the script with:

```bash
python classify.py
```

You should see output like:

```
Class: Cat
Confidence Score: 0.98234
```

To classify a different image, replace `example.jpg` with your desired image file.

---

## 📚 Example Code Snippet

```python
model = load_model("keras_model.h5", compile=False)
image = Image.open("example.jpg").convert("RGB")
image = ImageOps.fit(image, (224, 224), Image.Resampling.LANCZOS)
# preprocess and predict
```

---

## 📝 Notes

* Make sure the input image is RGB and properly sized (224x224).
* The model and labels must match (trained together).
* Labels in `labels.txt` should be in the correct order, one per line.

---

## 📄 License

This project is licensed under the MIT License.
