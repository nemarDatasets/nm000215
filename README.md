[![DOI](https://img.shields.io/badge/DOI-10.82901%2Fnemar.nm000215-blue)](https://doi.org/10.82901/nemar.nm000215)

# P300 dataset BI2014b from a "Brain Invaders" experiment

P300 dataset BI2014b from a "Brain Invaders" experiment.

## Dataset Overview

- **Code**: BrainInvaders2014b
- **Paradigm**: p300
- **DOI**: https://doi.org/10.5281/zenodo.3267301
- **Subjects**: 38
- **Sessions per subject**: 1
- **Events**: Target=2, NonTarget=1
- **Trial interval**: [0, 1] s
- **File format**: mat and csv

## Acquisition

- **Sampling rate**: 512.0 Hz
- **Number of channels**: 32
- **Channel types**: eeg=32
- **Channel names**: Fp1, Fp2, AFz, F7, F3, F4, F8, FC5, FC1, FC2, FC6, T7, C3, Cz, C4, T8, CP5, CP1, CP2, CP6, P7, P3, Pz, P4, P8, PO7, O1, Oz, O2, PO8, PO9, PO10
- **Montage**: standard_1010
- **Hardware**: g.USBamp (g.tec, Schiedlberg, Austria)
- **Software**: OpenVibe
- **Reference**: right earlobe
- **Ground**: Fz
- **Sensor type**: wet electrodes
- **Line frequency**: 50.0 Hz
- **Cap manufacturer**: g.tec
- **Cap model**: g.GAMMAcap
- **Electrode type**: wet
- **Electrode material**: Ag/AgCl

## Participants

- **Number of subjects**: 38
- **Health status**: healthy
- **Age**: mean=24.1, std=3.09
- **Gender distribution**: male=24, female=14
- **BCI experience**: not naïve users - selected on the basis of their individual score during a preliminary session of Brain Invaders
- **Species**: human

## Experimental Protocol

- **Paradigm**: p300
- **Task type**: oddball
- **Number of classes**: 2
- **Class labels**: Target, NonTarget
- **Study design**: multi-user/hyperscanning experiment with three randomized conditions (Solo1, Solo2, Collaboration). Subjects played in pairs. Solo conditions used a control design where non-playing participant focused on unanimated cross to prevent stimulus observation while EEG was recorded (to correct for fake inter-brain synchrony).
- **Study domain**: inter-brain synchrony in collaborative BCI
- **Feedback type**: visual
- **Stimulus type**: visual flashes
- **Stimulus modalities**: visual
- **Primary modality**: visual
- **Synchronicity**: synchronous
- **Mode**: online
- **Training/test split**: False
- **Instructions**: destroy the target alien symbol as fast as possible. Up to eight attempts per level. If all attempts missed, level restarted.
- **Stimulus presentation**: repetition_structure=12 flashes per repetition of pseudo-random groups of 6 symbols, such that each symbol flashes exactly twice per repetition, target_ratio=1:5 (Target vs Non-Target), flash_groups=6 rows and 6 columns (pseudo-random groups, not physical arrangement), animation=aliens slowly and regularly moved according to predefined path with constant inter-distance

## HED Event Annotations

Schema: HED 8.4.0 | Browse: https://www.hedtags.org/hed-schema-browser

```
  Target
    ├─ Sensory-event
    ├─ Experimental-stimulus
    ├─ Visual-presentation
    └─ Target

  NonTarget
    ├─ Sensory-event
    ├─ Experimental-stimulus
    ├─ Visual-presentation
    └─ Non-target

```
## Paradigm-Specific Parameters

- **Detected paradigm**: p300
- **Number of targets**: 1

## Data Structure

- **Trials**: variable per session (9 levels, up to 8 attempts per level)
- **Blocks per session**: 9
- **Block duration**: variable, average ~33 seconds per level (5 minutes total for 9 levels) s
- **Trials context**: 9 levels per game session, each with unique predefined spatial configuration of 36 aliens. Up to 8 attempts to destroy target per level.

## Preprocessing

- **Data state**: raw EEG with no digital filter applied, synchronized experimental tags using USB analog-to-digital converter to reduce jitter
- **Preprocessing applied**: False
- **Notes**: Experimental tags produced by Brain Invaders 2 were synchronized with EEG signals using USB analog-to-digital converter connected to g.USBamp trigger channel. This tagging procedure allows consistent tagging latency and jitter.

## Signal Processing

- **Classifiers**: RMDM (Riemannian Minimum Distance to Mean), Riemannian
- **Feature extraction**: Covariance/Riemannian

## Cross-Validation

- **Evaluation type**: cross_session

## Performance (Original Study)

- **Classifier**: real-time adaptive RMDM classifier (calibration-free procedure)

## BCI Application

- **Applications**: gaming
- **Environment**: small room with 24' screen, subjects sitting side by side at ~125cm distance, experimenter in adjacent room with one-way glass window
- **Online feedback**: True

## Tags

- **Pathology**: Healthy
- **Modality**: Visual
- **Type**: Perception

## Documentation

- **Description**: EEG recordings of 38 subjects playing in pairs to the multi-user version of Brain Invaders P300-based BCI. Contains three conditions: Solo1, Solo2, and Collaboration.
- **DOI**: 10.5281/zenodo.3267301
- **Associated paper DOI**: hal-02173958
- **License**: CC-BY-4.0
- **Investigators**: Louis Korczowski, Ekaterina Ostaschenko, Anton Andreev, Grégoire Cattan, Pedro Luiz Coelho Rodrigues, Violette Gautheret, Marco Congedo
- **Senior author**: Marco Congedo
- **Institution**: GIPSA-lab, CNRS, University Grenoble-Alpes, Grenoble INP
- **Address**: GIPSA-lab, 11 rue des Mathématiques, Grenoble Campus BP46, F-38402, France
- **Country**: FR
- **Repository**: Zenodo
- **Data URL**: https://doi.org/10.5281/zenodo.3267301
- **Publication year**: 2019
- **Ethics approval**: Ethical Committee of the University of Grenoble Alpes (Comité d'Ethique pour la Recherche Non-Interventionnelle)
- **Acknowledgements**: At the end of the experiment two tickets of cinema were offered to each subject, for a total value of 15 euros per subject.
- **Keywords**: Electroencephalography (EEG), P300, Brain-Computer Interface (BCI), Experiment, Collaboration, Multi-User, Hyperscanning

## Abstract

We describe the experimental procedures for a dataset containing electroencephalographic (EEG) recordings of 38 subjects playing in pairs to the multi-user version of a visual P300-based Brain-Computer Interface (BCI) named Brain Invaders. The interface uses the oddball paradigm on a grid of 36 symbols (1 Target, 35 Non-Target) that are flashed pseudo-randomly to elicit a P300 response. EEG data were recorded using 32 active wet electrodes per subject (total: 64 electrodes) during three randomised conditions (Solo1, Solo2, Collaboration). The experiment took place at GIPSA-lab, Grenoble, France, in 2014.

## Methodology

Multi-user hyperscanning P300 BCI experiment designed to study inter-brain synchrony. Participants played Brain Invaders 2 in three conditions: Solo1 (player1 plays, player2 watches cross), Solo2 (roles reversed), and Collaboration (4 game sessions with both players). Each game session consisted of 9 levels with predefined alien configurations. A repetition used 12 flashes of pseudo-random groups of 6 symbols, ensuring each symbol flashed twice per repetition (1:5 Target:Non-Target ratio). Real-time adaptive RMDM classifier provided online feedback. Control condition (non-playing participant) allowed correction for fake inter-brain synchrony.

## References

Korczowski, L., Ostaschenko, E., Andreev, A., Cattan, G., Rodrigues, P. L. C., Gautheret, V., & Congedo, M. (2019). Brain Invaders Solo versus Collaboration: Multi-User P300-Based Brain-Computer Interface Dataset (BI2014b). https://hal.archives-ouvertes.fr/hal-02173958
Appelhoff, S., Sanderson, M., Brooks, T., Vliet, M., Quentin, R., Holdgraf, C., Chaumon, M., Mikulan, E., Tavabi, K., Hochenberger, R., Welke, D., Brunner, C., Rockhill, A., Larson, E., Gramfort, A. and Jas, M. (2019). MNE-BIDS: Organizing electrophysiological data into the BIDS format and facilitating their analysis. Journal of Open Source Software 4: (1896). https://doi.org/10.21105/joss.01896

Pernet, C. R., Appelhoff, S., Gorgolewski, K. J., Flandin, G., Phillips, C., Delorme, A., Oostenveld, R. (2019). EEG-BIDS, an extension to the brain imaging data structure for electroencephalography. Scientific Data, 6, 103. https://doi.org/10.1038/s41597-019-0104-8

---
Generated by MOABB 1.5.0 (Mother of All BCI Benchmarks)
https://github.com/NeuroTechX/moabb
