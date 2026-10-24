# Third-party notices

PC Center's packaged Windows build contains or is produced with the following
open-source components:

| Component | Version | License |
| --- | ---: | --- |
| Python | 3.12 | Python Software Foundation License |
| pywebview | 6.2.1 | BSD 3-Clause |
| pywin32 | 312 | PSF and component-specific BSD-style licenses |
| Python.NET | 3.1.0 | MIT |
| clr-loader | 0.3.1 | MIT |
| Bottle | 0.13.4 | MIT |
| proxy-tools | 0.1.0 | MIT |
| typing-extensions | 4.16.0 | PSF-2.0 |
| cffi | 2.1.1 | MIT |
| pycparser | 3.0 | BSD-3-Clause |
| PyInstaller bootloader | 6.22.2 | GPL-2.0-or-later with the PyInstaller bootloader exception |
| Nuitka runtime | 4.3.1 | AGPL-3.0 with Nuitka Runtime Library Exception 1.0 |
| javascript-obfuscator (local build tool) | 5.9.0 | BSD-2-Clause |
| html-minifier-terser (local build tool) | 7.2.0 | MIT |
| Inno Setup | 6.7.3 | Inno Setup License |

The complete license metadata for these packages is distributed by each
package and is available from its official Python Package Index project page.
These components remain the property of their respective copyright holders.

The cffi and pycparser license texts are bundled in `licenses/`, with the installer and in this repository.

PC Center dynamically calls the NVIDIA Management Library supplied with the
user's installed NVIDIA display driver. PC Center does not redistribute
`nvml.dll`.

## NVIDIA Management Library API notice

Copyright 1993-2026 NVIDIA Corporation. All rights reserved.

This source code is subject to NVIDIA ownership rights under U.S. and
international copyright laws. Users and possessors of this source code are
granted a nonexclusive, royalty-free license to use this code in individual
and commercial software.

NVIDIA makes no representation about the suitability of this source code for
any purpose. It is provided "as is" without express or implied warranty of any
kind. NVIDIA disclaims all warranties with regard to this source code,
including all implied warranties of merchantability, noninfringement, and
fitness for a particular purpose. In no event shall NVIDIA be liable for any
special, indirect, incidental, or consequential damages, or any damages
whatsoever resulting from loss of use, data, or profits, whether in an action
of contract, negligence, or other tortious action, arising out of or in
connection with the use or performance of this source code.

U.S. Government End Users: this source code is a "commercial item" as that
term is defined at 48 C.F.R. 2.101 (OCT 1995), consisting of "commercial
computer software" and "commercial computer software documentation" as those
terms are used in 48 C.F.R. 12.212 (SEPT 1995), and is provided to the U.S.
Government only as a commercial end item. Consistent with 48 C.F.R. 12.212 and
48 C.F.R. 227.7202-1 through 227.7202-4 (JUNE 1995), all U.S. Government End
Users acquire the source code with only those rights set forth herein.

NVIDIA and related product names are trademarks or registered trademarks of
NVIDIA Corporation. PC Center is an independent project and is not affiliated
with or endorsed by NVIDIA Corporation.

## AMD ADLX interoperability notice

On AMD systems, PC Center dynamically calls the ADLX runtime supplied with the
installed AMD display driver. PC Center does not redistribute the ADLX SDK,
ADLX helper or sample source, or `amdadlx64.dll`.

AMD, Radeon, and related product names are trademarks of Advanced Micro
Devices, Inc. PC Center is an independent project and is not affiliated with
or endorsed by AMD.

## Lucide icons

PC Center uses Lucide SVG icons, pinned to commit `500620a2e8123f8d1db191538886dc0c223f69a9` of https://github.com/lucide-icons/lucide. The full license and copyright notices are included in `licenses/Lucide-LICENSE.txt` in this repository and `ui/vendor/lucide/LICENSE.txt` in the application. Icons are bundled locally; no icon service is contacted at runtime.

## Microsoft WebView2

The Windows interface uses Microsoft WebView2 SDK assemblies and loader
libraries distributed with pywebview. The GitHub installer requires the Microsoft WebView2 Runtime to be installed separately if it is missing. These Microsoft components are not
PC Center source code and remain subject to their applicable Microsoft terms.
The shared runtime has its own servicing and update behavior.

Official distribution information:
https://learn.microsoft.com/en-us/microsoft-edge/webview2/concepts/distribution
Microsoft privacy information: https://privacy.microsoft.com/privacystatement

## Native compilation and interface packaging

The executable includes Nuitka runtime code under its Runtime Library Exception.
The compiler itself is not distributed. JavaScript obfuscation runs locally at
build time. Full Nuitka license, exception and notice files, and the JavaScript
obfuscator license, are included in `licenses/`. These licenses do not change the
license of PC Center's independent application code.
