# Neural Melody

Teach a small neural network to compose melodies.

This repository contains a beginner-friendly Jupyter notebook that trains an LSTM to predict the next note in a melody, then generates new melodies as playable audio. It runs on CPU and includes a built-in pentatonic corpus, so no dataset download is required.

## Contents

- [`music_generation_lstm.ipynb`](music_generation_lstm.ipynb) — end-to-end data preparation, training, generation, and audio playback.
- `Build and Train a Small Neural Network Music Generation.pptx` — presentation accompanying the project.

## Run the notebook

1. Open `music_generation_lstm.ipynb` in [Google Colab](https://colab.research.google.com/) or Jupyter.
2. Run the cells from top to bottom. The notebook installs `pretty_midi` and uses PyTorch, NumPy, and Matplotlib.
3. Listen to the generated melody in the final cells.

The default configuration trains on a generated corpus of short pentatonic phrases. Training takes a few minutes on a CPU.

## Use your own MIDI files

Set `MIDI_DIR` in the notebook to a folder containing `.mid` or `.midi` files:

```python
MIDI_DIR = "my_midi/"
```

The notebook extracts pitches from non-drum instruments and uses them as the training sequences. Only use music you own or have permission to use, and credit artists whose work inspires your experiments.

## Experiment

- Adjust `temperature` when generating: lower values are safer and more repetitive; higher values are more adventurous.
- Change `EPOCHS`, sequence length, or hidden size and compare training and validation loss.
- Extend the model to predict note duration or replace the LSTM with a small Transformer.

## License

No license is currently specified for this repository. Add one before distributing or reusing the code.
