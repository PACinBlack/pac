PAC in Black
===============

Getting started
---------------
First you must initialize a repository with our sources:

    repo init -u git://github.com/PACinBlack/android.git -b cm-10.1

Then sync it up (This will take a while, so get a cup of coffee and some snickers):

    repo sync


Building PAC in Black
------------------------

For building PAC in Black you must cd to the working directory.
Make sure you have your device tree sources, located on

    cd device/-manufacturer-/-device-

Now you can run our build script:

    ./build-pib.sh -device-

example:
    ./build-pib.sh urushi

You can also use a second parameter for syncing sources before building

    ./build-pib.sh -device- true


There are also a few parameters that you can use together with before mentioned:

* threads: Allows to choose a number of threads for syncing operation
* clean: Removes intermediates and output files

The usage is the same
    
    ./build-pib.sh -device- -parameters- true


Parameters will be considered false unless you set them to true

This will make a signed zip located on out/target/product/-device-.
