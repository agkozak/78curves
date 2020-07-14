# Real-Time 78 Equalization Curves for Equalizer APO

This library of equalization curves allow you to listen to 78 rpm records with correct equalization in real time. Playback may be done using any program, as the correction to equalization is done using the [Equalizer APO](https://sourceforge.net/projects/equalizerapo/) system-wide equalizer (Windows required).

## Table of Contents

* [Introduction](#introduction)
* [Installing Equalizer APO](#installing-equalizer-apo)
* [Installing the Library of EQ Curves](#installing-the-library-of-eq-curves)
* [Using the Curves](#using-the-curves)

## Introduction

In 1925, when phonograph records began to be recorded electrically, sound engineers ran into a problem: if bass frequencies were loud enough, the grooves of a record would not be wide enough to contain them. The cutter that made the record would overcut and the grooves would run together. Instead of opting for wider grooves (which would have the undesirable effect of shortening playing time), engineers began to reduce the amplitude of low frequencies with the expectation that playback equipment would adjust accordingly. Soon they discovered that increasing the amplitude of higher frequencies on the disc and de-emphasizing them during playback had the effect of suppressing surface noise and preserving sounds that might otherwise be lost, such as sibilants.

These adjustments between the encoding of sound on a record and the transformation it undergoes during playback are known as equalization. For several decades, many equalization curves were in use, with individual record labels using different standards and even changing their standards from year to year. Even with the move from 78s to LPs and 45s, various standards were in use.

By 1955, the United States had adopted the RIAA standard for sound recording; the rest of the world would eventually follow suit. To this day, most phono preamps apply the RIAA equalization curve to their output, which results in most 78s sounding rather muffled during playback. A common solution is to record a disc and then equalize it correctly soon afterwards. There are complications; modern equipment tends to reproduce all too faithfully the irritating surface noise of early 78s, which means that the collector will have to declick, decrackle, and even denoise each recording to make it listenable, perhaps even applying a low pass filter to deemphasize high-frequency noise well above the range of meaningful sound. One of the best software solutions to facilitate these sorts of 78 transfers is [Audacity](https://www.audacityteam.org/), which happens to have [a wiki](https://wiki.audacityteam.org/wiki/78rpm_playback_curves#78_rpm_shellac_labels_and_their_EQ) that documents nicely many of the historical equalization curves.

Unfortunately, this solution means that the collector never gets to enjoy the records fully in real time. My solution to this problem is to draw upon the wealth of research that the Audacity Team has done, but to use filters that can be used by a system-wide equalizer so that a record can be enjoyed while it spins. [Equalizer APO](https://sourceforge.net/projects/equalizerapo/) for Windows allows one to combine more than one EQ curve, so it is what I have used.

## Installing Equalizer APO

## Installing the Library of EQ Curves

## Using the Curves

* [Inverse RIAA](Inverse_RIAA.csv)
* [RIAA](RIAA.csv)

This library provides Equalizer Pro equivalents for Audacity's [EQ toolbox for 78 rpm shellacs](https://wiki.audacityteam.org/wiki/78rpm_playback_curves#EQ_Curves_Library):

* [500-FLAT 500N-0](500-FLAT_500N-0.csv)
* [American 78 - 250N-7](American_78_-_250N-7.csv) - *Note: Audacity's "American 78" is a compromise between two different real-world curves, 250N-8 (provided below) and 250N-6.*
* [BBC 2db/octave](BBC_2db-octave.csv)
* [Blumlein300 - 300N-0](Blumlein300_300N-0.csv)
* [Columbia 78 - 300N-16](Columbia_78_-_300N-16.csv)
* [Decca 78 - 300N-5.5](Decca_78_-_300N-5.5.csv)
* [European 78 - 250N-0](European_78_250N-0.csv)
* [Telefunken 400N-0](Telefunken_400N-0)
* [Western Electric](Western_Electric.csv)

I include other curves:

* [250N-8](250N-8.csv)
* [AES - 400N-12.3](AES_-_400-12.3.csv)
* [Capitol - 400N-12.7](Capitol_400N-12.7.csv)
* [500N-5](500N-5.csv)
* [500N-8.5](500N-8.5.csv)
* [MGM - 500N-12](MGM_-_500N.12.csv)
* [500N-13.7](500N-13.7)
* [500N-16](500N-15.csv)
* [629N-12](629N-12.csv)
