Changelog
---------

PyHamTools 0.7.3
================

30. May 2019

 * fixed dependency redis dependency to use at least a version compatible with python 2.7.


PyHamTools 0.7.2
================

29. May 2019

 * Changed Macedonia to North Macedonia
 * Updated test fixtures
 * bumped dependencies to current versions

PyHamTools 0.7.1
================

21. May 2018

 * Refined FT8 frequencies


PyHamTools 0.7.0
================

20. May 2018
 * Added FT8 frequencies as DIGITAL
 * Updated test fixtures
 * Minor fixes wrt Kosovo & AD1C Countryfiles


PyHamTools 0.6.1
================

28. January 2018
 * Minor bugfix for lookuplib which used with country-files.com


PyHamTools 0.6.0
================

23. January 2018

 * Support for Python3 has been added
 * CI pipeline setup. Compatibility of Pyhamtools is now checked on Windows and
   Linux for Python 2.7, 3.4, 3.5, 3.6 and pypy
 * BREAKING CHANGE: Longitude is now provided with the correct sign for all
   lookup libraries. The AD1C cty format used by Countryfile and ClublogAPI
   provide the longitude with the wrong sign. This is now covered and internally
   corrected. East = positive longitude, West = negative longitude.
 * Added a function to download the Clublog user list and the associated activity dates
 * updated requirements for libraries used by pyhamtools
 * some slow regex were replaced by faster string based lookups


PyHamTools 0.5.6
================

20. August 2017

 * LOTW User list is now downloaded directly from ARRL



PyHamTools 0.5.5
================

18. August 2016

 * Refined callsign detection rule for two digit prefix with appendix (e.g. 7N0ERX/1)
 * Refined callsign detection rule for callsigns with two appendixes (e.g. SV8GXQ/P/QRP)



PyHamTools 0.5.4
================

11. January 2016

 * Bugfix: Callinfo.get_all(callsign, timestamp) did ignore timestamp
 * added unit test for the bug above
 * extended timeout for QRZ.com request to 10 seconds (sometimes a bit slow)
 * updated QRZ.com unit tests for fixture callsigns (XX1XX and XX2XX)


PyHamTools 0.5.3
================

30. December 2015

 * Updated DXCC entity name of ZL9 (arrl id 16) from Auckland & Campbell to "N.Z. Subantarctic Is." in countrymapping.json (tnx G0UKB)
 * Deleted "Auckland" (016) from countrymapping.json
 * corrected code example of latlong_to_locator() (tnx VE5ZX)

PyHamTools 0.5.2
================

14. April 2015

 * catching another bug related to QRZ.com sessions



PyHamTools 0.5.1
================

13. April 2015

 * improved handling of expired QRZ.com sessions


PyHamTools 0.5.0
================

5. April 2015

 * implemented QRZ.com interface into LookupLib [LookupLib]

 * changed and unified all output to Unicode

 * corrected Longitude to General Standard (-180...0° West, 0...180° East) [LookupLib]

 * improved callsign decoding alogrithm [CallInfo]

 * added special case to decode location of VK9 callsigns [CallInfo]

 * added handling of special callsigns which can't be decoded properly inside a separate callsign exception file (e.g. 7QAA) [CallInfo]

 * added ValueError when LOTW data from file contains too many errors [qsl]


PyHamTools 0.4.2
================

11. October 2014

 * added pyhamtools.qsl (get EQSL.cc and LOTW user lists)

PyHamTools 0.4.1
================

27. September 2014

 * short calls in different countries (e.g. 9H3A/C6A) are now decoded correctly

 * added pyhamtools.frequency

 * moved pyhamtools.utils.freq_to_band into pyhamtools.frequency

 * deprecated module pyhamtools.utils

PyHamTools 0.4.0
================

20. September 2014

 * Added module for locator based calculations (pyhamtools.locators)
