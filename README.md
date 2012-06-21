#README

Humblepie downloads game install files from the Humble Indie Bundle Releases

##Overview 

Humblepie is a bash script that will download [Humble Indie Bundle](https://www.humblebundle.com/) files and check the md5 sums. It will work with any Indie Humble Bundle.

##Usage

humblepie [options]

##Configuration

```
## Everything following the underbar ('_') is the bundle name. you may set it to whatever you like.
## Those are the names used for the -b <name> option.
## But the `hibkey_' prefix is mandatory for internal function.
hibkey_1="foobar"
hibkey_2="foobar"
hibkey_3="foobar"
hibkey_4="foobar"
hibkey_5="foobar"
hibkey_android1="foobar"
hibkey_android2="foobar"
hibkey_botanicula="foobar"
hibkey_frozenbyte="foobar"
hibkey_frozensynapse="foobar"
hibkey_introversion="foobar"
hibkey_mojang="foobar"
hibkey_voxatron="foobar"

## This is the download directory.
dir_hib="${HOME}/humbleindiebundle"

## And you may turn these on with a value of 1, off with 0.
## Setting them to 1 is the equivalent of using -cv when invoking humblepie.
check_md5=1
verbose=0
```

##Options

```
-b <name>
    Specify a bundle by name according to the config file; For example:
        hibkey_frozenbyte="0a1b2c3d" 
        humblepie -b frozenbyte

-c 
    Enable checking md5 hashes: DEFAULT=1

-C <path>
    Specify an alternate config file

-d <path>
    Specify a download directory. Overrides config option `hib_dir'.

-f <file>
    Specify a file to download without prompting; For example, to download Amnesia;
        humblepie -k 0a1b2c3d -f amnesia_tdd-1.2.1-3.sh

-h
    Print a usage message and exit

-k <key>
    Specify a key manually. Overrides -b.
    It is found at the end of your Humble Bundle download link:      
      https://www.humblebundle.com/downloads?key=<YOUR KEY>

-r
    Enable running as root for system-wide installs. *NOT RECOMMENDED*

-s <term>
    Specify a case-insensitive search to perform. Negates -g. For example:
        To search for all files containing the string `super' in your named bundle `hibkey_4':
        humblepie -b 4 -s super

-w
    Write out a default config file and exit

-v
    Enable verbose reporting for info, warnings, and errors.
```

##Contact

Email:  j.s.mcgee115@gmail.com
IRC:    irc.freenode.net/zendeavor

##Thanks

Credit to [meskarune](admin@doloresportalatin.info) for writing this initial README. No one does it like her.

Appreciation for Earnestly and gtmanfred for breaking this script often.

##Copyright

Copyright (c) 2012 Josh McGee
 
    Permission is hereby granted, free of charge, to any person obtaining a 
    copy of this software and associated documentation files (the "Software"),
    to deal in the Software without restriction, including without limitation 
    the rights to use, copy, modify, merge, publish, distribute, sublicense, 
    and/or sell copies of the Software, and to permit persons to whom the 
    Software is furnished to do so, subject to the following conditions:
    
    The above copyright notice and this permission notice shall be included in 
    all copies or substantial portions of the Software.
    
    THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR 
    IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, 
    FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL 
    THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER 
    LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING 
    FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER 
    DEALINGS IN THE SOFTWARE.
