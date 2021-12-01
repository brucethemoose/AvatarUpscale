The Blu Ray release of Avatar: The Last Airbender doesn't look great. So I'm gathering info on my previous attempts to upscale and clean up Avatar: The Last Airbender in one place, in the hopes of improving on the Blu Ray release. 

## Communities/Links
* GameUpscale Discord: https://discord.gg/cpAUpDK
* Specialized, pretrained ESRGAN models: https://upscale.wiki/wiki/Model_Database
* Vapoursynth help/discussion: http://forum.doom9.org/forumdisplay.php?s=6daf8be50c83c830ee8ab4b27c41f654&f=82
* GUI for browsing and installing (almost) every Vapoursynth plugin/script: https://github.com/theChaosCoder/VSRepoGUI

## General Info

* The original fan ATLA remaster floating around the internet was upscaled from the DVDs with Waifu2X and some other basic vapoursynth filters, but Waifu2X is basically obsolete.

* In my opinion, the Blu Ray is a better release than the DVD, and sharper, cleaner source material to work with for a future "remaster." But I have been told that it has some issues (frame blending, deinterlacing artifacts, motion stutter in a few native 30p scenes) that the DVDs don't have.

* Anime4K is a popular upscaler and anime cleaner, but I'm not particular impressed with the improvement I get with Avatar, particularly with the painted backgrounds. 

* Topaz AI is another popular upscaler/processor, one that I have yet to try.

* In general, upscaling anime/cartoon videos with AI networks is tricky, as noise can create temporal artifacts in otherwise static areas. Therefore, if a 2D upscaler like ESRGAN is to be used, the source *must* be denoised, and the AI filter can be temporally stabilized with another filter. 

* True video upscaling/processing networks have been finicky, impractical to train, and difficult to run in the past, but there are some new ones I have yet to try. 

## Blu Ray Issues To Solve/Replicate

- [ ] Temporal Noise/Grain
- [ ] Oversharpening
- [ ] Vertical blur (?)
- [ ] Get "native" res and scaling kernel of the source
- [ ] Frame interpolation (?)
- [ ] Blended frames


## Repos

* traiNNer: Train ESRGAN models with various parameters/options. Look for active forks in the GitHub network view for colab variants and new features: https://github.com/victorca25/traiNNer

* Vapoursynth: filter videos with python scripts: https://github.com/vapoursynth/vapoursynth

* Utility to get the native resoltion/upscaling kernel of upscaled materail: https://github.com/Infiziert90/getnative

* BM3D(CPU): good temporal denoiser: https://github.com/HomeOfVapourSynthEvolution/VapourSynth-BM3D

* CUDA version of BM3D: https://github.com/WolframRhodium/VapourSynth-BM3DCUDA

* Havsfunc: Has a very effective deinterlacer/decomber (QTGMC) and effective temporal denoisers (MCTemporalDenoise, KNLMeansCL): https://github.com/HomeOfVapourSynthEvolution/havsfunc/blob/master/havsfunc.py

* Scaling and debanding accelerated by MPV's backend: https://github.com/Lypheo/vs-placebo

## Datasets

* 1GB of hand-picked, cleaned Korra Blu-Ray frames: https://1drv.ms/u/s!AmOOktI6vxKegTzajSq4Q0d23iSS?e=lgIS6X

* (Larger, more complete datasets will be uploaded later)

## Degradation filters

(WIP)

## Trained Models

* Previous (mostly) 1x ESRGAN model attempts, trained on degraded Korra Blu-Ray frames with traiNNer, targeting the ATLA Blu Rays: https://1drv.ms/u/s!AmOOktI6vxKehzCwpd3plVxSEWtk?e=9UdFJH

* 2x Vertical Deblur model, possibly useful for the DVDs, from SaurusX on the GU Discord [(preview)](https://imgsli.com/ODIxMjU): https://mega.nz/file/vOwmULKK#nFznUd8ZY3-P0x9_63OyYE8eZifmTvZqDejIrMBXJtk

* A 2x model trained on Korra frames, targeting the ATLA DVDs, from aptitude on the GU Discord [(preview)]:(https://imgsli.com/NjIzMjQ) https://www108.zippyshare.com/v/PYWFtETd/file.html


## Scripts

* See "scripts" folder in the repo (soon)


## Untested repos to research

* Nvidia-accelerated processing and an interesting IQ metric: https://github.com/AkarinVS/vapoursynth-plugin

* Load models in vapoursynth: https://github.com/styler00dollar/vs-vfi

* Load ESRGAN models into vapoursynth, needs modification for high bit depth input: https://github.com/rlaphoenix/VSGAN

* Load HiNet models: https://github.com/HolyWu/vs-hinet

* Yet another scaler: https://github.com/HolyWu/vs-swinir

* Untested, animation-focused frame interpolation network: https://github.com/ShuhongChen/eisai-anime-interpolator

* Untested video network: https://github.com/HolyWu/vs-basicvsrpp

* Untested video network: https://github.com/csbhr/Deep-Blind-VSR

* Untested deblocking network: https://github.com/HolyWu/vs-dpir