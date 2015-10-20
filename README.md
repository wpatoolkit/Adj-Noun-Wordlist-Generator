# Adj Noun Wordlist Generator 
This is a small program written in C++ that will output all possible combinations of adjectives, nouns and digits in the format...<br>

`adjective + noun + 1 digit`<br>
`adjective + noun + 3 digits`

By using the -0, -1, -2, or -3 parameters you can control exactly how many digits you want appended.<br>
(by default only 1 and 3 digits are appended)<br>

To compile on Windows (requires the <a href="http://www.microsoft.com/en-us/download/details.aspx?id=8279">Windows 7 SDK</a>):<br>
`cl /EHsc adj.cpp`

To compile on Linux:<br>
`g++ adj.cpp -oadj`

##Example usage:
`adj | oclHashcat64 -m 2500 CAP.hccap`<br>
pipes its output into <a href="http://hashcat.net/oclhashcat/">oclHashcat</a> (AMD)

`adj | cudaHashcat64 -m 2500 CAP.hccap`<br>
pipes its output into <a href="http://hashcat.net/oclhashcat/">cudaHashcat</a> (NVIDIA)

`adj | aircrack-ng -w - CAP.cap -e SSID`<br>
pipes its output into <a href="http://www.aircrack-ng.org/">aircrack-ng</a>

`./adj | pyrit -r CAP.cap -i- attack_passthrough`<br>
pipes its output into <a href="https://code.google.com/p/pyrit/">pyrit</a>

## Parameters
`-0`<br>
Will output (adjective)+(noun) only<br>

`-1`<br>
Will output (adjective)+(noun)+(1 digit) only<br>

`-2`<br>
Will output (adjective)+(noun)+(2 digits) only<br>

`-3`<br>
Will output (adjective)+(noun)+(3 digits) only<br>

`-full`<br>
Uses a more comprehensive set of words.

By default a set of 152 adjectives and 136 nouns are used (approx. 20,878,720 combinations ~ 319MB).

If you use the -full switch 968 adjectives and 1,844 nouns are used (approx. 1,802,841,920 combinations ~ 27.5GB).
