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
		"colors": ["0669AC", "027CBD"],
		"starts": "top",
		"direction-angle": "down",
		"type": "linear"
	}
}
```

#### Flutter Translation.
```
BoxDecoration(
	gradient: LinearGradient(
			begin: Alignment.top,
              		end: Alignment.bottom,
              		colors: [
                		Colors(0669AC),
                		Colors(027CBD),
              		],
	)
)
```


#### Output.
<img width="510" alt="Screenshot 2023-07-06 at 11 56 46 AM" src="https://github.com/garcm494/sdui-gradients-research/assets/123591150/92d993a8-8e70-4a6a-ad68-b065a80e46ed">




--------------------
### Left to Right.
This `linear` gradient starts at the `left`, transitioning to light blue color at the `right`

```
{
	"gradient-sample": {
		"colors": ["0669AC", "027CBD"],
		"starts": "left",
		"direction-angle": "right",
		"type": "linear"
	}
}
```

#### Flutter Translation.
```
BoxDecoration(
	gradient: LinearGradient(
			begin: Alignment.left,
              		end: Alignment.right,
              		colors: [
                		Colors(0669AC),
                		Colors(027CBD),
              		],
	)
)
```


#### Output.
<img width="510" alt="Screenshot 2023-07-06 at 12 05 53 PM" src="https://github.com/garcm494/sdui-gradients-research/assets/123591150/797ea744-6739-4d3f-84ce-947244b136ec">

--------------------
### Sample Diagonal.
This `linear` gradient starts at the `top-left`, transitioning to light blue color at the `bottom-right`

```
{
	"gradient-sample": {
		"colors": ["0669AC", "027CBD"],
		"starts": "top-left",
		"direction-angle": "bottom-right",
		"type": "linear"
	}
}
```

#### Flutter Translation.
```
BoxDecoration(
	gradient: LinearGradient(
			begin: Alignment.topLeft,
              		end: Alignment.bottomRight,
              		colors: [
                		Colors(0669AC),
                		Colors(027CBD),
              		],
	)
)
```

#### Output.
<img width="510" alt="Screenshot 2023-07-06 at 12 15 54 PM" src="https://github.com/garcm494/sdui-gradients-research/assets/123591150/892007ce-528a-44c3-a4a0-219544375973">


## Linear Gradients - Different Angles

### Sample with Angles.
The next gradient colros and transitions are defined by a degree provided on the `direction-angle`, transitioning from the first color in the `colors` array to the last one.

```
{
	"gradient-sample-0Deg": {
		"colors": ["0669AC", "027CBD"],
		"direction-angle": "0",
		"type": "linear"
	},
	"gradient-sample-90Deg": {
		"colors": ["0669AC", "027CBD"],
		"direction-angle": "90",
		"type": "linear"
	},
	"gradient-sample-180Deg": {
		"colors": ["0669AC", "027CBD"],
		"direction-angle": "180",
		"type": "linear"
	},
	"gradient-sample-negative-90Deg": {
		"colors": ["0669AC", "027CBD"],
		"direction-angle": "-90",
		"type": "linear"
	}
}
```

#### Flutter Translation.

![angles](https://github.com/garcm494/sdui-gradients-research/assets/123591150/0ec8c6eb-04cb-44dc-ab25-db2cb4c9b300)


### 0 Degrees.
```
BoxDecoration(
	gradient: LinearGradient(
			begin: Alignment(0.0, -1.0),
              		end: Alignment(0.0, 1.0),
              		colors: [
                		Colors(0669AC),
                		Colors(027CBD),
              		],
	)
)
```

### 90 Degrees.
```
BoxDecoration(
	gradient: LinearGradient(
			begin: Alignment(-1.0, 0.0),
              		end: Alignment(1.0, 0.0),
              		colors: [
                		Colors(0669AC),
                		Colors(027CBD),
              		],
	)
)
```

### 180 Degrees.
```
BoxDecoration(
	gradient: LinearGradient(
			begin: Alignment(0.0, 1.0),
              		end: Alignment(0.0, -1.0),
              		colors: [
                		Colors(0669AC),
                		Colors(027CBD),
              		],
	)
)
```

### -90 Degrees.
```
BoxDecoration(
	gradient: LinearGradient(
			begin: Alignment(1.0, 0.0),
              		end: Alignment(-1.0, 0.0),
              		colors: [
                		Colors(0669AC),
                		Colors(027CBD),
              		],
	)
)
```


#### Output.
<img width="1069" alt="Screenshot 2023-07-06 at 12 37 16 PM" src="https://github.com/garcm494/sdui-gradients-research/assets/123591150/416cba1d-3716-4069-b669-4cf4ba5c29bc">

--------------------
## Multiple Color Stops
`linear` gradient with 3 color stops evenly spaced (since no percents are specified). 

```
{
	"gradient-sample": {
		"colors": ["0669AC", "1FA43C", "027CBD"],
		"starts": "top",
		"direction-angle": "down",
		"type": "linear"
	}
}
```

#### Flutter Translation.
```
BoxDecoration(
	gradient: LinearGradient(
			begin: Alignment.top,
              		end: Alignment.bottom,
              		colors: [
                		Colors(0669AC),
				Colors(1FA43C),
                		Colors(027CBD),
              		],
	)
)
```

#### Output.
<img width="510" alt="Screenshot 2023-07-06 at 12 57 37 PM" src="https://github.com/garcm494/sdui-gradients-research/assets/123591150/2b307052-ae55-49c2-8a57-0d44da01c502">

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
BoxDecoration(
	gradient: LinearGradient(
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
)
```

#### Output.
<img width="510" alt="Screenshot 2023-07-06 at 1 24 12 PM" src="https://github.com/garcm494/sdui-gradients-research/assets/123591150/b003c566-373c-471d-a319-3af824a6dbff">






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
				"status": "#dfe2eb",
				"gradients": {
					"hubCards": {
						"colors": ["0669AC", "027CBD"],
						"starts": "top",
						"direction-angle": "down",
						"type": "linear"
					},
					"homeCards": {
						"colors": ["0669AC", "027CBD"],
						"starts": "left",
						"direction-angle": "right",
						"type": "linear"
					},
					"menuCards": {
						"colors": ["0669AC", "027CBD"],
						"starts": "top-left",
						"direction-angle": "bottom-right",
						"type": "linear"
					},
					"profileCards": {
						"colors": ["0669AC", "027CBD"],
						"direction-angle": "0deg",
						"type": "linear"
					},
					"gradient-sample-with-percents": {
						"colors": ["0669AC", "1FA43C", "027CBD"],
						"percents": {
							"0669AC": "30.82%",
							"1FA43C": "40.68%",
							"027CBD": "50.53%"
						},
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
