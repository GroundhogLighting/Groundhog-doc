# List of Values

Some surfaces in the models will actually contain values that may be useless for SketchUp but that may be very useful for Radiance.

Different kinds of entities will have different kinds of values, as is specified later.

The way of retrieving a value is the following:

```text
value=GH_Labeler.get_value(entity)
```

## Faces Values

### Result Pixel value

Every pixel, generated when Radiance results are imported back to SketchUp, contains its value within it. This allow updating the scale \(which will require modifying the color of the pixel\) and retrieving the value of a certain pixel for numeric analysis.

The value of a pixel is a Float.

```text
value=GH_Labeler.get_value(entity) # 'value' is a float
```

## Definition Values

### Solved Workplane value

A Solved Workplane is a group of Result Pixels, each of which has its own numeric value stored. The value of the Solved Workplane will be a JSON that will contain the Metric that the workplane is displaying, the workplane it corresponds to and statistics.

It should be noted that this value is added when drawing the pixels

```text
value=JSON.parse(GH_Labeler.get_value(entity)) # 'value' is a Hash
min = value["min"]
max = value["max"]
average = value["average"]
uniformity1 = value["min_over_average"]
uniformity2 = value["min_over_max"]
nsensors = value["nsensors"]
area = value["total_area"]
metric = value["metric"]
workplane = value["workplane"]
scale_min = value["scale_min"] #This is added or updated when updating pixel colors
scale_max = value["scale_max"] #This is added or updated when updating pixel colors
```

### Local luminaire Value

The value of the Local Luminaire is the path to the IES file linked to it.

## Material Values

### Local material values

Local materials are SketchUp materials that contain their Radiance string definition \(i.e. primitive, modifier and arguments\) stored their "value".

The value of these materials is stored as an array containing two strings: one is everything that is before the materials's name, and the second is everything that goes after the material's name.

```text
value=GH_Labeler.get_value(material) # 'value' is an array
material_full_string=value[0]+"\t"+"Material_Name"+"\n"+value[1]
```

