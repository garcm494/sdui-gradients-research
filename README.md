# Gradient Configuration

## Phase I. Linear Gradients
Up, Down, Left, Right, Diagonally.

## Requirements:
- At least 2 colors.
- Starting point (top, bottom, left, right).
- Direction / angle (up, down, left, right, diagonally).
- Gradient type (linear, radial, conic).

### Sample Top to Bottom.
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

<img width="510" alt="Screenshot 2023-07-06 at 11 56 46 AM" src="https://github.com/garcm494/sdui-gradients-research/assets/123591150/92d993a8-8e70-4a6a-ad68-b065a80e46ed">


### Sample Left to Right.
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

<img width="510" alt="Screenshot 2023-07-06 at 12 05 53 PM" src="https://github.com/garcm494/sdui-gradients-research/assets/123591150/797ea744-6739-4d3f-84ce-947244b136ec">

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

<img width="510" alt="Screenshot 2023-07-06 at 12 15 54 PM" src="https://github.com/garcm494/sdui-gradients-research/assets/123591150/892007ce-528a-44c3-a4a0-219544375973">


## Linear Gradients - Different Angles

### Sample with Angles.
The next gradient colros and transitions are defined by a degree provided on the `direction-angle`, transitioning from the first color in the `colors` array to the last one.

```
{
	"gradient-sample": {
		"colors": ["0669AC", "027CBD"],
		"direction-angle": "0deg",
		"type": "linear"
	}
}
```

<img width="1069" alt="Screenshot 2023-07-06 at 12 37 16 PM" src="https://github.com/garcm494/sdui-gradients-research/assets/123591150/416cba1d-3716-4069-b669-4cf4ba5c29bc">







--------------------------------------------------------------

### Sample on theme document.
```
{
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
		}
	}
}
```
