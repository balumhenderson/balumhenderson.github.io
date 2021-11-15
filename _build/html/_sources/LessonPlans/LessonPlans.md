# Lesson Plans
## Week 1 - 04/10/2021
### Housekeeping
One lecture a week on Wednesdays, and one tutorial on Mondays. The tutorial should always be in person and always in the same place. Please try to be on time (5 past the hour) but I understand that this is a little away from the main campus so don't worry.

Attendance will be taken each week, please sign in on the sheet provided.

The format for our tutorials can change around if we want it to, but to start what I think we should do is try to do the problems before each tutorial, and then we can focus on any sticking points, rather than just going through every question on the board. As well as the problems given to you, feel free to ask questions about the course content either in person or via email.

[Learning Outcomes Survey](https://tinyurl.com/ry2c84xc)

https://tinyurl.com/ry2c84xc

### Introductory Questions
Go through the [introductory questions](content:IntroQs) given out last week.

### Mathematics Intervention Project
[MIP](https://moodle.ucl.ac.uk/mod/book/view.php?id=3034006)



## Week 5 - 01/11/2021
### Intro

### Differentiation Rules
```{figure} derivativeRules.png
---
name: derivativeRules
---
Here are some of the simple rules to follow for finding derivatives.
```

### Integration Rules
```{figure} integralRules.png
---
name: integralRules
---
Here are some of the simple rules to follow for finding integrals.
```

### Integration by parts
One of the nice ways to think about integration by parts is as the 'opposite' to the product rule.

```{math}
\frac{\mathrm{d}}{\mathrm{d}x}\left[\mathrm{f}(x) \cdot \mathrm{g}(x)\right] = \mathrm{f}'(x) \cdot \mathrm{g}(x) + \mathrm{f}(x) \cdot \mathrm{g}'(x)
```

Rearrange this to get

```{math}
\mathrm{f}(x) \cdot \mathrm{g}'(x) = \frac{\mathrm{d}}{\mathrm{d}x}\left[\mathrm{f}(x) \cdot \mathrm{g}(x)\right] - \mathrm{g}(x) \cdot \mathrm{f}'(x)
```

Now integrate both sides of the equation:

```{math}
\int \big( \mathrm{f}(x) \cdot \mathrm{g}'(x)\big) \mathrm{d}x = \int \big( \frac{\mathrm{d}}{\mathrm{d}x}\left[\mathrm{f}(x) \cdot \mathrm{g}(x)\right] - \mathrm{g}(x) \cdot \mathrm{f}'(x) \big) \mathrm{d}x
```

Split the right hand side into 2 using the sum rule:

```{math}
\int \big( \mathrm{f}(x) \cdot \mathrm{g}'(x)\big) \mathrm{d}x = \int \big( \frac{\mathrm{d}}{\mathrm{d}x}\left[\mathrm{f}(x) \cdot \mathrm{g}(x)\right] \big) \mathrm{d}x - \int \big( \mathrm{g}(x) \cdot \mathrm{f}'(x) \big) \mathrm{d}x
```

The first integral on the right undoes the differentiation:

```{math}
\int \big( \mathrm{f}(x) \cdot \mathrm{g}'(x)\big) \mathrm{d}x = \left[\mathrm{f}(x) \cdot \mathrm{g}(x)\right] - \int \big( \mathrm{g}(x) \cdot \mathrm{f}'(x) \big) \mathrm{d}x
```
And here we are left with integration by parts, in a form we can recognise! Simplifying slightly by letting $u=\mathrm{f}(x)$ and $v=\mathrm{g}(x)$ we obtain the very familiar:

```{math}
\int u \mathrm{d}v = u v - \int v \mathrm{d}u
``` 







