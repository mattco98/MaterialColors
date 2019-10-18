# matlab-material-colors

This library provides access to the Material UI Color Palette with a simple API, as well as a general Color object.

## Examples

The color constructor accepts a variable numbers of arguments, supporting a couple different formats:

- A single string argument representing a hex number of 3 or 4 colors. E.g.: '#FFA425', 'fF8bC2', '#81FD9155'. Note that the hash is optional.
- A single vector of length 3 or 4, representing rgb or rgba colors, respectively. The range of the values is [0, 255].
- Three floats representing RGB, respectively, in the range [0, 255]
- Four floats representing RGBA, respectively, in the range [0, 255]

```matlab
>> Color(255, 150, 150)

ans =

  Color with properties:

    r: 255
    g: 150
    b: 150
    a: 255
```

```matlab
>> Color(255, 150, 150, 100)

ans =

  Color with properties:

    r: 255
    g: 150
    b: 150
    a: 100
```

```matlab
>> Color('#FFa24d98')

ans =

  Color with properties:

    r: 255
    g: 162
    b: 77
    a: 152
```

The following color formats are supported by the Color class:

- rgb(a)
- cmyk
- hsl(a)
- hsv(a)

```matlab
>> Color(255, 150, 150, 100).rgb()

ans =

    1.0000    0.5882    0.5882
```

```matlab
>> Color(255, 150, 150, 100).rgba()

ans =

    1.0000    0.5882    0.5882    0.3922
```

```matlab
>> Color(255, 150, 150, 100).cmyk()

ans =

         0    0.4118    0.4118         0
```

```matlab
>> Color(255, 150, 150, 100).hsl()

ans =

         0    1.0000    0.7941
```

```matlab
>> Color(255, 150, 150, 100).hsla()

ans =

         0    1.0000    0.7941    0.3922
```

```matlab
>> Color(255, 150, 150, 100).hsv()

ans =

         0    0.4118    1.0000
```

```matlab
>> Color(255, 150, 150, 100).hsva()

ans =

         0    0.4118    1.0000    0.3922
```

## Material Colors examples

```matlab
>> MaterialColors.red(400)

ans =

  Color with properties:

    r: 239
    g: 83
    b: 80
    a: 255
```

Colors:

- red
- pink
- purple
- deepPurple
- indigo
- blue
- lightBlue
- cyan
- teal
- green
- lightGreen
- lime
- yellow
- amber
- orange
- deepOrange
- brown
- gray (or grey)
- blueGray (or blueGrey)

Variants:

- 50
- 100
- 200
- 300
- 400
- 500
- 600
- 700
- 800
- 900
