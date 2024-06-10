HISE is a cross-platform open source audio application for building virtual instruments. It emphasizes on sampling, but includes some basic synthesis features for making hybrid instruments as well as audio effects. You can export the instruments as VST / AU / AAX plugins or as standalone application for Windows / macOS or iOS.


System requirements

Supported OS:

Windows 7+
OSX 10.7+
iOS 8.0+
Linux (tested on Ubuntu 16.04 LTS)
HISE is tested on Windows and OSX with the following hosts:

Cubase
Ableton Live
Logic
Reaper
Protools
REASON 10
FL Studio    
Presonus Studio One
                                   It supports x86 and x64 on Windows, altough the 64bit version is highly recommended (it uses memory mapping for accessing samples and because of the limitations of the 32bit memory address space it needs a slower fallback solution).

OSX

Clone this repository. It also includes the (slightly modified) JUCE source code, so it might take a while.

Extract the contents of tools/SDK/sdk.zip to tools/SDK. Your tools folder should now contain folders named ASIOSDK2.3 and VST3 SDK.

Install xcpretty, a formatter for xcode. You can install it from the terminal using the command sudo gem install xcpretty.

Open the Projucer (there are compiled versions for every supported OS in the tools/projucer subdirectory) and load the HISE project (either projects/standalone/HISE Standalone.jucer or project/plugin/HISE.jucer).

If you hit a permission issue when launching Projucer (or an error stating that Projucer is damaged) you need to open Security & Privacy and whitelist Projucer.
Click on "Save Project and open in IDE" to load the project in XCode.

Hit compile and wait...

HISE does not run natively on Apple Silicon and should be compiled for x86 on that platform. Projects exported from HISE will run natively on both x86 and Apple Silicon devices when built as universal binaries.
