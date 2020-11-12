![VideoSilenceRemover](https://socialify.git.ci/bjoernpl/VideoSilenceRemover/image?description=1&descriptionEditable=Automatically%20cut%20video%20into%20segments%20containing%20speech%20while%20removing%20silence.&language=1&owner=1&pattern=Signal&theme=Dark)
# VideoSilenceRemover
### Automatically cut video into segments containing speech while removing silence.

This repo contains a Jupyter Notebook which demonstrates the combination
of [pyAudioAnalysis](https://github.com/tyiannak/pyAudioAnalysis) and [FFmpeg](https://ffmpeg.org/)
to cut any input video into distinct segments containing speech. To do this,
it uses pyAudioAnalysis `audioSegmentation.silence_removal()` function to find the start and end
times of speech segments, and a bunch of FFmpeg calls for all audio and video conversions, cuts and concatenations.

## Installation

#### Step 1. Prerequisites
- `conda` or some other environment manager to create a virtual environment.
- `python 3.7` and the `linux` distro of your choice are recommended.
- `ffmpeg` must be installed and in the path. See [here](https://ffmpeg.org/download.html) for more info.

#### Step 2. Clone this repo
Clone this repo while making sure to include `--recursive` to also get the [pyAudioAnalysis](https://github.com/tyiannak/pyAudioAnalysis) submodule.
```
git clone --recursive git@github.com:bjoernpl/VideoSilenceRemover
```

#### Step 3. Install pyAudioAnalysis
To install pyAudioAnalysis, first make sure your virtual environment is activated.
```
cd ./pyAudioAnalysis
pip install -r ./requirements.txt
pip install -e .
```

#### Step 4. Install requirements
```
cd ..
pip install -r ./requirements.txt
```

#### Done!
You can now run the notebook by calling `jupyter lab` or `jupyter notebook`.

## Usage
For more info on the usage, see the explanations in `VideoSegmentation.ipynb`

## References
This repo relies mainly on the [pyAudioAnalysis](https://github.com/tyiannak/pyAudioAnalysis) library. Thanks very much to it's creators and contributors.
```
@article{giannakopoulos2015pyaudioanalysis,
  title={pyAudioAnalysis: An Open-Source Python Library for Audio Signal Analysis},
  author={Giannakopoulos, Theodoros},
  journal={PloS one},
  volume={10},
  number={12},
  year={2015},
  publisher={Public Library of Science}
}
```

Thanks also to the creators and contributors at [FFmpeg](https://ffmpeg.org/) for their awesome tool.
