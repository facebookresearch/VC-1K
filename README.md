[Working on README.md]

# Dataset Description

## Folder Structure

The dataset is organized as follows:

```
.
├── Metadata.xlsx
├── video_with_even_fps/    # 930 videos
└── video_with_jitter_fps/  # 77 videos
```

- **`Metadata.xlsx`** — spreadsheet describing the details of every video in the dataset (device, camera, orientation, resolution, frame rate, lighting, motion, environment, and demographic attributes).
- **`./video_with_even_fps/`** — 930 videos with a consistent (even) frame rate.
- **`./video_with_jitter_fps/`** — 77 videos exhibiting frame rate jitter caused by device variability.

## Collection Methodology

The VC-1K dataset was collected through a structured data collection program engaging participants across five countries: the United States, Brazil, Mexico, India, and the Philippines. Participants were recruited to represent diverse demographics and were instructed to record short video sequences (~15 seconds) using their personal mobile devices in their natural environments (homes and public spaces).

The collection protocol specified controlled variation across the following dimensions:

- **Device**: Android (80%) and iOS (20%) smartphones
- **Camera**: Front-facing (90%) and rear-facing (10%)
- **Orientation**: Portrait (90%) and landscape (10%)
- **Resolution**: 720p (1280×720 landscape / 720×1280 portrait)
- **Frame rate**: 30 fps (primary), with 24 fps on select Android devices
- **Lighting**: Dark, low, medium, and good illumination
- **Motion**: Slow, medium, and fast background/subject motion
- **Environment**: Indoor and outdoor settings

All videos were captured using the device's native camera encoder (H.264/AVC) by the default high quality settings. We checked all the video and confirmed visually lossless quality, ensuring high source fidelity suitable for codec evaluation. The videos in the dataset were also recorded with voice. Participants provided informed consent and signed research participation agreements prior to data collection.

## Dataset Characteristics

The final dataset comprises 1,007 video sequences (930 with consistent frame rates and 77 exhibiting frame rate jitter from device variability). Table 1 summarizes the distribution of key attributes.

**Table 1: VC-1K Dataset Attribute Distribution.** Video Breakdown: 1007 Total (899 With Faces; 108 Outward-Facing, Rear-Camera, No-Face Videos)

| Attribute | Category | Count | Percentage |
| --- | --- | ---: | ---: |
| **Device** | Android | 798 | 79.2% |
| | iOS | 209 | 20.8% |
| **Orientation** | Portrait | 907 | 90.1% |
| | Landscape | 100 | 9.9% |
| **Camera** | Front-facing | 898 | 89.2% |
| | Rear-facing | 109 | 10.8% |
| **Environment** | Indoor | 760 | 75.5% |
| | Outdoor | 247 | 24.5% |
| **Motion** | Slow | 569 | 56.5% |
| | Medium | 303 | 30.1% |
| | Fast | 135 | 13.4% |
| **Lighting** | Good | 577 | 57.3% |
| | Medium | 347 | 34.5% |
| | Low | 59 | 5.9% |
| | Dark | 24 | 2.4% |
| **Frame Rate** | 30 fps | ~96% | — |
| | 24/25 fps | ~4% | — |

## Demographic Diversity

A key design goal of VC-1K is demographic representativeness. Unlike many existing datasets that skew toward specific populations, VC-1K was collected with explicit diversity targets across age, gender, ethnicity, and geography.

**Table 2: Demographic Distribution.** This Table Includes 899 Videos With Distinct Faces and Excludes 108 No-Talking-Head Videos.

| Attribute | Category | Count | Percentage |
| --- | --- | ---: | ---: |
| **Gender** | Female | 452 | 50.3% |
| | Male | 445 | 49.5% |
| | Non-binary | 2 | 0.2% |
| **Age** | 18–24 | 231 | 25.7% |
| | 25–50 | 445 | 49.5% |
| | 51+ | 223 | 24.8% |
| **Ethnicity** | Black | 227 | 25.3% |
| | White | 224 | 24.9% |
| | Latino/Hispanic | 221 | 24.6% |
| | South Asian | 130 | 14.5% |
| | Southeast Asian | 94 | 10.5% |
| | East Asian | 3 | 0.3% |
| **Country** | United States | 278 | 30.9% |
| | Brazil | 259 | 28.8% |
| | Mexico | 138 | 15.4% |
| | India | 131 | 14.6% |
| | Philippines | 93 | 10.3% |

This diversity ensures that technologies are evaluated across a representative range of skin tones, facial features, and environmental contexts—factors that can impact encoder behavior in video communication scenarios, particularly for face detection-based region-of-interest video coding.

## Content Characteristics

The majority of sequences (89%) feature a front-facing talking head, representative of the dominant video calling modality. The remaining sequences feature rear-camera footage capturing environments and objects, representing screen-sharing or environmental-show scenarios common in video calls.

Motion levels are intentionally skewed toward slow motion (57%), reflecting typical video calling behavior where participants are relatively stationary, with medium (30%) and fast (13%) motion sequences providing challenging test cases for encoder motion estimation.

# License

This project is licensed under the [Creative Commons Attribution-NonCommercial 4.0 International License (CC BY-NC 4.0)](https://github.com/facebookresearch/VC-1K?tab=License-1-ov-file#). This license permits sharing and adapting the work, provided it's not used for commercial purposes and appropriate credit is given. For a quick overview, visit [Creative Commons License](https://creativecommons.org/licenses/by-nc/4.0/).

