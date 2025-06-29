# Rigging Report

## Lifting Load Calculation

The lifting load calculation involves determining the weight of the load and the forces acting on it during lifting. The following formulas and methods were used:

- **Pipe Weight Calculation**:

  $$
  \text{Weight per Meter} = \text{Outer Diameter} \times \pi \times \text{Thickness} \times 7.85
  $$
  $$
  \text{Weight} = \text{Weight per Meter} \times \text{Length}
  $$

  The calculated weight of the spreader bar pipe is approximately **2.28 T**.

- **Load at Each Lifting Point**:

  $$
  L = W \times \left( \frac{d_{t1}}{od_{t1}} \right) \times \left( \frac{d_{t2}}{od_{t2}} \right)
  $$

## Position of C.O.G

The position of the center of gravity (C.O.G) is crucial for ensuring stability during lifting. The distances from the C.O.G to the lifting points were calculated and used in subsequent load calculations.

## Calculation for Each Lifting Point of the Load Structure

The load at each lifting point was calculated using the formula:

$$
\text{Load at Lifting Point} = \frac{\text{Weight of Load} \times \text{Distance from C.O.G to Lifting Point}}{\text{Distance from C.O.G to All Lifting Points}}
$$

The lifting points and their respective loads are as follows:

- **Lifting Point 1**: 37.5 T
- **Lifting Point 2**: 37.5 T
- **Lifting Point 3**: 37.5 T
- **Lifting Point 4**: 37.5 T

## Tension Calculation

The tension in the slings was calculated using the formula:

$$
\text{Tension} = \frac{\text{Load}}{\sin(\theta)}
$$

The calculated tensions for the slings are:

- **Sling 1**: 39.8 T
- **Sling 2**: 39.8 T
- **Sling 3**: 40.5 T
- **Sling 4**: 40.5 T

## Load at the Padeye of Spreader Bar

The loads at the padeye of the spreader bar were calculated as follows:

- **Load at Pu2**: 0.14 T
- **Load at Pu1**: 0.15 T

## Calculate for the Upper Sling

The tension in the upper slings and the hook load were calculated:

- **Slu2 Tension**: 75.0 T
- **Slu1 Tension**: 75.0 T
- **Hook Load**: 150.0 T

## Compressive Stress on the Spreader Bar

The compressive stress acting on the spreader bar was calculated using the formula:

$$
\text{Longitudinal Load} = \text{Load} \times \cos(\theta)
$$

The total compressive stress on the spreader bar is **140.0 T**.

## Summary

### Lifting Load at 4 Lifting Points of Structure

| Lifting Point | Load (T) |
| ------------- | -------- |
| 1             | 37.5     |
| 2             | 37.5     |
| 3             | 37.5     |
| 4             | 37.5     |

### Tension of the 4 Bottom Slings

| Sling | Tension (T) |
| ----- | ----------- |
| 1     | 39.8        |
| 2     | 39.8        |
| 3     | 40.5        |
| 4     | 40.5        |

### Upper Sling and Hook Load

| Component    | Load (T) |
| ------------ | -------- |
| Slu2 Tension | 75.0     |
| Slu1 Tension | 75.0     |
| Hook Load    | 150.0    |

### Compressive Stress on Spreader Bar

| Component                | Stress (T) |
| ------------------------ | ---------- |
| Total Compressive Stress | 140.0      |
