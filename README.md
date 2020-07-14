
# Dynamic Window Approach

### Value Function
1. Obstacle Avoid
2. Velocity Differece
3. Relative Angle to Goal
4. Relative Position to Goal

### caliculated cost
1. Obstacle Avoid (Obstacle)

    The maximum value along with predicted path with obstacle is used to evaluate

    <img src="https://latex.codecogs.com/gif.latex?v_{opt},\omega_{opt}=max((x_{obst}-x)^2+(y_{obst}-y)^2)" />

2. Velocity Differece (Velocity)
  
    The diffetence between desired speed and stop

    <img src="https://latex.codecogs.com/gif.latex?v_{opt},\omega_{opt}=max(v)" />

3. Relative Angle to Goal (Heading)
  
    Use end path point pose pose is used to evaluate

    <img src="https://latex.codecogs.com/gif.latex?v_{opt},\omega_{opt}=min(abs(theta_{pred}-theta_{goal}))" />

4. Relative Position to Goal (Near)

    Use end path point pose pose is used to evaluate
    
    <img src="https://latex.codecogs.com/gif.latex?v_{opt},\omega_{opt}=min(hypot(x_{pred}-x_{goal},y_{pred}-y_{goal}))" />

### Optimal Search Caliculation
  
    Normalize predicted value and search the best set

    <img src="https://latex.codecogs.com/gif.latex?V_{(v,\omega)}=\alpha*Obstacle(v,\omega)+\beta*Velocity(v,\omega)+\gamma*Heading(v,\omega)+\delta*Near(v,\omega)" />
