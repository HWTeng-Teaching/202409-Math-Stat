## Q8
## Find the joint and marginal densities corresponding to the cdf

$$
F(x, y) = (1 - e^{-\alpha x})(1 - e^{-\beta y}), \quad x \geq 0, y \geq 0, \alpha > 0, \beta > 0
$$

## Answer:

### Joint Density
To find the joint density function \( f(x, y) \), differentiate the CDF \( F(x, y) \) with respect to both \( x \) and \( y \):

$$
f(x, y) = \frac{\partial^2 F(x, y)}{\partial x \partial y}
$$

First, differentiate \( F(x, y) \) with respect to \( x \):

$$
\frac{\partial F(x, y)}{\partial x} = \alpha e^{-\alpha x}(1 - e^{-\beta y})
$$

Then, differentiate with respect to \( y \):

$$
f(x, y) = \frac{\partial}{\partial y} \left[ \alpha e^{-\alpha x}(1 - e^{-\beta y}) \right] = \alpha e^{-\alpha x} \cdot \beta e^{-\beta y}
$$

Thus, the **joint density** is:

$$
f(x, y) = \alpha \beta e^{-\alpha x} e^{-\beta y}, \quad x \geq 0, y \geq 0
$$

### Marginal Density of \( X \)
To find the marginal density of \( X \), integrate the joint density over \( y \):

$$
f_X(x) = \int_0^\infty f(x, y) \, dy = \int_0^\infty \alpha \beta e^{-\alpha x} e^{-\beta y} \, dy = \alpha e^{-\alpha x}
$$

Thus, the marginal density of \( X \) is:

$$
f_X(x) = \alpha e^{-\alpha x}, \quad x \geq 0
$$

### Marginal Density of \( Y \)
Similarly, to find the marginal density of \( Y \), integrate the joint density over \( x \):

$$
f_Y(y) = \int_0^\infty f(x, y) \, dx = \int_0^\infty \alpha \beta e^{-\alpha x} e^{-\beta y} \, dx = \beta e^{-\beta y}
$$

Thus, the marginal density of \( Y \) is:

$$
f_Y(y) = \beta e^{-\beta y}, \quad y \geq 0
$$

