txt2wave
=========

This program converts a text file to a .mp3 audio file. For this, a linux utility called `pico2wave` is used. `pico2wave` takes a limited number of characters for text-to-speech conversion. This program solves the problem of the limited permissible characters.

Prerequisites
==============

System : The compliant systems under Linux kernels: Debian, Ubuntu, Maemo ...

The SVOX Pico engine is a software speech synthesizer for German, English (GB and US), Spanish, French and Italian.

Installation required :

    - svox (pico2wave) https://packages.debian.org/source/squeeze/svox

SVOX package on https://openrepos.net/

Installation order:

    - libttspico-data (https://openrepos.net/content/mickaelh/libttspico-data)
    - libttspico0 (https://openrepos.net/content/mickaelh/libttspico0)
    - libttspico-utils (https://openrepos.net/content/mickaelh/libttspico-utils)
    - libttspico-dev (https://openrepos.net/content/mickaelh/libttspico-dev)

or simply `sudo apt-get install libttspico0 libttspico-utils libttspico-data`

Usage
=======

There are options given for the command-line input, which will provide the user with the specifications of what type of speech he/she wants. The options are as follows :

    Options:
        -i, --input_text_file   reads a text file
        -l, --lang  Language (default: default_lang)
        -h, --Help  Show this message

    Options for languages :
        en-US   English
        en-GB   Great Britain
        de-DE   German
        es-ES   Spanish
        fr-FR   French
        it-IT   Italian

Command-Line Input Type:

    $ ./txt2wave.py [-i|--input_text_file] <input text file name> [-l|--lang fr-FR]

NOTE:
The optional parameter `[-l | --lang]` by default = `en-GB`

In the current directory of `txt2wave.py`, it will generate the `audio_book.mp3` file.
