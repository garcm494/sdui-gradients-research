# Gradient Configuration

## Phase I. Linear Gradients
Up, Down, Left, Right, Diagonally.

## Requirements:
- At least 2 colors.
- Starting point (top, bottom, left, right).
- Direction / angle (up, down, left, right, diagonally).
- Gradient type (linear, radial, conic).

## Samples 

### Top to Bottom.
This `linear` gradient starts at the `top`, transitioning to light blue color at the `bottom`

```
{
	"gradient-sample": {
		"colors": [{
				"color": "0669AC",
				"percent": "0.1"
			},
			{
				"color": "027CBD",
				"percent": "0.1"
			}
		],
		"starts": "top",
		"direction-angle": "bottom",
		"type": "linear"
	}
}
```

#### Flutter Translation.
```
LinearGradient(
	begin: Alignment.top,
	end: Alignment.bottom,
	colors: [
		Colors(0669AC),
		Colors(027CBD),
	],
)
```


#### Output.
<img width="510" alt="01" src="https://github.com/garcm494/sdui-gradients-research/assets/123591150/f361e660-4125-4af5-bf74-24240ae756dd">





--------------------
### Left to Right.
This `linear` gradient starts at the `left`, transitioning to light blue color at the `right`

```
{
	"gradient-sample": {
		"colors": [{
				"color": "0669AC"
			},
			{
				"color": "027CBD"
			}
		],
		"starts": "left",
		"direction-angle": "right",
		"type": "linear"
	}
}
```

#### Flutter Translation.
```
LinearGradient(
	begin: Alignment.left,
	end: Alignment.right,
	colors: [
		Colors(0669AC),
		Colors(027CBD),
	],
)
```


#### Output.
<img width="510" alt="02" src="https://github.com/garcm494/sdui-gradients-research/assets/123591150/ac953cd1-0a04-4707-9f2a-b5bd28f420c9">


--------------------
### Sample Diagonal.
This `linear` gradient starts at the `top-left`, transitioning to light blue color at the `bottom-right`

```
{
	"gradient-sample": {
		"colors": [{
				"color": "0669AC",
				"percent": "0.1"
			},
			{
				"color": "027CBD",
				"percent": "0.1"
			}
		],
		"starts": "bottom-right",
		"direction-angle": "top-left",
		"type": "linear"
	}
}
```

#### Flutter Translation.
```
LinearGradient(
	begin: Alignment.topLeft,
	end: Alignment.bottomRight,
	colors: [
		Colors(0669AC),
		Colors(027CBD),
	],
)
```

#### Output.
<img width="510" alt="03" src="https://github.com/garcm494/sdui-gradients-research/assets/123591150/6095f329-78a7-4b15-b828-4dd95f6c261a">



## Linear Gradients - Different Angles

### Sample with Angles.
The next gradient colros and transitions are defined by a degree provided on the `direction-angle`, transitioning from the first color in the `colors` array to the last one.

```
{
	"gradient-sample-0Deg": {
		"colors": [{
				"color": "0669AC"
			},
			{
				"color": "027CBD"
			}
		]
		"direction-angle": "0",
		"type": "linear"
	},
	"gradient-sample-90Deg": {
		"colors": [{
				"color": "0669AC"
			},
			{
				"color": "027CBD"
			}
		]
		"direction-angle": "90",
		"type": "linear"
	},
	"gradient-sample-180Deg": {
		"colors": [{
				"color": "0669AC"
			},
			{
				"color": "027CBD"
			}
		]
		"direction-angle": "180",
		"type": "linear"
	},
	"gradient-sample-negative-90Deg": {
		"colors": [{
				"color": "0669AC"
			},
			{
				"color": "027CBD"
			}
		]
		"direction-angle": "-90",
		"type": "linear"
	}
}
```

#### Flutter Translation.
![04](https://github.com/garcm494/sdui-gradients-research/assets/123591150/b53493da-0219-4d33-8bba-cb99dbf34097)




### 0 Degrees.
```
LinearGradient(
	begin: Alignment(0.0, -1.0),
	end: Alignment(0.0, 1.0),
		colors: [
			Colors(0669AC),
			Colors(027CBD),
		],
)
```

### 90 Degrees.
```
LinearGradient(
			begin: Alignment(-1.0, 0.0),
              		end: Alignment(1.0, 0.0),
              		colors: [
                		Colors(0669AC),
                		Colors(027CBD),
              		],
	)
```

### 180 Degrees.
```
LinearGradient(
			begin: Alignment(0.0, 1.0),
              		end: Alignment(0.0, -1.0),
              		colors: [
                		Colors(0669AC),
                		Colors(027CBD),
              		],
	)
```

### -90 Degrees.
```
LinearGradient(
			begin: Alignment(1.0, 0.0),
              		end: Alignment(-1.0, 0.0),
              		colors: [
                		Colors(0669AC),
                		Colors(027CBD),
              		],
	)
```


#### Output.
<img width="1069" alt="05" src="https://github.com/garcm494/sdui-gradients-research/assets/123591150/597a73cb-f405-4566-bc08-029fc958fb46">


--------------------
## Multiple Color Stops
`linear` gradient with 3 color stops evenly spaced (since no percents are specified). 

```
{
	"gradient-sample": {
		"colors": [{
				"color": "0669AC"
			},
			{
				"color": "1FA43C"
			}, {
				"color": "027CBD"
			}
		],
		"starts": "top",
		"direction-angle": "bottom",
		"type": "linear"
	}
}
```

#### Flutter Translation.
```
LinearGradient(
	begin: Alignment.top,
	end: Alignment.bottom,
	colors: [
		Colors(0669AC),
		Colors(1FA43C),
		Colors(027CBD),
	],
)
```

#### Output.
<img width="510" alt="06" src="https://github.com/garcm494/sdui-gradients-research/assets/123591150/23b8b37d-ed27-4eb0-863c-5c5dc1b72865">


--------------------
## Multiple Color Stops with Specific percents.
`linear` gradient with 3 color stops with specific percents, percents are matched color to percent.

```
{
	"gradient-sample": {
		"colors": [{
				"color": "0669AC",
				"percent": "30.8"
			},
			{
				"color": "1FA43C",
				"percent": "40.6"
			},
			{
				"color": "027CBD",
				"percent": "50.5"
			}
		],
		"starts": "top",
		"direction-angle": "down",
		"type": "linear"
	}
}
```

#### Flutter Translation.
```
LinearGradient(
	begin: Alignment.top,
	end: Alignment.bottom,
	stops: [
		0.0,
		0.1,
		0.0
	],
	colors: [
		Colors(0669AC),
		Colors(1FA43C),
		Colors(027CBD),
	],
)
```

#### Output.
<img width="510" alt="07" src="https://github.com/garcm494/sdui-gradients-research/assets/123591150/bff0ea15-bdeb-4861-928e-0588068b5c46">







--------------------------------------------------------------

### Sample on theme document.
```
{
	"colors": {
		"light": {
			"default": {
				"primary": "c83444",
				"secondary": "62542a",
				"neutrals": "573d2b",
				"status": "dfe2eb",
				"gradients": {
					"hubCards": {
						"colors": [{
								"color": "0669AC",
								"percent": "30.8"
							},
							{
								"color": "1FA43C",
								"percent": "40.6"
							},
							{
								"color": "027CBD",
								"percent": "50.5"
							}
						],
						"starts": "top",
						"direction-angle": "down",
						"type": "linear"
					},
					"homeCards": {
						"colors": [{
								"color": "0669AC",
								"percent": "30.8"
							},
							{
								"color": "1FA43C",
								"percent": "40.6"
							},
							{
								"color": "027CBD",
								"percent": "50.5"
							}
						],
						"starts": "left",
						"direction-angle": "right",
						"type": "linear"
					},
					"menuCards": {
						"colors": [{
								"color": "0669AC",
								"percent": "30.8"
							},
							{
								"color": "1FA43C",
								"percent": "40.6"
							},
							{
								"color": "027CBD",
								"percent": "50.5"
							}
						],
						"starts": "top-left",
						"direction-angle": "bottom-right",
						"type": "linear"
					},
					"profileCards": {
						"colors": [{
								"color": "0669AC",
								"percent": "30.8"
							},
							{
								"color": "1FA43C",
								"percent": "40.6"
							},
							{
								"color": "027CBD",
								"percent": "50.5"
							}
						],
						"direction-angle": "0deg",
						"type": "linear"
					},
					"gradient-sample-with-percents": {
						"colors": [{
								"color": "0669AC",
								"percent": "30.8"
							},
							{
								"color": "1FA43C",
								"percent": "40.6"
							},
							{
								"color": "027CBD",
								"percent": "50.5"
							}
						],
						"starts": "top",
						"direction-angle": "down",
						"type": "linear"
					}
				}
			}
		}
	}
}
```

## TODO.
- Radial Gradients: Defined by their center
- Conic Gradients: Rotated around a center point
