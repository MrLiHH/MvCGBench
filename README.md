# MvCGBench

A benchmark for **Movie Commentary Generation**, introduced in *Clip Movies to Shorts: Narration-Guided Movie Commentary Generation*.

MvCGBench pairs plot-oriented narration queries with temporal intervals in full-length movies, together with temporally aligned subtitles.

## Dataset

The paper reports:

- **100 movies**, totaling **217.6 hours** (130.57 minutes per movie on average).
- **135,228** temporally aligned subtitle entries.
- **12,109** narration-segment pairs, with 29.3 words per query on average.
- A movie-level train/validation/test split of **80/10/10**.

## Data access

We distribute **features and annotations**, without original movies, extracted images, or soundtracks.

- **Public experience set:** 10 selected movies, comprising 9 test movies and 1 training movie, with **1,109 queries**. Feature extraction and validation are in progress; download links will be added here when ready.
- **Remaining 90 movies:** apply through the [MvCGBench research access form](https://docs.qq.com/form/page/DUEdpTENpQkdBZ0xa). Applications are reviewed manually. Approved applicants receive a cloud-drive download link by email, valid for **30 days**.

Experience-set movie IDs: `001, 003, 005, 006, 007, 097, 114, 138, 144, 161`. Movie `007` retains its training label; the others retain their test labels. This experience set is not the original test split and does not change the paper's split.

## Features and evaluation

The paper uses PySceneDetect (threshold 30), visual sampling at **1 fps**, and **Qwen2.5-VL-7B** as the default backbone. The feature release is being prepared using projected visual tokens; exact extraction settings and provenance will accompany the downloads.

CF-MvCG combines context-aware narrative encoding, query-segment attention, adaptive coarse localization, and narration-duration-aware boundary refinement. Temporal localization is evaluated using **R@K-BIoU**. Rendering audiovisual commentaries requires users to supply their own legally obtained movies.

## Terms

Use restricted data only for the approved research purpose. Do not redistribute restricted data or download links, or attempt to reconstruct original audiovisual media. Third-party rights remain with their respective holders. See [ACCESS.md](ACCESS.md) for the application process.
