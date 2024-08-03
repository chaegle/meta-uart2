Digi Embedded Yocto UART2 layer
============================================

This layer enables UART2 (pins 23 & 24) on the Raspberry Pi header of the ConnectCore 6UL 
SBC Express.

This layer depends on the following layers:

https://github.com/digi-embedded/meta-digi


Supported Platforms
-------------------

  * Digi ConnectCore 6UL SBC Express
    * This kit has been obsoleted and is no longer available for purchase 


Installation
------------
1. Install Digi Embedded Yocto distribution

    https://github.com/digi-embedded/dey-manifest#installing-digi-embedded-yocto

2. Clone the *meta-uart2* Yocto layers under the Digi Embedded Yocto source 
   directory.

        #> cd <DEY-INSTALLDIR>/sources
        #> git clone git://githubcom/chaegle/meta-uart2.git -b kirkstone 


Create and build a project
--------------------------

We will use a ConnectCore 6UL SBC Express. This module has an expansion
connector that makes connecting Pi Hats possible.

1. Create a project for ConnectCore 6UL SBC Express

   #> mkdir <project-dir>
   #> cd <project-dir>
   #> . <DEY-INSTALLDIR>/mkproject.sh -p ccimx6ulstarter

2. Add the *meta-uart2* layer to the project's
  *bblayers.conf* configuration file

   #> vi <project-dir>/conf/bblayers.conf

   <DEY-INSTALLDIR>/sources/meta-uart2

3. Build the image

   #> bitbake core-image-base

4. Deploy image 


License
-------

INSERT APPROPRIATE LICENSE STATEMENT HERE
