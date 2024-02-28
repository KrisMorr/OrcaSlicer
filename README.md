[![Build all](https://github.com/KrisMorr/OrcaSlicerRED/actions/workflows/build_all.yml/badge.svg?branch=main)](https://github.com/KrisMorr/OrcaSlicerRED/actions/workflows/build_all.yml)
# Orca SlicerRED    
![red z logo 2png](https://github.com/KrisMorr/OrcaSlicerRED/assets/154343071/78428ce7-4fd9-46ce-b7d6-15cfe710afaa)



# Download

### Stable Release
**[Download the Latest Stable Release](https://github.com/KrisMorr/OrcaSlicerRED/releases/latest)**  
Visit our GitHub Releases page for the latest stable version of Orca Slicer, recommended for most users.

### Nightly Builds
**[Download the Nightly Build](https://github.com/KrisMorr/OrcaSlicerRED/tags)**  
Explore the latest developments in Orca Slicer with our nightly builds. Feedback on these versions is highly appreciated.


# How to install
**Windows**: 
1.  Download the installer for your preferred version from the [releases page](https://github.com/KrisMorr/OrcaSlicerRED/releases).
    - *For convenience there is also a portable build available.*
    - *If you have troubles to run the build, you might need to install following runtimes:*
      - [MicrosoftEdgeWebView2RuntimeInstallerX64](https://github.com/SoftFever/OrcaSlicer/releases/download/v1.0.10-sf2/MicrosoftEdgeWebView2RuntimeInstallerX64.exe)
          - [Details of this runtime](https://aka.ms/webview2)
          - [Alternative Download Link Hosted by Microsoft](https://go.microsoft.com/fwlink/p/?LinkId=2124703)
      - [vcredist2019_x64](https://github.com/SoftFever/OrcaSlicer/releases/download/v1.0.10-sf2/vcredist2019_x64.exe)
          -  [Alternative Download Link Hosted by Microsoft](https://aka.ms/vs/17/release/vc_redist.x64.exe)
          -  This file may already be available on your computer if you've installed visual studio.  Check the following location: `%VCINSTALLDIR%Redist\MSVC\v142`
# How to install hms_xx.json - Windows

**Unzip the hms_xx_json.zip archive containing the hms_xx.json files into the "hms" directory within the configuration folder.**

These are files responsible for translating errors for Bambu Lab printers.

![folder konf win](https://github.com/KrisMorr/OrcaSlicerRED/assets/154343071/e4526d39-0c3c-4a7f-bc88-6805154d8eaf)

![katalogi](https://github.com/KrisMorr/OrcaSlicerRED/assets/154343071/bd49083b-1545-4595-8be0-bd4f767d5f62)



**Mac**:
1. Download the DMG for your computer: `arm64` version for Apple Silicon and `x86_64` for Intel CPU.  
2. Drag OrcaSlicer.app to Application folder. 
3. *If you want to run a build from a PR, you also need following instructions below*  
    <details quarantine>
    - Option 1 (You only need to do this once. After that the app can be opened normally.):
      - Step 1: Hold _cmd_ and right click the app, from the context menu choose **Open**.
      - Step 2: A warning window will pop up, click _Open_  
      
    - Option 2:  
      Execute this command in terminal: `xattr -dr com.apple.quarantine /Applications/OrcaSlicerRED.app`
      ```console
          softfever@mac:~$ xattr -dr com.apple.quarantine /Applications/OrcaSlicerRED.app
      ```
    - Option 3:  
        - Step 1: open the app, a warning window will pop up  
            ![image](./SoftFever_doc/mac_cant_open.png)  
        - Step 2: in `System Settings` -> `Privacy & Security`, click `Open Anyway`:  
            ![image](./SoftFever_doc/mac_security_setting.png)  
    </details>
 # How to install hms_xx.json - MAC   

**Unzip the hms_xx_json.zip archive containing the hms_xx.json files into the "hms" directory within the configuration folder.**

These are files responsible for translating errors for Bambu Lab printers.


# How to compile
- Windows 64-bit  
  - Tools needed: Visual Studio 2019, Cmake, git, Strawberry Perl.
      - You will require cmake version 3.14 or later, which is available [on their website](https://cmake.org/download/).
      - Strawberry Perl is [available on their github repository](https://github.com/StrawberryPerl/Perl-Dist-Strawberry/releases/).
  - Run `build_release.bat` in `x64 Native Tools Command Prompt for VS 2019`

- Mac 64-bit  
  - Tools needed: Xcode, Cmake, git, gettext, libtool, automake, autoconf, texinfo
      - You can install most of them by running `brew install cmake gettext libtool automake autoconf texinfo`
  - run `build_release_macos.sh`
  - To build and debug in XCode:
      - run `XCode.app`
      - open ``build_`arch`/OrcaSlicer.xcodeproj``
      - menu bar: Product => Scheme => OrcaSlicer
      - menu bar: Product => Scheme => Edit Scheme...
          - Run => Info tab => Build Configuration: `RelWithDebInfo`
          - Run => Options tab => Document Versions: uncheck `Allow debugging when browsing versions`
      - menu bar: Product => Run

- Ubuntu 
  - Dependencies **Will be auto installed with the shell script**: `libmspack-dev libgstreamerd-3-dev libsecret-1-dev libwebkit2gtk-4.0-dev libosmesa6-dev libssl-dev libcurl4-openssl-dev eglexternalplatform-dev libudev-dev libdbus-1-dev extra-cmake-modules libgtk2.0-dev libglew-dev libudev-dev libdbus-1-dev cmake git texinfo`
  - run 'sudo ./BuildLinux.sh -u'
  - run './BuildLinux.sh -dsir'


# Note: 
If you're running Klipper, it's recommended to add the following configuration to your `printer.cfg` file.
```
# Enable object exclusion
[exclude_object]

# Enable arcs support
[gcode_arcs]
resolution: 0.1
```

# Supports
**Orca Slicer** is an open-source project, and I'm deeply grateful to all my sponsors and backers.   
Their generous support enables me to purchase filaments and other essential 3D printing materials for the project.   
Thank you! :)

### Sponsors:  
<table>
<tr>
<td>
<a href="https://peopoly.net/">
    <img src="SoftFever_doc\sponsor_logos\peopoly-standard-logo.png" alt="Peopoly" width="64" height="">
</a>
</td> 
</tr>
<tr>
<td> </td>
</tr>
<tr>
<td>
<a href="https://qidi3d.com/">
    <img src="SoftFever_doc\sponsor_logos\QIDI.png" alt="QIDI" width="64" height="">
</a>
</td>
</tr>
</table>

### Backers:  
Ko-fi supporters: [Backers list](https://github.com/SoftFever/OrcaSlicer/wiki/OrcaSlicer-backers-%E2%80%90-28-Oct-2023)

Support me  
[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/G2G5IP3CP)

## Some background
OrcaSlicer is originaly forked from Bambu Studio, it was previously known as BambuStudio-SoftFever.

Bambu Studio is forked from [PrusaSlicer](https://github.com/prusa3d/PrusaSlicer) by Prusa Research, which is from [Slic3r](https://github.com/Slic3r/Slic3r) by Alessandro Ranellucci and the RepRap community. 
Orca Slicer incorporates a lot of features from SuperSlicer by @supermerill
Orca Slicer's logo is designed by community member Justin Levine(@freejstnalxndr)  


# License
Orca Slicer is licensed under the GNU Affero General Public License, version 3. Orca Slicer is based on Bambu Studio by BambuLab.

Bambu Studio is licensed under the GNU Affero General Public License, version 3. Bambu Studio is based on PrusaSlicer by PrusaResearch.

PrusaSlicer is licensed under the GNU Affero General Public License, version 3. PrusaSlicer is owned by Prusa Research. PrusaSlicer is originally based on Slic3r by Alessandro Ranellucci.

Slic3r is licensed under the GNU Affero General Public License, version 3. Slic3r was created by Alessandro Ranellucci with the help of many other contributors.

The GNU Affero General Public License, version 3 ensures that if you use any part of this software in any way (even behind a web server), your software must be released under the same license.

Orca Slicer includes a pressure advance calibration pattern test adapted from Andrew Ellis' generator, which is licensed under GNU General Public License, version 3. Ellis' generator is itself adapted from a generator developed by Sineos for Marlin, which is licensed under GNU General Public License, version 3.

The bambu networking plugin is based on non-free libraries from Bambulab. It is optional to the Orca Slicer and provides extended functionalities for Bambulab printer users.

