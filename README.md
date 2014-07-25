Rescuecoin integration/staging tree
================================

http://www.rsc-coin.com

Copyright (c) 2009-2013 Bitcoin Developers
Copyright (c) 2011-2013 Litecoin Developers
Copyright (c) 2014 Rescuecoin Developers

What is Rescuecoin?
----------------

Rescuecoin is a 'faster' version of Litecoin which also uses scrypt.

 - 2.0 minute block targets
 - subsidy halves in 200k blocks (~4 years)
 - ~100 million total coins
 - 1 blocks to retarget difficulty

Other than that, this coin is exactly like Litecoin and should by no means be used as a real cryptocurrency. All of the coin parameters
are chosen arbitrarily or at most with 'fairness' towards everyone in mind.

License
-------

Rescue is released under the terms of the MIT license. See `COPYING` for more
information or see http://opensource.org/licenses/MIT.

Development process
-------------------

Developers work in their own trees, then submit pull requests when
they think their feature or bug fix is ready.

The patch will be accepted if there is broad consensus that it is a
good thing.  Developers should expect to rework and resubmit patches
if they don't match the project's coding conventions (see coding.txt)
or are controversial.

The master branch is regularly built and tested, but is not guaranteed
to be completely stable. Tags are regularly created to indicate new
official, stable release versions of Litecoin.

Feature branches are created when there are major new features being
worked on by several people.

Testing
-------

Testing and code review is the bottleneck for development; we get more pull
requests than we can review and test. Please be patient and help out, and
remember this is a security-critical project where any mistake might cost people
lots of money.

### Automated Testing

Developers are strongly encouraged to write unit tests for new code, and to
submit new unit tests for old code.

Unit tests for the core code are in `src/test/`. To compile and run them:

    cd src; make -f makefile.unix test

Unit tests for the GUI code are in `src/qt/test/`. To compile and run them:

    qmake BITCOIN_QT_TEST=1 -o Makefile.test bitcoin-qt.pro
    make -f Makefile.test
    ./rescuecoin-qt_test

