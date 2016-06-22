# ACES Container Reference Implementation #

This folder contains a reference implementation for an ACES container file 
writer intended to be used with the Academy Color Encoding System (ACES). 
The resulting file is compliant with the ACES container specification (SMPTE 
S2065-4). However, there are a few things that are not demonstrated by this 
reference implementation.

* Stereo channels
* EndOfFileFiller
* Arbitrary attributes and naming validations
* half type attributes
* keycode value validations


## Installation Prerequisites ##

__CMake__

CMake can be downloaded directly from www.cmake.org or use one of the commands 
below.

* Ubuntu

        $ sudo apt-get install cmake

* Redhat

        $ yum install cmake

* OS X

    * Install homebrew if not already installed
    
            $ ruby -e "$(curl -fsSL https://raw.github.com/mxcl/homebrew/go)"
                
    * Install Cmake
    
            $ brew install cmake         
             
## Installation ##

* OS X

    * Install homebrew if not already installed

            $ ruby -e "$(curl -fsSL https://raw.github.com/mxcl/homebrew/go)"
        
    * Install aces_container
    
            $ brew install aces_container  

		
        
* From Source

    From the root source directory:
    
        $ mkdir build && cd build
        $ cmake ..
        $ make
        $ sudo make install

    The default process will install ``libAcesContainer.so`` to ``/usr/local/lib``
    and a number of header files into ``/usr/local/include/aces``
    
    
		
               
* Windows 

	* x86	
	    
	    From the root source directory:

			$ mkdir build && cd build
			$ cmake .. -G "Visual Studio 10 2010"
			
		The Visual Studio solution files will be generated in ``.\build``. You can open ``*.sln`` project solution file to continue the building process. If succeed, the ``aces_container.dll`` should be in ``.\Debug`` and/or ``.\Release``. 
		
		
	* x64	
	    
	    From the root source directory:

			$ mkdir build && cd build
			$ cmake .. -G "Visual Studio 10 2010 Win64"
			
		The Visual Studio solution files will be generated in ``.\build``. You can open ``*.sln`` project solution file to continue the building process. If succeed, the ``aces_container.dll`` should be in ``.\Debug`` and/or ``.\Release``. 

	
	
	
## License ##

The ACES Container Reference Implementation is provided by the Academy under the
following terms and conditions:

Copyright © 2015 Academy of Motion Picture Arts and Sciences ("A.M.P.A.S.").
Portions contributed by others as indicated. All rights reserved.

A worldwide, royalty-free, non-exclusive right to copy, modify, create
derivatives, and use, in source and binary forms, is hereby granted, subject to
acceptance of this license. Performance of any of the aforementioned acts
indicates acceptance to be bound by the following terms and conditions:

* Copies of source code, in whole or in part, must retain the above copyright
notice, this list of conditions and the Disclaimer of Warranty.

* Use in binary form must retain the above copyright notice, this list of
conditions and the Disclaimer of Warranty in the documentation and/or other
materials provided with the distribution.

* Nothing in this license shall be deemed to grant any rights to trademarks,
copyrights, patents, trade secrets or any other intellectual property of
A.M.P.A.S. or any contributors, except as expressly stated herein.

* Neither the name "A.M.P.A.S." nor the name of any other contributors to this
software may be used to endorse or promote products derivative of or based on
this software without express prior written permission of A.M.P.A.S. or the
contributors, as appropriate.

This license shall be construed pursuant to the laws of the State of California, 
and any disputes related thereto shall be subject to the jurisdiction of the 
courts therein.

Disclaimer of Warranty: THIS SOFTWARE IS PROVIDED BY A.M.P.A.S. AND CONTRIBUTORS
"AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO,
THE IMPLIED WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE, AND
NON-INFRINGEMENT ARE DISCLAIMED. IN NO EVENT SHALL A.M.P.A.S., OR ANY
CONTRIBUTORS OR DISTRIBUTORS, BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL,
SPECIAL, EXEMPLARY, RESITUTIONARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT
LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR
PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF
LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE
OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF
ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.

WITHOUT LIMITING THE GENERALITY OF THE FOREGOING, THE ACADEMY SPECIFICALLY
DISCLAIMS ANY REPRESENTATIONS OR WARRANTIES WHATSOEVER RELATED TO PATENT OR
OTHER INTELLECTUAL PROPERTY RIGHTS IN THE ACES CONTAINER REFERENCE
IMPLEMENTATION, OR APPLICATIONS THEREOF, HELD BY PARTIES OTHER THAN A.M.P.A.S.,
WHETHER DISCLOSED OR UNDISCLOSED.

Where indicated source code derived from or provided courtesy of:

---

License Terms for the ACES Container Writer 

The ACES Container Writer is provided by Adobe Systems Incorporated under the 
following terms and conditions:

Copyright © 2015 Adobe Systems Incorporated ("Adobe"). All rights reserved.

A worldwide, royalty-free, non-exclusive right to copy, modify, create
derivatives, and use, in source and binary forms, is hereby granted, subject to
acceptance of this license. Performance of any of the aforementioned acts
indicates acceptance to be bound by the following terms and conditions:

* Copies of source code, in whole or in part, must retain the above copyright
notice, this list of conditions and the Disclaimer of Warranty.

* Use in binary form must retain the above copyright notice, this list of
conditions and the Disclaimer of Warranty in the documentation and/or other
materials provided with the distribution.

* Nothing in this license shall be deemed to grant any rights to trademarks,
copyrights, patents, trade secrets or any other intellectual property of Adobe
or any contributors, except as expressly stated herein.

* Neither the name "Adobe" nor the name of any other contributors to this
software may be used to endorse or promote products derivative of or based on
this software without express prior written permission of Adobe or the
contributors, as appropriate.

This license shall be construed pursuant to the laws of the State of California,
and any disputes related thereto shall be subject to the jurisdiction of the
courts therein.

Disclaimer of Warranty: THIS SOFTWARE IS PROVIDED BY ADOBE AND CONTRIBUTORS "AS
IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE
IMPLIED WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE, AND
NON-INFRINGEMENT ARE DISCLAIMED. IN NO EVENT SHALL ADOBE, OR ANY CONTRIBUTORS OR
DISTRIBUTORS, BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL,
EXEMPLARY, RESITUTIONARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED
TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS;
OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER
IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE)
ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE
POSSIBILITY OF SUCH DAMAGE.

WITHOUT LIMITING THE GENERALITY OF THE FOREGOING, ADOBE SPECIFICALLY
DISCLAIMS ANY REPRESENTATIONS OR WARRANTIES WHATSOEVER RELATED TO PATENT OR
OTHER INTELLECTUAL PROPERTY RIGHTS IN ACES CONTAINER WRITER, OR
APPLICATIONS THEREOF, HELD BY PARTIES OTHER THAN ADOBE, WHETHER DISCLOSED OR
UNDISCLOSED.

---

MD5C.C - RSA Data Security, Inc., MD5 message-digest algorithm

Copyright (C) 1991-2, RSA Data Security, Inc. Created 1991. All rights reserved.

License to copy and use this software is granted provided that it is identified
as the "RSA Data Security, Inc. MD5 Message-Digest Algorithm" in all material
mentioning or referencing this software or this function.

License is also granted to make and use derivative works provided that such
works are identified as "derived from the RSA Data Security, Inc. MD5
Message-Digest Algorithm" in all material mentioning or referencing the derived
work.

RSA Data Security, Inc. makes no representations concerning either the
merchantability of this software or the suitability of this software for any
particular purpose. It is provided "as is" without express or implied warranty
of any kind.

These notices must be retained in any copies of any part of this documentation
and/or software.