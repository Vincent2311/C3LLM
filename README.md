<h1 align="center">C3LLM: Conditional Multimodal Content Generation Using Large Language Models</h1>
<div align="center">
  <span class="author-block">
    Zixuan Wang<sup>1*</sup>,</span>
  <span class="author-block">
    Qinkai Duan<sup>1*</sup>,</span>
  <span class="author-block">
    Yu-Wing Tai<sup>2</sup>,</span>
  <span class="author-block">
    Chi-Keung Tang<sup>1</sup>,</span>
</div>
<div align="center">
  <span class="author-block"><sup>1</sup>HKUST,</span>
  <span class="author-block"><sup>2</sup>Dartmouth College</span>
</div>

[![arXiv](https://img.shields.io/badge/arXiv-2405.16136-brightgreen.svg?style=flat-square)](https://arxiv.org/abs/2405.16136)  

## Abstract

<p align="center">
  <img align="middle" width="800" src="assets/arch-1.png"/>
</p>
We introduce C3LLM (Conditioned-on-Three-Modalities Large Language Models), a novel framework combining three tasks of video-to-audio, audio-to-text, and text-to-audio together. C3LLM adapts the Large Language Model (LLM) structure as a bridge for aligning different modalities, synthesizing the given conditional information, and making multimodal generation in a discrete manner. Our contributions are as follows. First, we adapt a hierarchical structure for audio generation tasks with pre-trained audio codebooks. Specifically, we train the LLM to generate audio semantic tokens from the given conditions, and further use a non-autoregressive transformer to generate different levels of acoustic tokens in layers to better enhance the fidelity of the generated audio. Second, based on the intuition that LLMs were originally designed for discrete tasks with the next-word prediction method, we use the discrete representation for audio generation and compress their semantic meanings into acoustic tokens, similar to adding “acoustic vocabulary” to LLM. Third, our method combines the previous tasks of audio understanding, video-to-audio generation, and text-to-audio generation together into one unified model, providing more versatility in an end-to-end fashion. Our C3LLM achieves improved results through various automated evaluation metrics, providing better semantic alignment compared to previous methods. Our Code will be released in the coming future.

## Methodology
Overview of the video encoding part and the LLM. 
<p align="center">
  <img align="middle" width="800" src="assets/arch-video.png"/>
</p>

Overview of audio encoding part and the LLM.
<p align="center">
  <img align="middle" width="800" src="assets/arch-audio.png"/>
</p>

## Experiments
Qualitative result on synchronization compared with CoDi. Our result is clearly more structured and aligned with the video input
<p align="center">
  <img align="middle" width="70%" src="assets/sync.png"/>
</p>

Quantitative result on three tasks
<p align="center">
  <img align="middle" width="70%" src="assets/main-result.png"/>
</p>

Quantitative result on evaluating synchronization for video-to-audio task
<p align="center">
  <img align="middle" width="70%" src="assets/sync-eval.png"/>
</p>

# Demo results
Demo for video-to-audio task. We combine the input silent video together with the generated audio to better show the alignment.


https://github.com/Vincent2311/C3LLM/assets/90130756/c5b9c858-7009-4591-a1aa-82576eab3a9a



https://github.com/Vincent2311/C3LLM/assets/90130756/e13ef660-e8b6-402e-8ad4-24c0a53a11fd



https://github.com/Vincent2311/C3LLM/assets/90130756/733c5f8c-44a4-43b3-91a1-865b3cbbbf76



