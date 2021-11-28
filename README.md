[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/dmarx/pytti/blob/master/PYTTI_pseudo_clone.ipynb)

# pytti
python text to image - [David Marx](https://twitter.com/DigThatData) edition

## FAQ

### What is this?

In Spring 2021, Katherine Crowson ([@RiversHaveWings](https://twitter.com/RiversHaveWings)) published two google colab notebooks (under the MIT license) which ignited a surge of interest in generating AI art using CLIP-embedded text prompts as a guide. At present, the vast majority of tools that leverage "VQGAN+CLIP" for image generation were modified from Katherine's notebooks. PYTTI is a popular variant authored by [@sportsracer48](https://twitter.com/sportsracer48). This is a hacked-together interface to sportsracer48's public code base, which is undocumented and non-functional without the pytti notebook.


### Isn't this notebook supposed to be like top secret?

sportsracer48 has published some of his code in an MIT licensed [public github repo](https://github.com/sportsracer48/pytti), but has not released the notebook which serves as an interface to this backend code. Access to his notebook is limited to his patreon supporters (of which I'm not), but the backend code is public and freely licensed. I just stumbled around with that code until I could make it work.


### This seems wildly underfeatured.

I haven't made an attempt to support the majority of pytti parameters or features. If you want to add something that's missing you can probably at least figure out what the parameter is supposed to be called by looking for pytti tutorials on youtube or whatever.

I mainly just wanted to get this working enough that I could figure out how certain effects are achieved.


### So What is some of the "secret sauce" you found?

* [AdaBins](https://github.com/shariqfarooq123/AdaBins) for depth estimation
* [GMA](https://github.com/zacjiang/GMA.git) (an adaptation of [RAFT](https://github.com/princeton-vl/RAFT)) for optical flow estimation
* Techniques from [dribnet's pixray](https://github.com/dribnet/pixray) project for pixel art generation
* Using an ensemble of CLIP models ("perceptors") for steering rather than just one

Honestly, I haven't dug into the code much yet beyond just getting it to run.
