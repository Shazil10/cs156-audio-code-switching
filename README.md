# CS156 Audio Code-Switching Final Project

This repository contains my CS156 final machine learning project on vocal code-switching across three social contexts: `Mom`, `Bestfriend`, and `Professional`.

The main report is:

- `Pipeline_3rd_draft.ipynb`
- `Pipeline_3rd_draft.html`

The project has two parts:

1. A classification pipeline that tests whether my voice alone is enough for a model to identify which social context a clip belongs to.
2. A generation pipeline that tries to produce short voice-like audio windows from the same archive using a conditional beta-VAE and a latent LSTM prior.

## Main Result

The strongest baseline classifier is the augmented CNN:

- Test accuracy: `90.3%`
- Macro F1: `0.901`

The generation section runs end to end and saves reconstructions plus free generations. The result is interesting but still limited: when I classify the generated clips with the strongest inherited CNN, all 15 generated samples are predicted as `Mom`, so generated-context accuracy stays at `33.3%`, which is the random baseline for a 3-class problem.

## Audio Gallery

The professor-facing audio files live in `assignment3_assets/audio/`.

Use this GitHub folder page to browse the audio files:

- `https://github.com/Shazil10/cs156-audio-code-switching/tree/main/assignment3_assets/audio`

Use raw links only for individual files. For example:

- `https://raw.githubusercontent.com/Shazil10/cs156-audio-code-switching/main/assignment3_assets/audio/original_clip_mom.wav`

I also added a small audio index page here:

- `assignment3_assets/audio/README.md`

Important files:

- `original_clip_mom.wav`
- `original_clip_bestfriend.wav`
- `original_clip_professional.wav`
- `real_window_mom.wav`
- `real_window_bestfriend.wav`
- `real_window_professional.wav`
- `reconstruction_mom.wav`
- `reconstruction_bestfriend.wav`
- `reconstruction_professional.wav`
- `generated_mom_00.wav` through `generated_mom_04.wav`
- `generated_bestfriend_00.wav` through `generated_bestfriend_04.wav`
- `generated_professional_00.wav` through `generated_professional_04.wav`

The manifest file is:

- `assignment3_assets/audio/audio_manifest.csv`

## Repository Notes

I intentionally do not include the entire raw and derived working dataset in this repository. The large local folders such as `clips/`, `wav_files/`, and the exported WhatsApp source folders are excluded. Instead, I include the report, the final generated assets, the selected original example clips, and the audio manifest so the results are easy to inspect.
