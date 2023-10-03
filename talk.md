<!-- cSpell:ignore olde synchronised -->
<!-- Comments to throw off 'Write Good' linter -->
<!-- cSpell:ignore iwou mbpv iaww -->
<!-- wg:iwou = write good: is wordy or unneeded -->
<!-- wg:cwm = write good: can weaken meaning -->
<!-- wg:mbpv = write good: may be passive voice -->
<!-- wg:iac = write good: is a cliche -->
<!-- wg:iaww = write good: is a weasel word -->

# HF Digital Modes Brief

A cursory glance at digital amateur radio modes, what to use, and how to do
them.

## Key Points

- Don't over-modulate!!!
- I love digital for compromised situations
- Easier than it looks
- Find help on YouTube and internet. Chances are someone else has tried your exact setup. HRCC Discord and TOADS Discord

## What is Digital?

2 : composed of data in the form of especial<!-- wg:cwm -->ly binary digits <https://www.merriam-webster.com/dictionary/digital>

## Digital Revolution

The Digital Revolution (also known as the Third Industrial Revolution) is the shift from mechanical and analogue electronic technology to digital electronics which began in the latter half of the 20th century, with the adoption and proliferation of digital computers and digital record-keeping, that continues to the present day. <https://en.wikipedia.org/wiki/Digital_Revolution>

## Is CW a Digital Mode?

Yes, and No. I discovered the philosophical argument depends on perspective.

- On/Off (2 symbols)
- Dit/Dah/intra-character-space/inter-character-space/word-space (5 symbols)
- Dit-with-trailing-space/Dah-with-trailing-space/character-space(minus trailing space)/word-space(minus trailing space) (4 symbols)
- ~26-alpha/~10-numeric/some-odd-punctuation/some-odd-prowords (~45 symbols)

## Popularity

Modes over last 2 hours

| Mode     |     Count |
| :--      |       --: |
| FT8      | 2,699,094 |
| FT4      |    64,954 |
| WSPR     |    29,971 |
| CW       |     8,998 |
| VARAC    |     5,336 |
| JS8      |     4,419 |
| T10      |     3,255 |
| MSK144   |       518 |
| PSK31    |       336 |
| JT65     |       137 |
| Q65      |        91 |
| ROS      |        85 |
| FST4W    |        36 |
| PI4      |        24 |
| OPERA    |        23 |
| RTTY     |        13 |
| FREEDV   |         6 |
| Q65A     |         4 |
| OLIVIA 8 |         3 |
| SIM31    |         3 |
| JT9      |         3 |
| OLIVIA-8 |         2 |
| JT65B    |         2 |
| Q65B     |         2 |
| OLIVIA   |         1 |
| PSK      |         1 |
| FSKH105  |         1 |

Pulled 2023-03-25T1415L  
<https://pskreporter.info/cgi-bin/pskstats.pl>

## FT8

<https://wsjt.sourceforge.io/wsjtx.html>

> FT8 or Franke & Taylor 8 is a frequency shift keying digital mode of radio communication. Following release on June 29, 2017, by its creators Joe Taylor, K1JT, and Steve Franke, K9AN, along with the software package WSJT, FT8 was<!-- wg:mbpv --> adopted rapid<!-- wg:cwm-->ly and, in little over two years, it became the most popular digital mode on spotting networks such as PSK Reporter.
>
> <https://en.wikipedia.org/wiki/FT8#>

Nobel Physics Prize winner Dr. Joe Taylor, K1JT

Steve Franke, K9AN University of Illinois - UC

> FT8 sends 77 information bits in 15-second cycles with 12.64 seconds of transmission time and 2.36 seconds of decode time for a user data rate of 6.09 bits/sec. Source encoding gives an effective throughput of about 5 words per minute. The required SNR in a 2500 Hz bandwidth is -21 dB, so the corresponding Eb/N0 is 10*log10(2500/6.09) = 26.1 dB greater, or -21 dB + 26.1 = 5.1 dB. The mode requires the sending and receiving computers to be<!-- wg:mbpv --> synchronised so, while manual time setting is possible, most users make use of automatic online time servers using NTP or by receiving broadcast time signals from the GPS to ensure their transmissions fall in the proper windows.
>
> Each FT8 transmission can support up to 13 text characters, coded using forward error correction to ensure proper transmission and decoding despite common radio effects such as fading, noise, interference, poor propagation, low power operation, or inefficient antennas in restricted urban spaces. As the mode is qu<!-- wg:iaww -->ite limited in the number of words that it can send, it onl<!-- wg:cwm -->y sends enough information to ensure a contact with each station.
>
> <https://en.wikipedia.org/wiki/FT8#Operation>

WSJT-X is the software.

Pros:

- DX
- Propagation
- compromised situation (antenna, noise floor, low power)

Cons:

- not conversational
- Time Synchronization is important!

Other discussion:

- GridTracker <https://gridtracker.org/>
- FT8 Automation tool(s) potentially \*ahem\* unattended operation
- Now phone apps with subset of FT8 capabilities

## WSPR

Weak Signal Propagation Reporter

The protocol was <!-- wg:mbpv -->designed, and a program written initially, by Joe Taylor, K1JT. [Wikipedia](https://en.wikipedia.org/wiki/WSPR_(amateur_radio_software))

> ### Protocol specification
>
> The standard message is &lt;callsign&gt; + &lt;4 character locator&gt; + &lt;dBm trans<!-- wg:iwou --> mit power&gt;; for example “K1ABC FN20 37” is a signal from station K1ABC in Maidenhead grid cell “FN20”, sending 37 dBm, or about 5.0 W (legal limit for 630 m). Messages with a compound callsign and/or 6 digit locator use a two-transmission sequence. The first transmission carries compound callsign and power level, or standard callsign, 4 digit locator, and power level; the second transmission carries a hashed callsign, 6 digit locator, and power level. Add-on prefixes can be up to three alphanumeric characters; add-on suffixes can be a single letter or one or two digits.
>
>     Standard message components after lossless compression:
>
>     28 bits for callsign,
>     15 bits for locator,
>     7 bits for power level,
>     total: 50 bits.
> <https://en.wikipedia.org/wiki/WSPR_(amateur_radio_software)#Protocol_specification>

Pros:

- Deep detection into the noise
- Antenna transmission and reception testing
- Low power. Ocean crossing at 200 mW!!!
- dedicated hardware available

Cons:

- not conversational

Other discussion:

- Finding Malaysian Airlines flight MH370 disappeared 8 March 2014
- using the three characters as simple canned message
- <http://wspr.rocks/>
- <http://www.wsprnet.org/drupal/> see 3rd Party Maps and Data

## FlDigi

<http://www.w1hkj.com/>

> Fldigi (short for Fast light digital) is a free and open-source program which allows an ordinary computer's sound card to be <!-- wg:mbpv -->used as a simple two-way data modem. The software is most<!-- wg:iaww -->ly used by amateur radio operators who connect the microphone and headphone connections of an amateur radio SSB or FM transceiver to the computer's headphone and microphone connections, respectively.
>
> This interconnection creates a "sound card defined radio" whose available bandwidth is <!-- wg:mbpv -->limited by the sound card's sample rate and the external radio's bandwidth.
>
> Such communications are normal<!-- wg:iaww -->ly done on the shortwave amateur radio bands in modes such as PSK31, MFSK, RTTY, Olivia, and CW (Morse code). Increasingly, the software is also being <!-- wg:mbpv -->used for data on VHF and UHF frequencies using faster modes such as 8-PSK.
>
> <https://en.wikipedia.org/wiki/Fldigi>

Dave Freese, W1HKJ

Pros:

- Lots of modes!
- Swiss Army Knife of Digital Modes
- Data modem
- Used for Emergency Communications already <http://www.arrl.org/NBEMS>
  - ARES (Amateur Radio Emergency Service)
  - [Salvation Army's SATERN (Salvation Army Team Emergency Radio Network)](https://centralusa.salvationarmy.org/usc/satern-program/)
- Suite of software
  - Flamp
    - verifiable chunks of message
    - can request/relay a chunk
  - Flmsg
    - Pre-formatted forms, without sending the common bits
  - Flrig
    - Control radio
    - Can stand-in as a proxy between radio apps and radio. One simple place to change rigs.

Cons:

- Lots of modes and lots of parameters to adjust for each mode
- doesn't hide complexity from new users

Other discussion

- Sights and Sounds of Digital Modes <http://www.w1hkj.com/modes/index.htm>
- Using Fldigi as a modem
- SWL can send articles and images <https://swradiogram.net/>
- Android App (sideloaded)
- [Build-a-Pi](https://github.com/km4ack/pi-build) to install on Raspberry Pi

## JS8CALL

<http://js8call.com/>

> JS8Call is a derivative of the WSJT-X application, restructured and redesigned for message passing using a custom FT8 modulation called JS8. It <!-- wg:iwou -->is not supported by nor endorsed by the WSJT-X development group. While the WSJT-X group maintains copyright over the original work and code, JS8Call is a derivative work licensed under and in accordance <!-- wg:iwou -->with the terms of the GPLv3 license. The source code modifications are public and can be <!-- wg:mbpv -->found in js8call branch of this repository: <https://bitbucket.org/widefido/js8call/>
>
> JS8Call is and will always be open-source and free software (free as in beer and free as in speech, do with it what you like, for sum of exact<!-- wg:cwm-->ly $0).
>
> You might be asking…why is this named JS8Call? Why was it renamed from FT8Call? Why not something else, like BACON or HF Messenger? Good question! It <!-- wg:iwou -->is <!-- wg:mbpv -->named this way as an homage to its heritage:
>
> - JS8Call was previous<!-- wg:cwm-->ly named FT8Call.
> - JS8Call uses a custom FT8 modulation called JS8 (Jordan Sherer designed 8-FSK modulation). This is the base RF transport.
> - JS8Call has a “directed calling” protocol laid over top the base RF transport to support free-form and directed message passing.
>
> Hence JS8 + Directed Calling = JS8Call. And in case you didn’t get that:
>
> The app is: **JS8Call**, the mode is: **JS8**
>
> <http://js8call.com/>

Pros:

- Good SNR performance
- Relay capability
- Store and forward message capability

Cons:

- Slow
- No forward error correction
- Time synchronization

Other Discussion:

- Chess over JS8Call in Massachusetts
- JS8Call over \*ahem\* CB
- JS8Call as internet backbone? <https://radengineering.tech/>

## WinLink

## VARA HF

## ARDOP

## HF Propagation Effects

- Multipath
- Fading (QSB)
- Echos
- 300 Baud limit
- Technician Privileges

## Interface

- DigiRig Mobile <https://digirig.net/product/digirig-mobile/>
- SignalLink USB (or SignalLink SL-1+) <https://www.tigertronics.com/slusbmain.htm>
- RigBlaster <http://www.westmountainradio.com/rigblaster.php>
- Digimode <http://xggcomms.com/>
- Soundcard
  - PC Soundcard
  - USB Soundcard
    - Sabrent USB Audio
  - Radio internal Soundcard
    - IC-7300

### CAT

- What is it?
- Serial overview (USB "fakes" it)
- CI-V hints

### Audio Interface

- Don't Over Modulate!!!

## Modes

Resources describing most modes, like Sights and Sounds of Digital Modes <http://www.w1hkj.com/modes/index.htm>.

## Online Resources

- W1HKJ home of FlDigi <http://www.w1hkj.com/>
  - Sights and Sounds <http://www.w1hkj.com/modes/index.htm>
  - Android App <http://www.w1hkj.com/files/AndFlmsg/>
  - NBEMS <http://www.arrl.org/nbems>
- APRS.fi <https://aprs.fi/>
- PSK Reporter <https://pskreporter.info/pskmap.html>
- JS8Call - <http://js8call.com/>
- WSJT-X - FT8 program <https://physics.princeton.edu/pulsar/k1jt/wsjtx.html>
  - "Get Started with FT8 - An Introduction for Beginners | WSJT-X Ham Radio"<https://youtu.be/YyWX0i87P0o>  
  Quick overview of FT8, some usage tips, GridTracker. No setup.
  - How To Setup Your HF Radio For Digital, WSJT-X FT8 <https://youtu.be/7uxIsadUStg>  
  HRCC, physical setup, not bad, older video, not specific
  - WSJT-X Basics in 10 minutes <https://youtu.be/UBwdSlDnDX4>  
  Overview of the interface. No setup.
  - Everybody's Trying the New FT8! (#104)<https://youtu.be/zHXScGrsw-A>  
  Great historical context.
  - Setting up for Digital Modes, AD#25 <https://youtu.be/COmSkT06_CY>  
  The best digital history.
  - GridTracker - Grid map Display <https://gridtracker.org/grid-tracker/>
- VARA HF - <https://rosmodem.wordpress.com/2017/09/03/vara-hf-modem/>
- Winlink - <https://www.winlink.org/>
- KM4ACK Build-a-Pi - <https://github.com/km4ack/pi-build>
- [SIGIDWIKI.com: Signal Identification Guide](https://www.sigidwiki.com/wiki/Signal_Identification_Guide)
  - Images and sounds of radio signals.
- This presentation's [predecessor](https://github.com/chrisBosse/ham-digi-prez)

### YouTube Channels

- Ham Radio Crash <!-- wg:iac -->Course [@HamRadioCrashCourse](https://www.youtube.com/@HamRadioCrashCourse)
  - Welcoming introduction to Ham Radio concepts.
- David Casler, KE0OG [@DavidCasler](https://www.youtube.com/@DavidCasler)
  - Classic teacher of Ham Radio.
- KM4ACK [@KM4ACK](https://www.youtube.com/@KM4ACK)
  - Build-a-Pi.
- Ham Radio 2.0 [@HamRadio2](https://www.youtube.com/@HamRadio2)
  - Product reviews and DMR.
- Off-Grid Ham Radio OH8STN [@OH8STN](https://www.youtube.com/@OH8STN)
  - Off-grid and HF digital modes.
- Temporarily Offline Ham Radio [@temporarilyoffline](https://www.youtube.com/@temporarilyoffline)
  - Ham radio and computers.

## Acronyms

- AM - Amplitude Modulation
- ARES - Amateur Radio Emergency Service
- ASK - Audio Shift Keying
- CAT - Computer Aided Transceiver
- CB - Citizens' Band (26.965 to 27.405 MHz [*ye olde* 11m ham band])
- Codec - coder/decoder, a device or computer program which encodes or decodes a data stream or signal <https://en.wikipedia.org/wiki/Codec>
- EME - Earth-Moon-Earth, moon bounce
- FEC - Forward Error Correction
- FM - Frequency Modulation
- FSK - Frequency Shift Keying
- HF - High Frequency (3 - 30 MHz)
- HRCC - Ham Radio Crash<!-- wg:iac --> Course - <http://hamradiocrashcourse.com/>
- IP - Ingress Protection (dust/water)
- IP - Internet Protocol
- LSB - Lower Side Band
- MAC - Machine Access Control, 6 byte identifier for network hardware 41:43:31:45:51:20 ("AC1EO ")
- MFSK - Multi<!-- wg:iwou -->ple Frequency Shift Keying
- NBEMS - Narrow Band Emergency Messaging Software <http://www.arrl.org/nbems>
- OOK - On-Off Keying
- PSK - Phase Shift Keying
- QSB - Q Code for "signal is fading" / "is my signal fading?"
- SATERN - Salvation Army Team Emergency Radio Network <https://centralusa.salvationarmy.org/usc/satern-program/>
- SDR - Software Defined Radio
- SNR - Signal to Noise Ratio
- SSB - Single Side Band
- USB - Universal Serial Bus
- USB - Upper Side Band
- VoIP - Voice Over IP (Internet Protocol)
- VOX - Voice on X-mit (Trans<!-- wg:iwou -->mit)
