<!---
title: "CWDAML and Adaptive CWDA Algorithm"
excerpt: "Adaptive learning algorithms proposed in my PhD."
mathjax : true
header:
  teaser: assets/images/PhD/ACWDA_BER.jpg
sidebar:
  - title: "Role"
    text: "PhD student (2010-2014)"
  - title: "Topic"
    text: "Statistical Signal Processing and Adaptive Filter Theory"
  - title: "Application"
    text: "Optical Communication receiver design"
  - title: "Contributions"
    text: "Proposed (i) 2 novel adaptive learning algorithms, namely, CWDAML and adaptive CWDA for long-haul optical communication receiver design, and (ii) an all-optical filter design for intensity-modulated direct-detected radio-over-fiber receivers, used in broadband wireless optical access networks."
feature_row:
  - image_path: assets/images/PhD/ACWDA_BER.jpg
  - image_path: assets/images/PhD/ACWDA_BER_and_cycle_slip.jpg
  - image_path: assets/images/PhD/ACWDA_NL_cycle_slip.jpg
---

{% include feature_row %}

{% include toc %}

## Overview

### Thesis
<a href="http://scholarbank.nus.edu.sg/handle/10635/118577">Digital and optical compensation of signal impairments for optical communication receivers</a>

### Info
This is my Ph.D. dissertation work. I proposed and implemented 2 novel adaptive learning algorithms for real-time-series data prediction and classification using modified linear and logistic regression techniques, which was applied to long-haul optical communication receiver application.
* CWDAML: A complex-weighted, decision-aided, maximum-likelihood, phase and frequency estimator for intradyne coherent receivers
* Adaptive CWDA: A low complexity, low cycle-slip probability, format-independent carrier estimator with adaptive filter length for linear- and nonlinear-noise impaired channels

Here, our algorithms (i) predict the impairment value (i.e., noise) introduced in the optical fiber using statistical modelling techniques and then (ii) classify the received data (bits, i.e., 1s and 0s) at the receiver using regression and adaptive learning techniques. We provide below on this page, a brief explanation of the (i) prediction/classification problem addressed by CWDAML and adaptive CWDA algorithms and (ii) the Matlab source codes simulating the prformance of these two algorithms. For brevity, mathematical derivations, proofs, and analysis, are left to the thesis for interested readers.

Furthermore in my PhD, I had proposed an optical filter design for simultaneous signal equalization, chirp modulation, and single-sideband filtering in intensity-modulated direct-detection (IMDD) radio-over-fiber (RoF) receivers, used for broadband wireless optical access networks. This is an ingenious, highly efficient, all-optical-domain signal processing technique, with no need for additional digital signal processing. It solves multiple problems simultaneously, namely, constrained modulation bandwidth, limited transmission distance, and radio frequency signal fading. The effectiveness of our optical filter design was proved experimentally. Interested readers may refer to my thesis for the mathematical operating principles and for further explanation of our proposed optical filter design.  

### Repository
The [repository](https://github.com/Adaickalavan/CWDAML_and_AdaptiveCWDA) consists of the following: 
* Complex Weighted Decision Aided Maximum Likelihood - Matlab codes
* Adaptive Complex Weighted Decision Aided - Matlab Codes

## Review
Long haul optical communication systems aim for bit rates per channel in excess of
100 Gb/s as the next interface rates are geared toward 400 Gb/s and 1 Tb/s[^3]<sup>,</sup>[^4].
Increasing the transmission capacity, to service the growth of data traffic, at a fixed
optical amplification bandwidth requires increasing the spectral efficiency. 

Coherent detection with multilevel modulation promises superior spectral efficiency, receiver sensitivity, and transmission distance compared to noncoherent systems[^15], and enables the attainment of Shannon’s capacity with the use of coding such as Turbo codes[^16]<sup>,</sup>[^17]<sup>,</sup>[^18].

A major impediment in homodyne coherent detection is the synchronization of the local oscillator (LO) laser to the optical carrier of the received optical signal. The received signal can be perturbed by phase noise arising from nonzero laser linewidth $$\Delta\nu$$ and frequency offset $$\Delta f$$ between the transmitter and LO lasers.

Current interest lies in intradyne coherent detection using a free running LO laser,
followed by sampling with high-speed analog-to-digital converter (ADC), and execution
of carrier estimation in digital signal processing (DSP) modules [31].

<figure>
  <img src="/assets/images/PhD/coh_sys.jpg" alt="Polarization multiplexed coherent optical communication receiver. Tx: transmitter.">
  <figcaption>Polarization multiplexed coherent optical communication receiver. Tx: transmitter.</figcaption>
</figure>

Most long haul transmission systems are limited by inline optical amplifier noise, which is additive
white Gaussian noise (AWGN) in nature[^5].

Accuracy of prediction and classification is measured in terms of bit-error rate.

Contents are still being added. Check back later for more updates. 
The two subsections below are currently meant to be placeholders with some brief details.
{: .notice--warning}

### CWDAML

The <a href="https://github.com/Adaickalavan/CWDAML_and_AdaptiveCWDA">repository</a> contains the Matlab code to simulate [1] Complex-Weighted Decision-Aided Maximum-Likelihood (CWDAML) and [2] Adaptive Complex-weighted Decision-Aided (Adaptive CWDA), algorithms for M-ary Phase-Shift Keying (MPSK) and M-ary Quadrature Amplitude Modulation (MQAM) modulation formats in the presence of laser phase noise and frequency offset impairments at the receiver. The simulations consists of transmitter, fiber optic transmission medium, laser phase noise, frequency offset between transmitter and receiver oscillator lasers, IQ receiver, and baseband digital signal processing algorithm comprising CWDAML or adaptive CWDA algorithm.

For CWDAML:
<ol>
	<li>The codes will draw BER vs SNR graph.</li>
	<li>In the Matlab folder, you only have to modify the parameters in “Batch_file_16QAM.m” or "Batch_file_4PSK.m" which is the main file.</li>
	<li>The batch file will call all other files which are function files.</li>
	<li>For a start with my Matlab codes, you can simply run the batch file as-is without any modifications.</li> 
	<li>It will produce a BER vs SNR graph corresponding to that of CWDAML algorithm.</li>
	<li>The simulation will take several minutes to complete.</li>
	<li>You will need to create a "Simulation Results" folder in the same directory as the rest of the codes to store the results at the end of the simulation.</li>
</ol>

The default settings in "Batch_file_4PSK.m" are:

```
symbol rate = 28e9 symbols/s
Filter length = 15
Laser linewidth = 11.2e6 Hz
Frequency offset = 2.8e9 Hz
The default settings in "Batch_file_16QAM.m" are:
symbol rate = 28e9 symbols/s
Filter length = 12
Laser linewidth = 1.12e6 Hz
Frequency offset = 2.8e9 Hz
```

### Adaptive CWDA
An adaptive complex-weighted decision-aided carrier estimator is introduced, whose effective filter length automatically adapts according to the SNR with no preset parameters required. Besides bit error rate, choice of filter length also affects the cycle slip probability.

### References
[^3]: P. J. Winzer, “Beyond 100G ethernet,” IEEE Commun. Mag., vol. 48, no. 7, pp. 26–30, Jul. 2010.
[^4]: A. H. Gnauck, P. J. Winzer, S. Chandrasekhar, X. Liu, B. Zhu, and D. W. Peckham, “Spectrally efficient long-haul WDM transmission using 224-Gb/s polarization-multiplexed 16-QAM,” J. Lightw. Technol., vol. 29, no. 4, pp. 373–377, Feb. 2011.
[^5]: K.-P. Ho, “Exact evaluation of the capacity for intensity-modulated direct detection channels with optical amplifier noises,” IEEE Photon. Technol. Lett., vol. 17, no. 4, pp. 858–860, Apr. 2005.
[^15]: L. G. Kazovsky, G. Kalogerakis, and W.-T. Shaw, “Homodyne phase-shift keying systems: past challenges and future opportunities,” J. Lightw. Technol., vol. 24, no. 12, pp. 4876–4884, Dec. 2006.
[^16]: C. Berrou, A. Glavieux, and P. Thitimajshima, “Near Shannon limit error correcting coding and decoding: turbo-codes,” in Proc. ICC, Geneva, Switzerland, 1993, pp. 1064–1070.
[^17]: S.-Y. Chung, G. D. Forney, Jr., T. J. Richardson, and R. Urbanke, “On the design of low-density parity-check codes within 0.0045 db of the Shannon limit,” IEEE Commun. Lett., vol. 5, no. 2, pp. 58–60, Feb. 2001.
[^18]: C. Berrou, “The ten-year-old turbo codes are entering into service,” IEEE Commun. Mag., vol. 41, no. 8, pp. 110–116, Aug. 2003.-->