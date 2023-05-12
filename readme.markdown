# Wordlist information 

This readme file contains information about word lists commonly used to generate passphrases. 

Copies of the word lists are included in this repository, but when possible, please get word lists from their original sources, as the ones included here are likely outdated.

The information printed below was generated using a tool called [Tidy](https://github.com/sts10/tidy) (version 0.2.91) by running `tidy -AAAA --samples <wordlist-file>`.

See below for an explanation of some of the attributes listed.

## EFF long list
[Source](https://www.eff.org/deeplinks/2016/07/new-wordlists-random-passphrases)

This list was designed to be used with physical dice. That said, many passphrase generators, [including Bitwarden's](https://github.com/bitwarden/clients/blob/master/libs/common/src/misc/wordlist.ts), use this word list. 

```text
List length               : 7776 words
Mean word length          : 6.99 characters
Length of shortest word   : 3 characters (aim)
Length of longest word    : 9 characters (zoologist)
Free of prefix words?     : true
Free of suffix words?     : false
Uniquely decodable?       : true
Entropy per word          : 12.925 bits
Efficiency per character  : 1.849 bits
Assumed entropy per char  : 4.308 bits
Above brute force line?   : true
Shortest edit distance    : 1
Mean edit distance        : 6.858
Longest shared prefix     : 8
Unique character prefix   : 9

Word samples
------------
habitat hatbox cramp unspoiled lazy image
gestation overplant bronzing delirious aspect sandlot
gangway manual preformed handstand caddy exciting
operate etching unhealthy mayday moonbeam unhappy
purist clay unlikable subsector perfected quote
```

## KeePassXC's word list 

This is the list that the [KeePassXC password manager](https://keepassxc.org/) will use by default ([source](https://github.com/keepassxreboot/keepassxc/blob/develop/share/wordlists/eff_large.wordlist)). Note: This list is very similar to the EFF long list.

```text
List length               : 7776 words
Mean word length          : 6.99 characters
Length of shortest word   : 3 characters (aim)
Length of longest word    : 10 characters (legitimate)
Free of prefix words?     : true
Free of suffix words?     : false
Uniquely decodable?       : true
Entropy per word          : 12.925 bits
Efficiency per character  : 1.848 bits
Assumed entropy per char  : 4.308 bits
Above brute force line?   : true
Shortest edit distance    : 1
Mean edit distance        : 6.859
Longest shared prefix     : 8
Unique character prefix   : 9

Word samples
------------
eloquent uninjured scrutiny snowdrift bonelike plaza
sandpaper pointy drier survive deplete clear
sugar splashed pounce vitamins wispy twisting
ice flattered wobbling diminish veggie snowless
subject stuffing spinning gallery reenter panhandle
```

## 1Password word list

Word list used by the [1Password password manager](https://1password.com/). 

Note that there are a few version of the 1Password word list on line, but they're all about 18,200 words. [Here's one version that's public](https://github.com/1Password/spg/blob/master/testdata/agwordlist.txt), and here's [another](https://1password.com/txt/agwordlist.txt). The list included here is just one of them.

```text
List length               : 18176 words
Mean word length          : 6.20 characters
Length of shortest word   : 3 characters (abe)
Length of longest word    : 8 characters (zwieback)
Free of prefix words?     : false
Free of suffix words?     : false
Uniquely decodable?       : false
Entropy per word          : 14.150 bits
Efficiency per character  : 2.283 bits
Assumed entropy per char  : 4.717 bits
Above brute force line?   : false
Shortest edit distance    : 1
Mean edit distance        : 6.168
Longest shared prefix     : 7
Unique character prefix   : 8

Word samples
------------
sprint budd fanciful roulette thymus distant
lily chowder nirvana heroes muleteer clincher
dialog why shallop coverall paisley ingather
grumble allay urgency stuffy been gammon
future mailbox palmate spark paddle hillock
```


## NSA RandPassGen List

[Source](https://github.com/nsacyber/RandPassGenerator/blob/master/RandPassGenerator/data/wordlist.txt).

```text
List length               : 117828 words
Mean word length          : 7.90 characters
Length of shortest word   : 2 characters (ad)
Length of longest word    : 21 characters (microminiaturizations)
Free of prefix words?     : false
Free of suffix words?     : false
Uniquely decodable?       : false
Entropy per word          : 16.846 bits
Efficiency per character  : 2.133 bits
Assumed entropy per char  : 8.423 bits
Above brute force line?   : false
Shortest edit distance    : 1
Longest shared prefix     : 20
Unique character prefix   : 21
```

## Reinhold Diceware list
[Source](https://theworld.com/%7Ereinhold/diceware.wordlist.asc). Note that the EFF long list was created to replace this list. I would recommend using that list instead of this one.
```text
List length               : 7776 words
Mean word length          : 4.24 characters
Length of shortest word   : 1 characters (-)
Length of longest word    : 6 characters (zurich)
Free of prefix words?     : false
Free of suffix words?     : false
Uniquely decodable?       : false
Entropy per word          : 12.925 bits
Efficiency per character  : 3.049 bits
Assumed entropy per char  : 12.925 bits
Above brute force line?   : false
Shortest edit distance    : 1
Mean edit distance        : 4.423
Longest shared prefix     : 5
Unique character prefix   : 6

Word samples
------------
shave visa page bloom cccc pill
chat eg bee sieve uw wonder
co hub gabon tell tore fade
boron fig rope tog peppy aster
lw wand fungi gala boom spurt
```

## Short word lists 

Some of these lists were/are designed such that each word is phonetically distinct, meaning they are good choices if passphrases are going to read aloud frequently. 

### EFF general short list
[Source](https://www.eff.org/files/2016/09/08/eff_short_wordlist_1.txt).
```text
List length               : 1296 words
Mean word length          : 4.54 characters
Length of shortest word   : 3 characters (aim)
Length of longest word    : 5 characters (zippy)
Free of prefix words?     : true
Free of suffix words?     : false
Uniquely decodable?       : true
Entropy per word          : 10.340 bits
Efficiency per character  : 2.277 bits
Assumed entropy per char  : 3.447 bits
Above brute force line?   : true
Shortest edit distance    : 1
Mean edit distance        : 4.367
Longest shared prefix     : 4
Unique character prefix   : 5

Word samples
------------
thank walk curse aide kick clay
slick good judge depth smile omen
duck stamp sandy crush self spew
ream desk dart blunt reset dock
baggy grief scoot zippy kung malt
```

### EFF Short list with unique prefixes

EFF's short word list (with words that have unique three-character prefixes). [EFF writes of this list](https://www.eff.org/deeplinks/2016/07/new-wordlists-random-passphrases):

> Each word has a unique three-character prefix. This means that future software could auto-complete words in the passphrase after the user has typed the first three characters.
>
> All words are at least an edit distance of 3 apart. This means that future software could correct any single typo in the user's passphrase (and in many cases more than one typo).

```text
List length               : 1296 words
Mean word length          : 7.32 characters
Length of shortest word   : 3 characters (cup)
Length of longest word    : 10 characters (wrongdoing)
Free of prefix words?     : true
Free of suffix words?     : false
Uniquely decodable?       : true
Entropy per word          : 10.340 bits
Efficiency per character  : 1.413 bits
Assumed entropy per char  : 3.447 bits
Above brute force line?   : true
Shortest edit distance    : 3
Mean edit distance        : 7.225
Longest shared prefix     : 2
Unique character prefix   : 3

Word samples
------------
atrocious borough ethics mustard myspace jelly
pucker sniff elliptical onlooker smartphone unusual
acetone cotton cucumber luscious saltshaker escalator
enquirer upholstery emoticon accountant pyramid padlock
clock enchilada luscious neither zucchini mousetrap
```

### Mnemonicode word list (v 0.7)

[Source](https://github.com/schollz/mnemonicode/blob/master/word_list.go).

```text
List length               : 1633 words
Mean word length          : 5.75 characters
Length of shortest word   : 3 characters (ego)
Length of longest word    : 7 characters (william)
Free of prefix words?     : true
Free of suffix words?     : false
Uniquely decodable?       : true
Entropy per word          : 10.673 bits
Efficiency per character  : 1.857 bits
Assumed entropy per char  : 3.558 bits
Above brute force line?   : true
Shortest edit distance    : 1
Mean edit distance        : 5.552
Longest shared prefix     : 6
Unique character prefix   : 7

Word samples
------------
pancake record bambino patent join lobster
studio falcon kermit erosion except andy
phrase judo tokyo family gate folio
road editor silver zoom canoe chant
spray telex cartoon radical inch rachel
```

### BIPS0039 English list

[Source](https://github.com/bitcoin/bips/blob/master/bip-0039/english.txt). Note that this short list contains the British spelling "artefact", which seems strange?

```text
List length               : 2048 words
Mean word length          : 5.40 characters
Length of shortest word   : 3 characters (act)
Length of longest word    : 8 characters (universe)
Free of prefix words?     : false
Free of suffix words?     : false
Uniquely decodable?       : false
Entropy per word          : 11.000 bits
Efficiency per character  : 2.035 bits
Assumed entropy per char  : 3.667 bits
Above brute force line?   : true
Shortest edit distance    : 1
Mean edit distance        : 5.386
Longest shared prefix     : 3
Unique character prefix   : 4

Word samples
------------
merit horse physical inmate cage solid
rate gather habit safe wire bar
medal chicken crunch weird dune gain
input february art city thank work
error laugh sand oak tuition inner
```

### Monero word list

[Source](https://github.com/monero-project/monero/blob/master/src/mnemonics/english.h).

```text
List length               : 1626 words
Mean word length          : 6.05 characters
Length of shortest word   : 4 characters (aces)
Length of longest word    : 12 characters (verification)
Free of prefix words?     : true
Free of suffix words?     : false
Uniquely decodable?       : true
Entropy per word          : 10.667 bits
Efficiency per character  : 1.762 bits
Assumed entropy per char  : 2.667 bits
Above brute force line?   : true
Shortest edit distance    : 1
Mean edit distance        : 6.004
Longest shared prefix     : 2
Unique character prefix   : 3

Word samples
------------
tipsy ensign governing tirade memoir upgrade
swept addicted lamb jaded talent zigzags
tufts gnome atlas lordship cinema eskimos
ungainly dogs zodiac maverick judge after
ravine orbit turnip dads ghost divers
```

### PGP Wordlist

[As appears in Magic Wormhole project](https://github.com/magic-wormhole/magic-wormhole/blob/master/src/wormhole/_wordlist.py). See also: [https://en.wikipedia.org/wiki/PGP_Words](https://en.wikipedia.org/wiki/PGP_Words).

```text
List length               : 512 words
Mean word length          : 7.65 characters
Length of shortest word   : 4 characters (acme)
Length of longest word    : 11 characters (stethoscope)
Free of prefix words?     : true
Free of suffix words?     : true
Uniquely decodable?       : true
Entropy per word          : 9.000 bits
Efficiency per character  : 1.176 bits
Assumed entropy per char  : 2.250 bits
Above brute force line?   : true
Shortest edit distance    : 2
Mean edit distance        : 7.411
Longest shared prefix     : 6
Unique character prefix   : 7

Word samples
------------
bedlamp Ohio proximate stormy revenue befriend
Orlando pioneer bombast travesty hemisphere stagnate
mural almighty dwelling infancy standard bifocals
outfielder rhythm specialist candidate processor treadmill
supportive infancy stupendous gremlin spaniel backwater
```

----


## [Orchard Street Medium List (v0.1.4)](https://github.com/sts10/orchard-street-wordlists/blob/ee46d29aad7a2e0a677b2ffd3a72034f2e2ecaf1/lists/orchard-street-medium.txt)

Self-promotion alert: I created this word list. This list is not included in this repository for licensing reasons. As the creator of this list, I can confidently recommend that if you want to use this list, head over to [GitHub repository](https://github.com/sts10/orchard-street-wordlists) and get the very latest version.

```text
List length               : 7776 words
Mean word length          : 7.05 characters
Length of shortest word   : 3 characters (add)
Length of longest word    : 10 characters (worthwhile)
Free of prefix words?     : false
Free of suffix words?     : false
Uniquely decodable?       : true
Entropy per word          : 12.925 bits
Efficiency per character  : 1.834 bits
Assumed entropy per char  : 4.308 bits
Above brute force line?   : true
Shortest edit distance    : 1
Mean edit distance        : 6.951
Longest shared prefix     : 9
Unique character prefix   : 10

Word samples
------------
novel sediment historical instance tubes widespread
exercise birds blamed sits plenty readiness
assuming burns matched monitor heavily reader
below interact taught breeding slid walked
connect sin owe slept agencies deeds
```

## [Orchard Street Long List (v0.1.4)](https://github.com/sts10/orchard-street-wordlists/blob/ee46d29aad7a2e0a677b2ffd3a72034f2e2ecaf1/lists/orchard-street-long.txt)

Self-promotion alert: I created this word list. This list is not included in this repository for licensing reasons. As the creator of this list, I can confidently recommend that if you want to use this list, head over to [GitHub repository](https://github.com/sts10/orchard-street-wordlists) and get the very latest version. 

```text
List length               : 17576 words
Mean word length          : 7.98 characters
Length of shortest word   : 3 characters (add)
Length of longest word    : 15 characters (troubleshooting)
Free of prefix words?     : false
Free of suffix words?     : false
Uniquely decodable?       : true
Entropy per word          : 14.101 bits
Efficiency per character  : 1.767 bits
Assumed entropy per char  : 4.700 bits
Above brute force line?   : true
Shortest edit distance    : 1
Mean edit distance        : 7.914
Longest shared prefix     : 14
Unique character prefix   : 15

Word samples
------------
unwarranted embodied professional achieved stupidity dye
conservation orange considerable estuary stripped remains
villagers cowardice destination detailed capacities intruder
dentists synthetic cannabis dignity bagel accession
ocean rooftop indifferent sometimes pamphlet thinkers
```

---

## Licensing

Refer to LICENSE file for how this readme file itself is licensed.

## Explanation of some of the list attributes printed above

Note: See [Tidy documentation](https://github.com/sts10/tidy#list-attributes) for more information.

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
