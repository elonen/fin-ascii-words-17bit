# Long Finnish Word List for ASCII-Only Passphrases

This is a curated list of over 150,000 inflected Finnish and loan words, specifically designed for generating Diceware-like passwords for Finnish speakers.
Inclusion of inflected forms makes the passphrases cryptographically stronger.

The list uses only basic Latin alphabet (a-z, no umlauts äöå) and provides approximately 17.2 bits of entropy per word.

Compared to Noppaware (https://users.ics.aalto.fi/kaip/noppaware/):
- Words containing umlauts are _excluded_, not converted to a/o
- ~4 bits more entropy per word

## Methodology

The word list was created through the following process:

1. Started with a Finnish Wikipedia dump that included word base forms and their inflections (https://www.kielipankki.fi/download/wikipedia-fi/wikipedia-fi-2017-src/)
2. Filtered for words containing only a-z characters (no umlauts or special characters other than dash)
3. Verified each word's base form against a comprehensive Finnish dictionary (https://github.com/hugovk/everyfinnishword)
4. Performed multi-stage content filtering:
   - Used an LLM to identify any potentially disturbing words for the use case
   - Applied morphological analysis (using Voikko, https://github.com/voikko) to also exclude inflected forms of problematic base words
   - Ran multiple passes with conservative thresholds to ensure thorough filtering

## License

Compiled by Jarno Elonen, Nov 2024

This work is released under CC0 1.0 Universal (CC0 1.0) Public Domain Dedication.

To the extent possible under law, all copyright and related or neighboring rights to this word list are waived. You can copy, modify, distribute and perform the work, even for commercial purposes, all without asking permission.

For more information: https://creativecommons.org/publicdomain/zero/1.0/
