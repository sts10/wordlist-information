
# Tidy-Analyze

This is a shell script intended to run Tidy against 1 or more wordlists, and output
the results into a CSV which can then be crunched by Google Sheets (or whatever).

## Usage

- `./tidy-analyze level file [ file [ ... ] ]`
  - `level` - Should be 1 to 4.  Higher numbers are more detailed analysis.
    - Level 4 can take a *really* long time to run.  I warned ya.
  - `file` - 1 or more wordlist files.

Output is written to `wordlist-stats-level-[1-4].csv` depending on the level.
If the file does not exist, it is created with a header row.


## Example Run times

The times are with `lists/1password-2023.txt`:
- Level 1: Under 1s
- Level 2: 2s
- Level 3: 20s
- Level 4: 111s (1m51s)

## Reports

This script was run against the lists in `lists/` as well as [those in Strongbox](https://github.com/strongbox-password-safe/Strongbox/tree/master/resources/wordlists).  The results are in these files:

- [wordlist-stats-level-1.csv](./wordlist-stats-level-1.csv)
- [wordlist-stats-level-2.csv](./wordlist-stats-level-2.csv)
- [wordlist-stats-level-3.csv](./wordlist-stats-level-3.csv)

If spreadsheets are more to your liking, [here they are in Google Sheets](https://docs.google.com/spreadsheets/d/1hvEYdaYp4OxOgChnglDAlejIavBFdJuzWkvxlaDHxYQ/edit?usp=sharing).


