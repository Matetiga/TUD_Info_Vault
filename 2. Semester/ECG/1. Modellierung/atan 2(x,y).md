$$
atan2(x,y)
\left\{

    \begin{array}{ll}
        \arctan\left( \frac{y}{x} \right) & \text{if } x \geq 0 \\
        \arctan\left( \frac{y}{x} \right)+\pi & \text{if } x < 0 \ \text{und}\ y\geq 0 \\
\arctan\left( \frac{y}{x} \right)-\pi & \text{if }x<0 \text{und }y<0 \\
\frac{\pi}{2} & \text{if }x=0 \text{und }y>0 \\
-\frac{\pi}{2} & \text{if }x=0 \text{und }y<0 \\
\text{nicht definiert} & \text{if }x=0 \text{und }y=0 
    \end{array}
\right.
$$
