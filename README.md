Simple command line utility to convert TP-Link modem/router backup config files from binary to XML and back:
- conf.bin ➡ decrypt, md5hash and uncompress ➡ conf.xml
- conf.xml ➡ compress, md5hash and encrypt ➡ conf.bin

*Should work for TP-Link models: TD-W8970, TD-W8980, TD-W9970, TD-W9980 (thanks d3dave), Archer VR900, C2, C20 and C60 (d3dave).*<br>
*May or may not work with other TP-Link modem/routers, newer firmwares.*


####License

````
MIT License

Copyright (c) 2022 Toxinum.

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
````

Router config link : http://192.168.0.1/cgi/conf.bin?

## Install Termux Commands
````bash
pkg update -y
pkg install git -y
pkg install python -y
git clone https://github.com/ITSN0B1T4/tplink
cd tplink
pip install -r requirements.txt
chmod +x tpdec.py
python tpdec.py [path] [output].xml
````

###Thanks
