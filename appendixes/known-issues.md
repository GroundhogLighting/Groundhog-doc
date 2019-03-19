# Known issues

## Exporting problems

* Copying and pasting windows, walls, workplanes or any surface with a name will end in repeated names... that causes errors when exporting.
* TILT field in IES files \(for exporting luminaires\) does not work.

## Simulation problems

* Radiance multithreading is not supported on Windows
* Some windows users have had trouble assigning the Radiance path. I have been told that was solved as follows:
  1. Go to 'Control Panel' &gt; 'System' &gt; 'Advanced' &gt; 'Environmental Variables' and check if the Radiance PATH is correct. If not, fix it.
  2. Then input the PATH in the Groundhog Preferences menu as follows: **C:/Program Files \(x86\)/Radiance/bin**, that is, with "/" \(not "\"\) and without adding any program name.

## Creating materials problems

