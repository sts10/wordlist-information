# Wordlist information 

This readme file contains information about word lists commonly used to generate passphrases. 

Copies of the word lists are included in this repository, but when possible, please get word lists from their original sources, as the ones included here are likely outdated.

The information printed below was generated using a tool called [Tidy](https://github.com/sts10/tidy) (version 0.2.91) by running `tidy -AAAA --samples <wordlist-file>`.

See below for an explanation of some of the attributes listed.

## Word list comparison

See [wordlists-stats-level-4.csv](./wordlist-stats-level-4.csv) for a comparison of many word lists.

## Word list sources

- [1Password's word list](https://github.com/1Password/spg/blob/master/testdata/agwordlist.txt)
- [BIPS0039 English list](https://github.com/bitcoin/bips/blob/master/bip-0039/english.txt)
- [Diceware (Beale)](https://theworld.com/~reinhold/beale.wordlist.asc)
- [EFF Short list with unique prefixes](https://www.eff.org/files/2016/09/08/eff_short_wordlist_2_0.txt)
- [EFF general short list](https://www.eff.org/files/2016/09/08/eff_short_wordlist_1.txt).
- [EFF long list](https://www.eff.org/deeplinks/2016/07/new-wordlists-random-passphrases)
- [Eyeware](https://github.com/celskeggs/eyeware/blob/master/eyeware8k)
- [Jack Singleton Diceware](https://github.com/jacksingleton/diceware/blob/master/diceware.txt)
- [KeePassXC's word list](https://github.com/keepassxreboot/keepassxc/blob/develop/share/wordlists/eff_large.wordlist)
- [Mnemonicode word list (v 0.7)](https://github.com/schollz/mnemonicode/blob/master/word_list.go).
- [Monero English word list](https://github.com/monero-project/monero/blob/master/src/mnemonics/english.h).
- [NSA RandPassGen list](https://github.com/nsacyber/RandPassGenerator/blob/master/RandPassGenerator/data/wordlist.txt)
- [Orchard Street Long List](https://github.com/sts10/orchard-street-wordlists/blob/main/lists/orchard-street-long.txt) (v0.1.4)
- [Orchard Street Medium List](https://github.com/sts10/orchard-street-wordlists/blob/main/lists/orchard-street-medium.txt) (v0.1.4)
- [PGP Wordlist](https://github.com/magic-wormhole/magic-wormhole/blob/master/src/wormhole/_wordlist.py). See also: [https://en.wikipedia.org/wiki/PGP_Words](https://en.wikipedia.org/wiki/PGP_Words).
- [Passplum Proposed](https://github.com/atoponce/passplum/blob/master/packages/web/example-seed-data.json)
- [Pokerware Formal](https://github.com/skeeto/pokerware/blob/master/words-formal.txt)
- [Pokerware Slang](https://github.com/skeeto/pokerware/blob/master/words-slang.txt)
- [Reinhold 8k](https://theworld.com/~reinhold/diceware8k.txt)
- [Reinhold's original diceware list](https://theworld.com/%7Ereinhold/diceware.wordlist.asc)
- [S/KEY](https://tools.ietf.org/html/rfc2289#page-4-19)
- [SecureDrop](https://github.com/freedomofpress/securedrop/blob/develop/securedrop/wordlists/en.txt)
- [Uli Fouquet Diceware](https://github.com/ulif/diceware/blob/master/diceware/wordlists/wordlist_en_securedrop.asc)
- [Webplaces 10k Short](http://www.webplaces.org/passwords/lists/10k-word-list-short.txt)
- [Webplaces 4k Hexadecimal](http://www.webplaces.org/passwords/lists/hexadecimal-4096-list.txt)
- [Webplaces Combined Diceware](http://www.webplaces.org/passwords/lists/Diceware-Combined-7776.txt)
- [Webplaces Improved Diceware](http://www.webplaces.org/passwords/lists/Diceware-Improved-7776.txt)

---

## Licensing

Refer to LICENSE file for how this readme file and all CSV files are licensed. 

Please refer to the license of each word list before use.

Any and all Orchard Street Wordlists are licensed under the [Creative Commons Attribution-ShareAlike 3.0 Unported License](http://creativecommons.org/licenses/by-sa/3.0/).


## Explanation of some of the list attributes in spreadsheet

Note: See [Tidy documentation](https://github.com/sts10/tidy#list-attributes) for more information.

### Understanding the relationship between word list length and passphrase entropy

The more word a word list has, the "stronger" the passphrases created from will be. 

For example, each word from a 7,776-word list adds 12.925 bits of entropy to a passphrase. A 3-word passphrase from such a list will have 38.775 bits of entropy (3 * 12.925). A 6-word passphrase from the same list will have 77.55 bits of entropy (6 * 12.925).

The chart below shows how many words from different list-lengths are required to hit minimum entropy requirements (starting at 55 bits of entropy).

| Min entropy  | 4,000 words | 7,776 words | 8,000 words |17,576 words|
| ------------ | ----------- | ----------- | ----------- | ----------- |
| 55 bits      | 5 words     | 5 words     | 5 words     | 4 words
| 60 bits      | 6 words     | 5 words     | 5 words     | 5 words
| 65 bits      | 6 words     | 6 words     | 6 words     | 5 words
| 70 bits      | 6 words     | 6 words     | 6 words     | 5 words
| 75 bits      | 7 words     | 6 words     | 6 words     | 6 words
| 80 bits      | 7 words     | 7 words     | 7 words     | 6 words

### Prefix codes, suffix codes, and uniquely decodable codes

If a word list is **uniquely decodable** that means that words from the list can be safely combined without a delimiter between each word, e.g. `enticingneurosistriflecubeshiningdupe`.

As a brief example, if a list has "boy", "hood", and "boyhood" on it, users who specified they wanted two words worth of randomness (entropy) might end up with "boyhood", which an attacker guessing single words would try. Removing the word "boy", which makes the remaining list uniquely decodable, prevents this possibility from occurring.

My understanding is that a good way to determine if a given word list in uniquely decodable or not is to use [the Sardinas–Patterson algorithm](https://en.wikipedia.org/wiki/Sardinas%E2%80%93Patterson_algorithm). This is [how Tidy determines if a word list is uniquely decodable](https://github.com/sts10/tidy/blob/main/src/display_information/uniquely_decodable.rs) and the result of that code is printed next to the label "Uniquely decodable?" in the word information above.

Removing all [prefix words](https://en.wikipedia.org/wiki/Prefix_code) (or all suffix words) is one way to make a list uniquely decodable, but I contest it is not the only way, nor usually the most efficient. I adapted the Sardinas-Patterson algorithm to create, what I believe, is a more efficient method for making a word list uniquely decodable. I used this method to make all of the [Orchard Street Wordlists](https://github.com/sts10/orchard-street-wordlists) uniquely decodable. You can learn more about uniquely decodable codes and Schlinkert pruning from [this blog post](https://sts10.github.io/2022/08/12/efficiently-pruning-until-uniquely-decodable.html).

### On maximum shared prefix length

If a word list's maximum shared prefix length is 4, that means that knowing the first 4 characters of any word on the generated list is sufficient to know which word it is.

On this hypothetical list, we'd know that if a word starts with "radi", we know it must be the word "radius" (if "radical" had been on the list, Tidy would have removed it).

This is useful if you intend the list to be used by software that uses auto-complete. For example, a user will only have to type the first 4 characters of any word before a program could successfully auto-complete the entire word.

### What is "Efficiency per character" and "Assumed entropy per char" and what's the difference?

If we take the entropy per word from a list (log<sub>2</sub>(list_length)) and divide it by the **average** word length of words on the list, we get a value we might call "efficiency per character". This just means that, on average, you get _E_ bits per character typed.

If we take the entropy per word from a list (log<sub>2</sub>(list_length)) and divide it by the length of the **shortest** word on the list, we get a value we might call "assumed entropy per char" (or character).

For example, if we're looking at the EFF long list, we see that it is 7,776-words long, so we'd assume an entropy of log<sub>2</sub>7776 or 12.925 bits per word. The average word length is 7.0, so the efficiency is 1.8 bits per character. (I got this definition of "efficiency" from [an EFF blog post about their list](https://www.eff.org/deeplinks/2016/07/new-wordlists-random-passphrases).) And lastly, the shortest word on the list is three letters long, so we'd divide 12.925 by 3 and get an "assumed entropy per character" of about 4.31 bits per character.

I contend that this "assumed entropy per character" value in particular may be useful when we ask the more theoretical question of "how short should the shortest word on a good word list should be?" There may be an established method for determining what this minimum word length should be, but if there is I don't know about it yet! Here's the math I've worked out on my own.

### The "brute force line"

Assuming the list is comprised of 26 unique characters, if the shortest word on a word list is shorter than log<sub>26</sub>(list_length), there's a possibility that a user generates a passphrase such that the formula of entropy_per_word = log<sub>2</sub>(list_length) will _overestimate_ the entropy per word. This is because a brute-force character attack would have fewer guesses to run through than the number of guesses we'd assume given the word list we used to create the passphrase.

As an example, let's say we had a 10,000-word list that contained the one-character word "a" on it. Given that it's 10,000 words, we'd expect each word to add an additional ~13.28 bits of entropy. That would mean a three-word passphrase would give users 39.86 bits of entropy. However! If a user happened to get "a-a-a" as their passphrase, a brute force method shows that entropy to be only 14.10 bits (4.7 \* 3 words). Thus we can say that it falls below the "brute force line", a phrase I made up.

To see if a given generated list falls above or below this line, use the `-A`/`--attributes` flag.

#### Maximum word list lengths to clear the Brute Force Line

Formula:

Where _S_ is the length of the shortest word on the list, 26 is the number of letters in the English alphabet, and _M_ is max list length: _M_ = 2<sup>_S_ * log<sub>2</sub>(26)</sup>. Conveniently, [this simplifies rather nicely](https://github.com/sts10/tidy/issues/9#issuecomment-1216003299) to _M_ = 26<sup>_S_</sup>.

(or in Python: `max_word_list_length = 26**shortest_word_length`)

| shortest word length | max list length |
|----------------------|-----------------|
| 2                    | 676             |
| 3                    | 17576           |
| 4                    | 456976          |
| 5                    | 11881376        |
