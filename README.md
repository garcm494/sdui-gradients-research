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
		"direction": "down",
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
		"direction": "right",
		"type": "linear"
	}
}
```

<img width="510" alt="Screenshot 2023-07-06 at 12 05 53 PM" src="https://github.com/garcm494/sdui-gradients-research/assets/123591150/797ea744-6739-4d3f-84ce-947244b136ec">







### Sample on theme document.
```
{
	"gradients": {
		"hubCards": {
			"colors": ["0669AC", "027CBD"],
			"starts": "top",
			"direction": "down",
			"type": "linear"
		},
		"homeCards": {
			"colors": ["0669AC", "027CBD"],
			"starts": "left",
			"direction": "right",
			"type": "linear"
		}
	}
}
```
