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

For example, checking the strength of the password `p4$$w0rd` gives:
```bash
$ zxcv 'p4$$w0rd'
Entropy: 1.585 bits
Crack Time: instant (0.0s)
Score: # (1)
Calculation Time: 0.00101113319397ms
```

A stronger example with a randomly generated password such as `cHuBoL^xHicph87U?L`  gives:
```bash
$ zxcv 'cHuBoL^xHicph87U?L'
Entropy: 100.21 bits
Crack Time: centuries (7.3303763254e+25s)
Score: ##### (5)
Calculation Time: 0.00177001953125ms
```

## Caveats
Terminals that do not support Unicode (UTF-8) characters may not display the score bar correctly.
