  
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

To work around this caveat, we instead use a **non-zero** interval, one that becomes infinitely small. A **derivative** is then the value that the average rate approaches as the interval shrinks to zero. 

The formal definition of a derivative then logically follows this definition. The change in output divided by the change in input as the change in input itself *approaches zero*.

	$$f'(a) = \lim\limits_{h \to 0} \frac{f(a + h) - f(a)}{h}$$
*As $h$ gets closer and closer to 0, does the slope tend toward one single number? If yes, that number is the derivative, if not, the derivative doesn't exist. 


## Integration
Derivatives dealt with slopes of curves, where integration deals with the area of curves. 