# Assignment 3 Audio Gallery

This folder contains the listening examples for `Pipeline_3rd_draft.ipynb`.

Browse the folder on GitHub:

- https://github.com/Shazil10/cs156-audio-code-switching/tree/main/assignment3_assets/audio

Manifest:

- [audio_manifest.csv](https://raw.githubusercontent.com/Shazil10/cs156-audio-code-switching/main/assignment3_assets/audio/audio_manifest.csv)

If a raw link gives a 404, it means that exact WAV file has not been pushed to GitHub yet. The links below are the files used by the final executed Assignment 3 section.

## Start Here: Three-Way Comparison

Each class has three generated examples:

1. **beta-VAE + LSTM**: actual neural generation attempt; blurry/smeared.
2. **Autoencoder + Transformer**: improved neural attempt; still blurry, but a smarter architecture.
3. **Unit selection**: non-neural baseline; jumpy, but clearer and more voice-like because it stitches real snippets.

### Mom

- [beta-VAE + LSTM generated Mom](https://raw.githubusercontent.com/Shazil10/cs156-audio-code-switching/main/assignment3_assets/audio/generated_mom_00.wav)
- [Autoencoder + Transformer generated Mom](https://raw.githubusercontent.com/Shazil10/cs156-audio-code-switching/main/assignment3_assets/audio/ae_transformer_generated_mom.wav)
- [Unit-selection generated Mom](https://raw.githubusercontent.com/Shazil10/cs156-audio-code-switching/main/assignment3_assets/audio/unit_generated_mom_00.wav)

### Bestfriend

- [beta-VAE + LSTM generated Bestfriend](https://raw.githubusercontent.com/Shazil10/cs156-audio-code-switching/main/assignment3_assets/audio/generated_bestfriend_00.wav)
- [Autoencoder + Transformer generated Bestfriend](https://raw.githubusercontent.com/Shazil10/cs156-audio-code-switching/main/assignment3_assets/audio/ae_transformer_generated_bestfriend.wav)
- [Unit-selection generated Bestfriend](https://raw.githubusercontent.com/Shazil10/cs156-audio-code-switching/main/assignment3_assets/audio/unit_generated_bestfriend_00.wav)

### Professional

- [beta-VAE + LSTM generated Professional](https://raw.githubusercontent.com/Shazil10/cs156-audio-code-switching/main/assignment3_assets/audio/generated_professional_00.wav)
- [Autoencoder + Transformer generated Professional](https://raw.githubusercontent.com/Shazil10/cs156-audio-code-switching/main/assignment3_assets/audio/ae_transformer_generated_professional.wav)
- [Unit-selection generated Professional](https://raw.githubusercontent.com/Shazil10/cs156-audio-code-switching/main/assignment3_assets/audio/unit_generated_professional_00.wav)

## Reference Clips

Original 10-second examples used earlier in the notebook:

- [Mom original clip](https://raw.githubusercontent.com/Shazil10/cs156-audio-code-switching/main/assignment3_assets/audio/original_clip_mom.wav)
- [Bestfriend original clip](https://raw.githubusercontent.com/Shazil10/cs156-audio-code-switching/main/assignment3_assets/audio/original_clip_bestfriend.wav)
- [Professional original clip](https://raw.githubusercontent.com/Shazil10/cs156-audio-code-switching/main/assignment3_assets/audio/original_clip_professional.wav)

Held-out 2-second real windows used for reconstruction comparison:

- [Mom real window](https://raw.githubusercontent.com/Shazil10/cs156-audio-code-switching/main/assignment3_assets/audio/real_window_mom.wav)
- [Bestfriend real window](https://raw.githubusercontent.com/Shazil10/cs156-audio-code-switching/main/assignment3_assets/audio/real_window_bestfriend.wav)
- [Professional real window](https://raw.githubusercontent.com/Shazil10/cs156-audio-code-switching/main/assignment3_assets/audio/real_window_professional.wav)

beta-VAE reconstructions of those held-out windows:

- [Mom reconstruction](https://raw.githubusercontent.com/Shazil10/cs156-audio-code-switching/main/assignment3_assets/audio/reconstruction_mom.wav)
- [Bestfriend reconstruction](https://raw.githubusercontent.com/Shazil10/cs156-audio-code-switching/main/assignment3_assets/audio/reconstruction_bestfriend.wav)
- [Professional reconstruction](https://raw.githubusercontent.com/Shazil10/cs156-audio-code-switching/main/assignment3_assets/audio/reconstruction_professional.wav)

## Interpretation

The neural clips are important because they are the actual learned-generation attempts. They produce speech-like energy, but they sound blurry because the models generate log-mel spectrograms and then use Griffin-Lim to reconstruct waveform phase. Fine harmonic detail gets smoothed away.

The unit-selection clips are clearer because they reuse real waveform snippets from the training archive. They sound more like me, but they can jump at boundaries because the method is stitching recorded units together rather than generating a smooth waveform from scratch.
