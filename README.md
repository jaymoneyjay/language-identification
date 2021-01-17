# Language Identification with ngrams
Language Identification provides a neural network, which identifies the language given a sentence. The model is trained on short sentences between 20 and 200 characters long. Longer texts are trivial to classify.

## Installation
Use the packet manager to install the following packets:
```bash
pip3 install torch, pandas, sklearn, numpy
```

## Usage
Start the jupyter notebook with

```bash
jupyter notebook
```

Select *Cells -> Run All* to run the code.

With the TRAINING flag set to false the model will be loaded from memory.
With the TRAINING flag set to true the model will be trained from scratch.

To test the model one can either:
* Use the method **predict_sentence(text, model)** to predict a single phrase.

```python
sample_string = "Hell is empty and all the devils are here."
predict_sentence(sample_string_eng, model)	# -> "eng"
```

* Generate a custom dataset from a csv file and use the method **test_dataset(dataset, model)** to test the accuracy of the model over the specified dataset.

```python
custom_dataset = CustomDataset("sample.csv", vocab)
test_data(data_set, model)
```

Examples are included in the code.

## Data
The data is expected to be a .csv file and be stored in the data directory. The format should follow ['index', 'lang', 'text'].

The file sample.csv provides some sample data to showcase this format.

The language identifiers are the following:

| Language   | Identifier |
|------------|------------|
| English    | eng        |
| German     | deu        |
| French     | fra        |
| Esperanto  | epo        |
| Kabyle     | kab        |
| Russian    | rus        |
| Turkish    | tur        |
| Portuguese | por        |
| Spanish    | spa        |
| Berber     | ber        |
| Hungarian  | hun        |
| Japanese   | jpn        |
| Hebrew     | heb        |
| Ukrainian  | ukr        |
| Italian	   | ita			|
| Dutch		| nld			|
| Finnish		| fin			|
| Polish		| pol			|
| Latin		| lat			|