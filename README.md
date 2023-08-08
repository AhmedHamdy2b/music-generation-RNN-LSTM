
Music Generation RNN-LSTM
## Introduction

The Music Generation RNN-LSTM project is a Python-based application that generates new music using recurrent neural networks (RNNs) and long short-term memory (LSTM) models. It uses TensorFlow, a popular open-source machine learning framework, to train the models.

The project's primary goal is to create a model that can learn from a large dataset of MIDI files and generate new, original music in a similar style. The MIDI files are preprocessed to extract the necessary features, including note duration, velocity, and pitch, and transformed into sequences of notes and chords.
## Installation

To run the code, please follow these steps:

1. Install the required dependencies by running the following command:
pip install music21
2. Unzip the `xmusic.zip` file.

## Usage

1. Import the necessary dependencies:

- glob
- pickle
- numpy
- music21 (converter, instrument, note, chord, stream)
- keras (Sequential, Dense, Dropout, LSTM, Activation, np_utils, ModelCheckpoint)

2. Load the MIDI file and extract the notes:

- Specify the MIDI file path in the `file` variable.
- Use the music21 library to parse the MIDI file and extract the notes.
- Print the first 10 notes with their offsets.

3. Parse multiple MIDI files and create a list of notes:

- Use the `glob` module to iterate over all MIDI files in the `xmusic` directory.
- Parse each MIDI file and extract the notes.
- Store the notes in a list.

4. Preprocess the notes for training:

- Count the number of unique pitches in the notes to determine the vocabulary size.
- Specify the sequence length for input/output pairs.
- Create a dictionary to map pitches to integers.
- Create input sequences and corresponding output labels by sliding a window over the notes.
- Reshape the input sequences and normalize the values.
- Convert the output labels to categorical format.

5. Create the RNN-LSTM model:

- Define the model architecture with three LSTM layers, dropout layers, and dense layers.
- Compile the model with the categorical cross-entropy loss and RMSprop optimizer.

6. Train the model:

- Specify the path for saving model checkpoints.
- Use the ModelCheckpoint callback to save the best model based on the loss.
- Fit the model to the training data.

7. Generate new music:

- Load the trained weights from a file if available.
- Choose a random sequence from the input as the starting point for prediction.
- Generate a sequence of notes by predicting the next note using the trained model.
- Convert the predicted notes to music21 note and chord objects.
- Write the generated notes to a MIDI file named "test.mid".

## Additional Information

- You can experiment with different model architectures by modifying the `create_network` function.
- To use previously trained weights, specify the file path in the `weights` variable.
- The generated music consists of 500 notes. You can adjust this by modifying the loop condition in the generation process.
- Feel free to explore and customize the code further to suit your needs.

The Music Generation RNN-LSTM project is an innovative application of machine learning techniques to the field of music generation. It provides a great opportunity for developers and music enthusiasts to explore the potential of RNNs and LSTMs in generating new and original music. With its user-friendly interface and flexible configuration options, the project is a valuable tool for anyone interested in creating new music using machine learning techniques.
