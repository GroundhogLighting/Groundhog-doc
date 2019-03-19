# List of Labels

As you might have read, it is very important for Groundhog to know if a surface is a Workplane, an Illum, a Window or other things. This is because, depending on what they are, they they will be exported in different ways. For example, you do not want a Workplane \(which is meant to be a plane in space where you want to calculate different values\) to be exported as a real surface that will be actually seen in your renders.

## Face \(surface\) Labels

### Windows

Even though it is not necessary to identify windows as "special elements" when we want to make a render, there are some other cases where it is very convenient to export them separately. In order to achieve this identification, Groundhog can internally tell \(from its Label\) if a surface is a window or not, and export it separately.

```text
if Labeler.window?(face) then
    #face is a window
else
    #face is not a window
end
```

### Workplanes

Workplanes are planes of the space where we would like to measure the illuminance or luminance levels. Even though in a Groundhog-created SketchUp model the workplanes will be represented as a \(semi-transparent red\) surface, it will be exported as a sensor grid in a file that represent such sensors in a format that can be used with Radiance's [RCONTRIB](http://www.radiance-online.org/learning/documentation/manual-pages/pdfs/rcontrib.pdf) and [RTRACE](http://www.radiance-online.org/learning/documentation/manual-pages/pdfs/rtrace.pdf) programs.

```text
if Labeler.workplane?(face) then
    #face is a workplane
else
    #face is not a workplane
end
```

### Illum surfaces

On an e-mail conversation, Greg Ward helped me define illum surfaces as:

> Illum surfaces, also known as "impostors" or "proxies," are light-emitting surfaces whose luminous distributions are equivalent to the distribution transmitted through them as the consequence of the existence of other \(direct and indirect\) light sources. [Mkillum](http://www.radiance-online.org/learning/documentation/manual-pages/pdfs/mkillum.pdf) is the program that allows creating illum surfaces in a convenient way [\(Ward & Shakespeare, 1998\).](http://radsite.lbl.gov/radiance/book/)For example, the daylight distribution transmitted through a window, which can be considered a consequence of the existence of the sun and sky, can be summarized into an illum surface.

Illum surfaces may be very useful when rendering and modeling luminaires in detail. Personally, I am not good at either of those, but I thought it was useful to include this feature in Groundhog.

Strictly speaking, these surfaces are not yet illum surfaces. They are exported without any Radiance modifier \("void"\), so they are invisible, and are supposed to be used for creating illums by running mkIllum program in order to create the actual illum.

```text
if Labeler.illum?(face) then
    #illum is a workplane
else
    #illum is not a workplane
end
```

**NOTE:** Every time the "Make Window" tool is used, an illum surface is created at the interior side of the wall, represented in a semi-transparent green.

### Result Pixel

When results are imported back to SketchUp using Groundhog, a new SketchUp group is created, which contains several rectangles that are colored in such way that they create a heatmap. Each of such pixels is labeled as a "result\_pixel".

```text
if Labeler.result_pixel?(face) then
    #illum is a result_pixel
else
    #illum is not a result_pixel
end
```

### Unlabeled surfaces

The rest of the surfaces are the not-labeled surfaces of the scene. They will be exported in radiance geometry files separated by layers.

## Definition Labels

### Solved workplanes

When results are imported back to SketchUp using Groundhog, a number of squares \(result pixels\) will be packed in a group. Such group will be labeled as a Solved Workplane

```text
if Labeler.solved_workplane?(component_definition) then
    #component_definition is a solved_workplane
else
    #component_definition is not a solved_workplane
end
```

### Local luminaire

A component may labeled as Local luminaire, which means that such component has been linked with an IES file that is within the computer.

```text
if Labeler.local_luminaire?(component_definition) then
    #component_definition is a local_luminaire
else
    #component_definition is not a local_luminaire
end
```

## Groups

### Tubular Daylight Devices \(TDD\)

A group may labeled as Tubular Daylight Device, which means that it will be exported accordingly for simulation and workaround \(TDDs are not easy to simulate using ray-tracing\)

```text
if Labeler.tdd?(group) then
    #group is a TDD
else
    #Group is not a TDD
end
```

## Material Labels

### Local materials

Local materials are SketchUp materials that contain their Radiance string definition \(i.e. primitive, modifier and arguments\) stored their "value"

```text
if Labeler.local_material?(material) then
    #material is a local_material
else
    #material is not a local_material
end
```

