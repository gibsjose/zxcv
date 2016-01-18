# zxcv
Show password strength statistics using the `zxcvbn` library.

## Installation
First grab the `zxcvbn-py3` and `docopts` modules:
```bash
pip3 install zxcvbn-py3 docopts
```

Then install using Homebrew:
```bash
brew tap gibsjose/crypto
brew install zxcv
```

## Usage
```bash
zxcv <password>
```

For example, checking the strength of the password `p4$$w0rd123*!@#` gives:
```bash
$ zxcv 'p4$$w0rd123*!@#'
Entropy: 21.709 bits
Crack Time: 4 minutes (171.396s)
Score: ██░░░░░░ [2/8]
Calculation Time: 0.0026421546936035156ms
```

A stronger example with a randomly generated password such as `cHuBoL^xHicph87U?L`  gives:
```bash
$ zxcv 'cHuBoL^xHicph87U?L'
Entropy: 100.21 bits
Crack Time: centuries (7.330376325397945e+25s)
Score: ████████ [8/8]
Calculation Time: 0.0011339187622070312ms
```

`zxcvbn` takes into account various word lists, keyboard layouts, character patterns, etc. to give a more comprehensive view of a password's 'strength'. See the [`zxcvbn` page](https://github.com/dropbox/zxcvbn) and their great [blog post](https://blogs.dropbox.com/tech/2012/04/zxcvbn-realistic-password-strength-estimation/) for the development and reasoning behind how `zxcvbn` works.

## Caveats
Terminals that do not support Unicode (UTF-8) characters may not display the score bar correctly.
