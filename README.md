# Writing shell scripts
This repository contains shell scripts that checks for common problems:
- abuse of the passive voice,
- weasel words
- lexical illusions

These scripts are based on those available [here](matt.might.net).

# Usage
Each script can be run independently. It might probably more convenient to run them within your latex workflow.
Following, [Matt's suggestion](http://matt.might.net/articles/shell-scripts-for-passive-voice-weasel-words-duplicates/), I keep a local copy of the scripts in the bin/ directory of each paper's repository. Then, I add a make proof rule to Makefile:

# Check style:
proof:
        echo "weasel words: "
        sh bin/weasel *.tex
        echo
        echo "passive voice: "
        sh bin/passive *.tex
        echo
        echo "duplicates: "
        perl bin/dups *.tex
