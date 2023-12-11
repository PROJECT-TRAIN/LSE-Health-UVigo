# LSE-Health-UVigo Dataset

The LSE-Health-UVigo dataset is a collection of 273 videos focused on health-related topics, presented in Spanish Sign Language (Lengua de Signos Española, LSE). The dataset offers comprehensive annotations and alignments for various linguistic elements within the videos.

[![Video Preview](https://github.com/PROJECT-TRAIN/LSE-Health-UVigo/blob/main/images/Sample_ELAN-LSE-Health-UVigo.png)](https://youtu.be/ND4YaDZEtx8)

## Overview

- **Total Videos**: 273
- **Total Duration**: ~11 hours

The dataset is acquired in studio conditions with blue chroma-key, no shadow effects and uniform illumination, at 25 fps and FHD. The added value of the dataset is he rich and rigorous hand-made annotations. Experts interpreters and deaf people were in charge of annotating the dataset with strict criteria explained below.
A previous version of this dataset with less videos and annotations was distributed for the [2022 Sign Spotting Challenge at ECCV](https://chalearnlap.cvc.uab.cat/challenge/49/description/). The description of the former dataset, LSE_eSaude_UVIGO (ECCV'22), can be found [here](https://chalearnlap.cvc.uab.cat/dataset/42/description/), including the downloadable train/val/test splits for the two organized tracks (MSSL-multiple shot supervised learning, and OSLWL-one shot learning and weak labels). The results of the challenge with the description of the dataset, protocols and baseline models, as well as discussing top-winning solutions and future directions on the topic can be found in this [paper](https://dl.acm.org/doi/abs/10.1007/978-3-031-25085-9_13)

## Annotations

### 1. Translation from LSE to Spanish

- **Description**: Each video is translated into Spanish, segmented and aligned into sentences and smaller segments.
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
- Training/testing machine learning models for sign language translation, sign spotting, isolated sign language recognition and fingerspelling detection/recognition.
- Studying health-related sign language communication
- Analyzing linguistic patterns and structures within sign language

## Distribution

We provide two options for distribution:

#### 1. Direct download of:

- **[Excel file](https://github.com/PROJECT-TRAIN/LSE-Health-UVigo/blob/main/data/LSE-Health-UVigo.xlsx)**: Includes the links to download the videos from youtube, meta data and all the annotations (segments, glosses and fingerspelled words)
- **[273 annotation files](https://github.com/PROJECT-TRAIN/LSE-Health-UVigo/blob/main/data/ELAN-LSE-Health-UVigo.zip) using the ELAN program**: These files contain 3 Tiers explained below

#### 2. Download files from the Zenodo platform after signing an EULA agreement of
- the previous excel and ELAN files
- 273 FHD videos spanning ~11 hours of topics related to diseases, symptoms, treatment, care, etc.

## Annotations:

LSE-Health-UVigo has been annotated with the ELAN program. Annotators used three Tiers:

- **Tier ‘M_Glosa’** for the location of the 105 selected glosses.
- **Associated Tier ‘Var’** for annotating variants of the signed gloss. 3-letter codes have been defined to note 8 types of sign variations. These variations are:
    -  linguistic, like slight modifications of the sign due to relaxed execution (coded LAX), slight change of location in space (LOC), abnormal use of the non-dominant hand (MAN) and morphology changes as in distributed plurals (MPH), or
    -  non-linguistic, like very short sign due to speed and large coarticulation SHO), partial occlusion of the sign with other body parts (OCC) or because out of the frame (OUT) and other gloss with similar signed appearance to the selected gloss (SIM).
For the sake of completeness, these variations are not filtered out in the distribution, just informed.
- **Tier 'Trad'** for the translation into Spanish and annotation of start and end of each sentence or partial sentence. Translation of a visual language to a written language is not a trivial task. Two-letter codes have been defined to note 8 types of special events regarding visual-to-written translation. The next subsection explains the strict annotation criteria.

### Annotation criteria:

The annotation criteria shared by all the annotators (4) were as follows:

- **For Glosses and fingerspelled words**:
    - The begin_timestamp for a sign is set as soon as the parameters hand configuration, palm orientation and movement and/or location correspond to that sign more than to the transition from the previous one.
    - The end_timestamp for a sign is set as soon as the parameters hand configuration, palm orientation and movement and/or location start to change to a transition to the next sign.
    - As far as possible, transitions are not included in the annotated intervals.
    - A star ‘*’ prefix indicate that there’s slight drift from normal realization or that there's a OOV sign very similar visually. The reasons can be linguistic (MAN, LOC, MPH, LAX) or not linguistic (SHO, OCC, OUT, SIM)
    - It is important to highlight the annotation of the plurals. In Spanish sign Language, plurals use to be performed by sign repetition. Annotations for plurals are coded as a single interval comprising all the concatenated repetitions if no other parameter is modified. The only special case corresponds to the glosses PERSON and its plural PERSON(M-RE), that are coded with different gloss-class because the second repetition use to be smaller and relaxed, as a rebound without changing the hand configuration. 
  
- **For Translation**: The general criterion for segmentation (performed by a professional interpreter involved also in the recordings) was to adapt the text in OL (oral language) to resemble as closely as possible the signed LSE (Spanish Sign Language) and to segment complete phrases, or smaller particles if it results in more semantically coherent segments. Additionally, due to discursive and grammatical differences between OL and LSE, 8 specific types of annotations were defined and marked in brackets:
    - If the text in OL has a visual but not literal correspondence in LSE, it will be marked with the code "V" (visual) in brackets [V:original text].
    - When discursive markers are used in LSE that do not usually appear in the text, [MD:type-MD] is inserted in the corresponding text: [MD:one], [MD:two], [MD:three], etc. [MD:theme], [MD:alternative], [MD:section], [MD:next], etc.
    - When the phrase in LSE is affected by bimodal signing (restricted by the grammatical order in the text), it is marked as [B: and the text signed bimodally]. This phenomenon is very typical in Sign Language when the person is reading and translating in real-time, as in broadcasting.
    - When fingerspelling is used and/or the corresponding sign is given, it will be translated literally. For example, in tier 'Trad': "The disease called [DL:GALACTORREA], its sign is [GL:GALACTORREA]" is signed in LSE as (gloss-type notation): DISEASE NAME G-A-L-A-C-T-O-RR-E-A (fingerspelled), SIGN cl:fluid-chest (visually explained).
    - If a semantic confusion occurs when signing a specific sign, the substitution code is used [S: "Spanish text - GLOSS of the sign actually performed"]. For example, the text says "There are many species:" and in the signed video, the sign for "culinary spices" is used, therefore [S: species - SPICES] is inserted.
    - When a deictic is used that replaces part of the text because they have previously located what they are mentioning there, and it is necessary for the sentence to make sense: [VD:"text replaced by the deictic"].
    - When a sign is temporarily defined for that discourse context, [T: signed word] is used.

    The frequency of each type of annotation is: [MD: ] 941, [DL: ] 841, [B: ] 680, [S: ] 265, [V: ] 123, [GL: ] 70, [T: ] 63, [VD: ] 52

## License

The dataset is provided under license [CC BY-NC-SA](https://creativecommons.org/licenses/by-nc-sa/4.0/deed.en), that it is the same license assigned to the youtube videos by their owners. Please review the license for terms of use.

## Acknowledgments

This dataset is a collaborative effort of the next research goups and entities: 
- [Group of Multimedia Technologies (GTM)](http://gtm.uvigo.es/en/) from the [atlanTTic Research Center](https://atlanttic.uvigo.es/en) of [University of Vigo](http://www.uvigo.es) (Spain)
- [Group of Discourse and Society (GRADES)](http://grades.uvigo.gal) from the [School of Philology and Translation](https://fft.uvigo.es/en/) of [University of Vigo](http://www.uvigo.es) (Spain)
- [Federation of Deaf People Galician Associations (FAXPG)](http://www.faxpg.es)
- [Galician Health Service (SERGAS)](http://www.sergas.es)
Gratitude is extended to them for their contributions and support.

## Citation

If you use this dataset for your own research, cite the next publication:

Vázquez Enríquez, M, Castro, JLA, Fernandez, LD, Jacques Junior, JCS & Escalera, S 2023, ECCV 2022 Sign Spotting Challenge: Dataset, Design and Results. in L Karlinsky, T Michaeli & K Nishino (eds), Computer Vision – ECCV 2022 Workshops, Proceedings. Springer Science+Business Media, Lecture Notes in Computer Science (including subseries Lecture Notes in Artificial Intelligence and Lecture Notes in Bioinformatics), vol. 13808 LNCS, pp. 225-242, 17th European Conference on Computer Vision, ECCV 2022, Tel Aviv, Israel, 23/10/2022. https://doi.org/10.1007/978-3-031-25085-9_13
