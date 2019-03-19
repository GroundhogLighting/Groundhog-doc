# History

The Groundhog Project started in 2013, with the purpose of accelerating the creation of Radiance models, and making it simpler to draw complex geometries.

At the beginning, Groundhog intended to integrate daylighting and energy performance simulations. After some time of development, Groundhog became a Daylighting tool. The integration of light and thermodynamics was left to tools like Sefaira, OpenStudio, etc.

## Development history

This just shows a little bit of how Groundhog has been growing and changing. It may be a bit inaccurate.

### Groundhog 1.0 \(in development\)

* version 0.9.4 moved the Workplane definitions to the model attributes
* version 0.9.3 moved the Objective definitions to the model attributes
* From 0.9.3 and on, the Groundhog version is stored in the model.
* "surface closing" algorithm \(used for transforming faces with holes into Radiance polygons\) changed... it does not modify the model anymore and is much faster.
* Several workplanes can now be grouped as a single space, allowing simpler models.
* Non-horizontal and non-planar \(mesh, cylinders\) workplanes are allowed now.
* The concept of Objective was integrated
* Bug fixing... first tests of Groundhog for educational purposes.
* Pipes were found to cause trouble in some machines... they were removed.
* Tubular daylight devices have been incorporated. This feature is still experimental.
* Static simulations can now be performed by using Daylight Coefficient approach.
* Weather files are now a part of the model, and are ported with it.
* The Design Assistant was developed, enhancing the User Interface a lot.
* UI is developed with JqueryUI
* Better integration of day and electric lighting
* Groundhog is not focused on Compliance... you define goals and try to accomplish them.

### Groundhog 0.9

* Integration of Artificial lighting \(validation and documentation has not been done\)
* Configuration is now automatically saved when closing the WebDialog.
* Terrain is automatically added according to the size of the model
* Groundhog now allows working with several metrics at the same time.
* Exporting illums and windows within groups and components is now working. Workplanes cannot be nested within groups or components.
* Thanks to NREL, we now ship Radiance with Groundhog
* Important bug fixing! now it seems to be stable on WINDOWS and MAC.

### Groundhog 0.8

* Add-on environment is initiated \(0.7.1\)
* Bug fixing and enhancements \(0.7.2\)
* Started the integration of Support Files. Now you can insert an Irradiance sensor.

### Groundhog 0.7

* Annual simulation is done by using simple DC method
* Simulation GUI incorporated
* Enhanced Configuration

### Groundhog 0.6

* Exporting distributions were unified into a unique one that places illums of each layer in a separate file and window groups in other files.
* Groups are now exported as if they were components.
* SketchUp 2015 is now considered the required SketchUp version
* Added a RIF file exporter to simplify rendering.
* Workplanes now need to be rectangular and have no holes.
* Importing results for visualizing them within SketchUp.
* The concept of "value" was incorporated.
* All tools, features and functions are now grouped under the same menu: Plugins \(extensions\) --&gt; Groundhog
* Local materials were introduced. These are materials that contain their whole Radiance definition as their value
* Eliminated duplicity of materials. Now the same material may be exported a number of times \(one for each component or group on which is used\), but every time with different names.
* Sky is exported separately
* Basic materials can now be created from within SketchUp… avoiding some post-processing.
* Bug fixing, testing on Windows and OSX.

### Groundhog 0.5

* The “show/hide” tools were moved from the Groundhog Toolbar to the View menu.
* The “Show Window Groups” tool was algo moved to the View Menu.
* It is now possible to export a model without saving it as well as saving it in a different directory.
* The “Add Workplane” tool was downgraded to a simple script. It is more comfortable since the user no longer has to write down the height of the Worplane. The Workplanes may be moved just as any other face.
* Added the “Label as workplane” Context Menu. The faces have to be horizontal.
* Window Groups and Workplanes require a name. This name will be used for exporting them.
* Components may now be exported. Even Nested components \(components within components\) seem to be working OK. Groups are trickier.

### Groundhog 0.4

* Groundhog seem to be working O.K. on SketchUp 2014
* Materials can be supported by \*.mat file stored on a directory... if not, they are guessed.
* Exporting groups and one-level components is supported \(components within components do not really work... needed?\)
* Wrapped "Make Window" and "Add Workplane" operations into one "Undo"... better and more comfortable.

### Groundhog 0.3

* Materials started to be supported, as well as SketchUp Components \(non of them is ready yet\).
* Although windows can still be grouped, the groups can´t be seen, since "materials" \(i.e. colors\) mean something now. We need to solve this.
* The project was completely reorganized, introducing classes… Then, it was published.

### Groundhog 0.2

* Change of paradigm. Groundhog intends to export well, for now. In the future we might simulate within SketchUp.
* Grouping of windows option was added, as well as showing them in different colors.
* "Winfo" and "SimFile" files do not exist any more.
* Groundhog is now an extension, that can be turned on or off inside SketchUp.

### Groundhog 0.1

* Project started by Germán Molina, Sergio Vera Ph.D and Waldo Bustamante, Ph.D.
* Exports into Radiance and 3phase method formats.
* Calculations have to be done from a "Window Information File" and a "Simulation File", using perl scripts outside SketchUp.
* Materials are not supported at all. The program exports a list of assigned modifiers, and they have to be filled by the user.
* Sensor location is done over the workplane... the location is shown by drawing two lines forming an X.
* Sensor location involves ray-casting... which is very inefficient.
* Materials are treated separated from CFS.
* Grouping windows was not yet supported.

