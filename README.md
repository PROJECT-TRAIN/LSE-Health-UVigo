


# LSE-Health-UVigo Dataset

The LSE-Health-UVigo dataset is a collection of 273 videos focused on health-related topics, presented in Spanish Sign Language (Lengua de Signos Española, LSE). The dataset offers comprehensive annotations and alignments for various linguistic elements within the videos.

[![Video Preview](https://github.com/PROJECT-TRAIN/LSE-Health-UVigo/blob/main/images/Sample_ELAN-LSE-Health-UVigo.png)](https://youtu.be/ND4YaDZEtx8)

## Overview

- **Total Videos**: 273
- **Total Duration**: 11 hours

A previous version of this dataset with less videos and annotations was distributed for the [2022 Sign Spotting Challenge at ECCV](https://chalearnlap.cvc.uab.cat/challenge/49/description/) The description of the former dataset, LSE_eSaude_UVIGO (ECCV'22) can be found [here](https://chalearnlap.cvc.uab.cat/dataset/42/description/) including the train/val/test splits for the two organized tracks (MSSL-multiple shot supervised learning, and OSLWL-one shot learning and weak labels). The results of the challenge with the description of the dataset, protocols and baseline models, as well as discussing top-winning solutions and future directions on the topic can be found in this [paper](https://dl.acm.org/doi/abs/10.1007/978-3-031-25085-9_13)

## Annotations

### 1. Video Translations to Spanish

- **Description**: Each video is translated into Spanish, segmented into sentences and smaller segments.
- **Total Segments**: 7,738

### 2. Sign Annotations

- **Description**: 105 distinct signs annotated across all 273 videos.
- **Total Instances**: 15,098

### 3. Fingerspelling Annotations

- **Description**: Accurate location and annotation of all fingerspelled words.
- **Total Instances**: 1,029

## Signers

- **Total Signers**: 10 (7 women, 3 men)
    - **Deaf Signers**: 7 (4 women, 3 men)
    - **Hearing Signers**: 3 (all women)
      
## Usage

Researchers and practitioners in machine translation, linguistics, healthcare, and sign language interpretation may find this dataset valuable for:
- Training machine learning models for sign language translation, sign spotting and Isolated sign language recognition
- Studying health-related sign language communication
- Analyzing linguistic patterns and structures within sign language

## Distribution

We provide two options for distribution:

### 1. Direct download of:

- **Excel file**: Includes the links to download the videos from youtube, meta information and all the annotations (segments, glosses and fingerspelled words)
- **Compressed file with the 273 annotation files using the ELAN program**: These files contein 3 Tiers explained below

### 2. Download the videos from here after signing and submitting an EULA form

## Detailed explanation of annotations


## License

The dataset is provided under license [CC BY-NC-SA](https://creativecommons.org/licenses/by-nc-sa/4.0/deed.en), that it is the same license assigned to the youtube videos by their owners. Please review the license for terms of use.

## Acknowledgments

This dataset is a collaborative effort of the next research goups and entities: 
- [Group of Multimedia Technologies (GTM)](http://gtm.uvigo.es/en/) from the [atlanTTic Research Center](https://atlanttic.uvigo.es/en) of [University of Vigo](http://www.uvigo.es) (Spain)
- [Group of Discourse and Society (GRADES)](http://grades.uvigo.gal) from the [School of Philology and Translation](https://fft.uvigo.es/en/) of [University of Vigo](http://www.uvigo.es) (Spain)
- [Federation of Deaf People Galician Associations (FAXPG)](http://www.faxpg.es)
- [Galician Health Service (SERGAS)](http://www.sergas.es)
Gratitude is extended to them for their contributions and support.

For more details and access to the dataset, kindly refer to [link_to_dataset_repository].
