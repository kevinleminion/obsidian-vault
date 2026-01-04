  
>[!note] Overview
>Basic stuff concerning MATH 249 concepts that $\textbf{should}$ be known for MATH 267. While concepts like limits and derivatives will be covered, MATH 267 has a much larger emphasis on integration.

Recall that calculus exists to answer the simple question of how we describe things that continuously change. Things like growth, flow, and accumulation cannot be easily described through algebra or other methods. *Derivatives* describe the current rate of change, while *integrals* describe how much changes in **total**, or simply the area of a curve. 
## Limits
A limit simply *describes the behaviour* of a function as it approaches a certain value. It doesn't equal anything.

> [!info] 
> We search for a *trend* in the function rather than the value itself; think of it as the smallest value adjacent to the point. This isn't a value that exists, since decimals expand infinitely.

> [!faq]- Why do we care about behaviour near a point?
> Sometimes the value at the point is meaningless or results in an impossible answer; for example, take division by 0. When x = 0, it is simply undefined, but when we take values *near* 0 it tells something completely different.

Therefore, we can conclude that a limit will not exist if both the right-side and the left-side approximations do not converge to a single number. 
## Derivatives
The instantaneous rate of change of any given point on the graph, determined through the slope of a tangent line.

> [!warning]
> You cannot just use the $\frac{\Delta y}{\Delta x}$ formula for a specific point because both values for change will be equal to 0.

To get around this caveat, we instead use a **non-zero** interval, one that becomes infinitely small. A **derivative** is then the value that the average rate approaches as the interval shrinks to zero. 

The formal definition of a derivative then logically follows this definition. The change in output divided by the change in input as the change in input itself *approaches zero*.

	$$f'(a) = \lim\limits_{h \to 0} \frac{f(a + h) - f(a)}{h}$$
*As $h$ gets closer and closer to 0, does the slope tend toward one single number? If yes, that number is the derivative, if not, the derivative doesn't exist. 

> [!warning]
> Derivatives do not exist for sharp points or vertical lines because the limit of the slope is not a unique number.

This is because for a sharp point, the slopes on the left and right side both approach different numbers. The limit of slopes do not converge, therefore the derivative doesn't exist. Vertical lines are much simpler because as you approach a point on the line, the slope grows infinitely. 

> [!example]
> For the function $f(x) = \lvert{x}\rvert$, take the corner at $x = 0$. On the left side, the graph has a slope of -1, but on the right side it has a slope of 1. While the limits converge, the slope does not.  

![[Derivative Rules.png]]

### Chain Rule
A basic formula that allows the expression of the derivative of the *composition* of two differentiable functions. So basically the derivative of a composite function.


## Integration
Derivatives dealt with slopes of curves, where integration deals with the area of curves. This allows us to ask questions such as "how much has something changed in total", things like total distance travelled or mass compared to density.

> [!info] 
> This is simple enough to figure out when you have a rectangle, but what about when you have something like a curve where you can't easily do this?

What we do is split a curve into as many infinitely small rectangles as possible; the precision of this rectangle as it gets smaller increases, and adding up the area of all the rectangles gives us the total area. 

*There is no smallest interval or size of rectangles. You can infinitely increase the number of rectangles by shrinking the width, which is where limits come back into play.* 

For our purposes, the limit we use is 0; as the width of each rectangle approaches zero, do the accumulated totals of all the rectangles converge to a single number? If so, that number will be the total area of the curve. 

> [!faq]- What then is the definition of an integral?
> An integral is the **limit** of this accumulation of rectangles. So, the *signed* area (or number we approach) under the curve as the number of rectangles increases.
$$\int_a^b f(x)\,\mathrm{d}x$$
1. $a$ and $b$ describe the bounds of the function that you accumulate; so if $a$ and $b$ were 0 and 2, then you would accumulate rectangles from the range $[0:2]$. 
2. $f(x)$ describes the height of each individual rectangle. So if $f(x)$ is a value above the x-axis, it is a positive contribution, if it is a value below the x-axis it is a negative contribution.
3. $dx$ is pretty strange, but for our purposes we can say it represents whichever variable is being sliced into rectangles. 

> [!tip] 
> Eventually, we will have to change $dx$. It can even represent entire functions, such as $g(x)$ in the case of a nested function.

### Relationship Between Derivatives

$$\frac{d}{dx}\left(\int_a^b f(t)\,\mathrm{d}t\right) = f(x)$$
Strangely complex formula, but all it says in reality is that the derivative of the accumulation is the original function. Accumulation undoes differentiation, and vice versa. 

> [!info] 
> You can probably then come to the conclusion that to calculate an integral, you can compute the antiderivative of a function.