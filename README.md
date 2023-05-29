# music-generation-RNN-LSTM
Music Generation RNN-LSTM
Introduction

The Music Generation RNN-LSTM project is a Python-based application that generates new music using recurrent neural networks (RNNs) and long short-term memory (LSTM) models. It uses TensorFlow, a popular open-source machine learning framework, to train the models.

The project's primary goal is to create a model that can learn from a large dataset of MIDI files and generate new, original music in a similar style. The MIDI files are preprocessed to extract the necessary features, including note duration, velocity, and pitch, and transformed into sequences of notes and chords.
Installation

To install the project, clone the repository and install the required dependencies using pip:
pip install music21
# Usage

The script provides several options for configuring the model and training it on different datasets. Users can adjust the number of LSTM layers, the number of nodes in each layer, the batch size, and the number of epochs during training.

Once the model is trained, the generate.py script can be used to generate new music

The script generates a new piece of music in MIDI format, with the specified length and complexity. The output can be listened to using any MIDI player.

# Conclusion

The Music Generation RNN-LSTM project is an innovative application of machine learning techniques to the field of music generation. It provides a great opportunity for developers and music enthusiasts to explore the potential of RNNs and LSTMs in generating new and original music. With its user-friendly interface and flexible configuration options, the project is a valuable tool for anyone interested in creating new music using machine learning techniques.
