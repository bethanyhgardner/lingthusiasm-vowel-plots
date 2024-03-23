[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.10642632.svg)](https://doi.org/10.5281/zenodo.10642632)

# Lingthusiasm Vowel Plots

## About

This repository includes the data, code, and [tutorial website](https://bethanyhgardner.github.io/lingthusiasm-vowel-plots/) accompanying Lingthusiasm's episodes about vowel plots. You can find the main episode, "What visualizing our vowels tells us about who we are", on [Lingthusiasm's website](https://lingthusiasm.com/post/745605428371701760/lingthusiasm-episode-90-what-visualizing-our) and the bonus episode, "How we made vowel plots with Bethany Gardner" on [Lingthusiasm's patreon](https://www.patreon.com/posts/99832833).

If you use this tutorial to make your own plots, I’d love to see them! If you have questions about this material, feel to get in touch with me by posting on discussion page or sending me an email. To see if I’m currently taking freelance contracts for data visualizations or other related tasks, send me an email (this GitHub username @ gmail.com).

## Includes
```
├── 1_find_words.qmd
├── 2_annotate_audio.qmd
├── 3_plot_vowels.qmd
```

The code for the tutorials, written in Python (`1_find_words.qmd` and `2_annotate_audio.qmd`) and R (`3_plot_vowels.qmd`) and rendered using [Quarto](https://quarto.org/).

```
├── audio
└── └──words
```

The audio data. Although `1_find_words.qmd` downloads all of the episodes from YouTube and `2_annotate_audio.qmd` refers to recordings of the Wells Lexical Set that Gretchen and Lauren made for me, only the .wav files that trim out individual words, plus the .TextGrid files annotating the vowel location in each word, are tracked in this repository.

```
├── data
│   ├── captions.csv
│   ├── formants.csv
│   ├── timestamps_all.csv
│   ├── timestamps_annotate.csv
└── └──transcripts.csv
```

Data files from the various stages of finding vowels in the Lingthusiasm episodes, then annotating that and the Wells Lexical Set recordings:

* Downloading the episode transcripts from the Lingthusiasm website  (`transcripts.csv`).
* Downloading the captions—which don't always have speaker labels and aren't always proofread, but do have timestamps—from YouTube (`captions.csv`).
* Finding target words in the transcript data and matching them to timestamps in the caption data (`timestamps_all.csv`) and (`timestamps_annotate.csv`).
* Extracting F1 and F2 after annotating the location of the vowel in each word in Praat (`formants.csv`). This is the data used in the plots.

```
├── plots
│   ├── 1_means_original.png
│   ├── 2_means_flipped.png
│   ├── 3_individual_points.png
│   ├── 4_words_episodes.png
│   ├── 4_words_lexical_set.png
│   ├── 5_ellipses.png
│   ├── gretchen_vowels_ep.png
│   ├── gretchen_words_ls.png
│   ├── lauren_vowels_ep.png
│   ├── lauren_words_ls.png
└── └── paired_vowels_ep.png
```

PNG files for all of the plots created in `3_plot_vowels.qmd`.

```
├── docs
├── index.qmd
└── _quarto.yml
```

Website files.


```
├── _environment.yml
```

Python environment info (using conda).

```
├── renv.lock
```

R environment info (using {renv}).

```
├── resources
│   ├── ipa_chart.png
│   ├── lingthusiasm_logo_circle.png
│   ├── lingthusiasm_logo_tagline.png
│   ├── praat_screenshot.png
│   ├── theme.css
└── └── wells_lexical_set.jpg
```

Images used in tutorial, Lingthusiasm logos included in plots, and CSS theme edited to make the website used the Lingthusiasm green color.
