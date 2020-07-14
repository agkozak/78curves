# Real-Time 78 Equalization Curves for Equalizer APO

This library of equalization curves allow you to listen to 78 rpm records with correct equalization in real time. Playback may be done using any program, as the correction to equalization is done using the [Equalizer APO](https://sourceforge.net/projects/equalizerapo/) system-wide equalizer (Windows required).

## Table of Contents

* [Introduction](#introduction)
* [Installing Equalizer APO](#installing-equalizer-apo)
* [Installing the Library of EQ Curves](#installing-the-library-of-eq-curves)
* [Using the Curves](#using-the-curves)
* [Curves Included](#curves-included)

## Introduction

In 1925, when phonograph records began to be recorded electrically, sound engineers ran into a problem: if bass frequencies were loud enough, the grooves of a record would not be wide enough to contain them. The cutter that made the record would overcut and the grooves would run together. Instead of opting for wider grooves (which would have the undesirable effect of shortening playing time), engineers began to reduce the amplitude of low frequencies with the expectation that playback equipment would adjust accordingly. Soon they discovered that increasing the amplitude of higher frequencies on the disc and de-emphasizing them during playback had the effect of suppressing surface noise and preserving sounds that might otherwise be lost, such as sibilants.

These adjustments between the encoding of sound on a record and the transformation it undergoes during playback are known as equalization. For several decades, many equalization curves were in use, with individual record labels using different standards and even changing their standards from year to year. Even with the move from 78s to LPs and 45s, various standards were in use.

By 1955, the United States had adopted the RIAA standard for sound recording; the rest of the world would eventually follow suit. To this day, most phono preamps apply the RIAA equalization curve to their output, which results in most 78s sounding rather muffled during playback. A common solution is to record a disc and then equalize it correctly soon afterwards. There are complications; modern equipment tends to reproduce all too faithfully the irritating surface noise of early 78s, which means that the collector will have to declick, decrackle, and even denoise each recording to make it listenable, perhaps even applying a low pass filter to deemphasize high-frequency noise well above the range of meaningful sound. One of the best software solutions to facilitate these sorts of 78 transfers is [Audacity](https://www.audacityteam.org/), which happens to have [a wiki](https://wiki.audacityteam.org/wiki/78rpm_playback_curves#78_rpm_shellac_labels_and_their_EQ) that documents nicely many of the historical equalization curves.

Unfortunately, this solution means that the collector never gets to enjoy the records fully in real time. My solution to this problem is to draw upon the wealth of research that the Audacity Team has done, but to use filters that can be used by a system-wide equalizer so that a record can be enjoyed while it spins. [Equalizer APO](https://sourceforge.net/projects/equalizerapo/) for Windows allows one to combine more than one EQ curve, so it is what I have used.

## Installing Equalizer APO

To use the EQ curves, you must first download [Equalizer APO](https://sourceforge.net/projects/equalizerapo/). After installing it, you will have to reboot your computer for the system-wide equalizer to work. The program is usually installed to `C:\Program Files\EqualizerAPO`. The configuration files are kept in `C:\Program Files\EqualizerAPO\config`.

## Installing the Library of EQ Curves

You can download the whole library of curves [as a ZIP file](https://github.com/agkozak/78curves/archive/master.zip) or using Git (from `https://github.com/agkozak/78curves`). Put the configuration files in the Equalizer APO configuration directory (`C:\Program Files\EqualizerAPO\config`). Please note that if you have already been using and have configured Equalizer APO, you may already have a `config.txt` file; please be sure to save it somewhere, as it will be overwritten.

## Using the Curves

Open the Configuration Editor from your Start Menu (it's in the Equalizer APO folder). That will open your `config.txt` configuration file.

The `config.txt` file contains all of the EQ curves in this library. To keep things simple, you may eventually choose to remove from it any curves that you do not need. If you want to restore an individual curve, you may do so by creating a 31-band graphic equalizer in Equalizer APO and then importing the relevant `.csv` file from your configuration directory.

To play any given record with the correct equalization, go through the following steps.

Determine at the beginning if the sound coming from your preamp is has an RIAA curve imposed on it. It usually is; almost all preamps (whether internal to the record player or external) use the RIAA curve, making an old shellac record sound rather muffled. In this case, you will want to turn on the *Inverse* RIAA curve, which will be the second item down in Equalizer Pro -- this will have the effect of undoing the RIAA equalization.

![Inverse RIAA](img/Inverse_RIAA.png)

Now that you are sure that your audio input is flat, it is time to impose the correct curve. If you need to, consult the [Audacity Wiki](https://wiki.audacityteam.org/wiki/78rpm_playback_curves#78_rpm_shellac_labels_and_their_EQ) to find the curve appropriate to the record you are playing. Turn on the relevant filter.

![Blumlein300](img/Blumlein300.png)
*In this example, Blumlein300 has been enabled; note that Columbia 78 below it is turned off. You will not generally want to enable more than one historical EQ curve.*

Start playing the record and see how it sounds. Equalizer APO doesn't play records; you will need other software to do that (I use Audacity with monitoring turned on). Most older shellac records from the 1920s and 1930s have a great deal of surface noise (mostly clicks and crackle). You will probably not want to hear the higher-frequency noise. Turn on and adjust the Low-pass filter (the first item in Equalizer Pro) to suppress high-frequency noise. If you get it right, all of the harsh clicks and crackle will become more pleasant to listen to (without too much muffling of the music itself).

![Low-Pass Filter](img/Low-Pass_Filter.png)
*Once the Low-pass filter is turned on, you may adjust how strong it is by spinning the wheel on the left or changing the number in the box. A noisy 1920s shellac record might need 4500 Hz; a higher-quality 1930s record might sound good at 9000 Hz; and for some later records, you can turn off the filter entirely.*

## Curves Included

Two basic curves you will need are:

* [Inverse RIAA](Inverse_RIAA.csv) - for flattening out any RIAA curve imposed by your preamp
* [RIAA](RIAA.csv) - included just in case you need it

I have made Equalizer Pro equivalents for Audacity's [EQ toolbox for 78 rpm shellacs](https://wiki.audacityteam.org/wiki/78rpm_playback_curves#EQ_Curves_Library):

* [500-FLAT 500N-0](500-FLAT_500N-0.csv)
* [American 78 - 250N-7](American_78_-_250N-7.csv) - *Note: Audacity's "American 78" is a compromise between two different real-world curves, 250N-8 (provided below) and 250N-6.*
* [BBC 2db/octave](BBC_2db-octave.csv)
* [Blumlein300 - 300N-0](Blumlein300_300N-0.csv)
* [Columbia 78 - 300N-16](Columbia_78_-_300N-16.csv)
* [Decca 78 - 300N-5.5](Decca_78_-_300N-5.5.csv)
* [European 78 - 250N-0](European_78_250N-0.csv)
* [Telefunken 400N-0](Telefunken_400N-0)
* [Western Electric](Western_Electric.csv)

Other curves:

* [250N-8](250N-8.csv)
* [AES - 400N-12.3](AES_-_400-12.3.csv)
* [Capitol - 400N-12.7](Capitol_400N-12.7.csv)
* [500N-5](500N-5.csv)
* [500N-8.5](500N-8.5.csv)
* [MGM - 500N-12](MGM_-_500N.12.csv)
* [500N-13.7](500N-13.7)
* [500N-16](500N-15.csv)
* [629N-12](629N-12.csv)

Feel free to open an issue and ask me to include any other curves that you need. If you are not a GitHub user, you may [contact me through my Elsie Carlisle website](https://www.elsiecarlisle.com/alexandros-kozak/).
