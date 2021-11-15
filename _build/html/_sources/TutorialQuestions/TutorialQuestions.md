# Tutorial Questions
(content:IntroQs)=
## Introductory Questions - 04/10/2021
### Question 1
1\. Factorise fully the expression: $(x+1)(2x-2) + (x-1)(x+1)^2$


```{math}
(x+1)[2x-2 + (x-1)(x+1)] \\
= (x+1)[2x-2 + x^2 - 1] \\
= (x+1)[x^2 + 2x -3] \\
= (x+1)(x+3)(x-1)
```

Take out a factor of $(x+1)$ from both terms, and treat the rest like a normal binomial. Best not to expand out fully, as the common factor makes it much easier from the get-go.

### Question 2
2\. Find the maximum of the function: $\frac{1}{ax^2+bx+c}$

We know very little about this system, and so we need to think about how to gain insights. The best initial method would be to find a general plot for this system. Do this using wolfram alpha or something similar. There are 3 possibilities


```{figure} IntroQs2.png
---
name: IntroQs2 Plot
---
Two of the possible variants of the inverse parabola. Either it is wholly under the x axis, in which case it does not have a well defined maximum, or it is completely above the x-axis in which case the maximum is well defined.
```


We can then find more information on the system by "completing the square".


```{math}
\textrm{Let } p=ax^2+bx+c \\
= a[x^2 + \frac{b}{a}x + \frac{c}{a}] \\
= a[(x+\frac{b}{2a})^2 + \frac{c}{a} - \frac{b^2}{4a^2}] \\
= a[(x+\frac{b}{2a})^2 + \frac{4ac-b^2}{4a^2}]
```


Note that the term $(x+\frac{b}{2a})^2$ is always positive because of the squared term. The important portion of the expression is then $\frac{4ac-b^2}{4a}$. This allows us to say that:
* If $4ac-b^2<0$, the function has no finite maximum, as it crosses the x-axis and can be arbritararily large,
* If $4ac-b^2>0$ and $a<0$, the function has no maximum but is bounded above by $0$,
* If $4ac-b^2>0$ and $a>0$, the maximum of the function is $\frac{4a}{4ac-b^2}$.

### Question 3
3\. Write $log_3(17)$ fully in terms of lo to the base $e$.

```{math}
y = log_3(17) \\
3^y = 17 \\
ln(3^y) = ln(17) \\
yln(3) = ln(17) \\
y = \frac{ln(17)}{ln(3)}
```

### Question 4
4\. Find all the values of $x$ which are satisfied by: $|3x+2| < |x^2 - 2|$

A graphical approach can help here. Naming the RHS $f(x)$ and the LHS $g(x)$, we can plot both the functions and see where $f(x)>g(x)$.

```{figure} IntroQs4.png
---
name: IntroQs4 Plot
---
Plotting both functions and finding the intercepts, we can see that they intersect at 4 points.
```

Points $1-4$ can be found by solving:

```{math}
x^2 - 2 = 3x + 2 >>> x = -1, 4 \\
\textrm{OR} \\
x^2 - 2 = -3x - 2 >>> x = -3, 0
```

We can then say that the solution is when $x<-3, -1<x<0, x>4$.

### Question 5
5\. What is the sum of $\frac{1}{n} + \frac{1}{2n} + \frac{1}{4n} + \frac{1}{8n} + ...$ where $n=2$ and $n=-3$?

We can re-write this as $\frac{1}{n}(1 + \frac{1}{2} + \frac{1}{4} + \frac{1}{8} + ...)$ which is a geometric series. The first term, $a$ is $1$, and the common ration $r=\frac{1}{2}$. The infinite sum of the series can be found with $S_\inf = \frac{a}{1-r} = \frac{1}{1-\frac{1}{2}} = 2$.

The sum of our expression is then given by $\frac{2}{n}$. The only value for $n$ that is undefined is $n=0$.

### Question 6
6\. Given that $u_n = \frac{x^n}{2^{2n}\sqrt{n}}$, find and simplify the expression for $\frac{u_{n+1}}{u_n}$.

```{math}
\frac{x^{n+1}2^{2n}\sqrt{n}}{2^{2(n+1)}\sqrt{n+1}x^n} \\
= \frac{x\sqrt{n}}{2^2\sqrt{n+1}} \\
= \frac{x}{4}\sqrt{\frac{n}{n+1}}
```

Common error to miss out the $2^2$, and get over 2 instead of over 4.

### Question 7
7\. Find all of the solutions to the simultaneous equations $6x+ay^2=-1$ and $2axy+2y=0$.

It is potentially tempting to try and solve each equation seperately, but this can introduce false solutions. It is best to factorise one, find the solutions and substitute then into the other. Start by re-writing them both:

```{math}
6x+ay^2+1=0 \\
2y(ax+1) = 0 \\
```

Looking at (2), either $y=0$ or $x=-\frac{1}{a}$.

If $y=0$, eqn (1) gives $x=-\frac{1}{6}$.

Taking $x=-\frac{1}{a}$, we can find that $y=\pm\sqrt{\frac{6-a}{a^2}}$.

We then have the solutions $(-\frac{1}{6},0)$, and $(-\frac{1}{a},\pm\sqrt{\frac{6-a}{a^2}})$.


## Sequences and Series - 11/10/2021
### Question 1
1\. Find the constant term in the expansion $(x^2 - \frac{1}{x})^9$

```{math}
(x+y)^n = \sum_{k=0}^{n} \binom{n}{k} x^k y^{n-k} \textrm{ where } \binom{n}{k} = \frac{n!}{(n-k)!k!}
```


## Differentiation and Integration - 01/11/2021
### Parametric Differentiation - Q1
Letting $x(t) = t\sin(t)$ and $y(t) = \cos(t)$, find $\frac{\mathrm{d}^2 y}{\mathrm{d}x^2}$ at $t=1$.

To start with this one, we need to remember:
```{math}
\frac{\mathrm{d} y}{\mathrm{d}x} = \frac{\mathrm{d} y}{\mathrm{d}t} \frac{\mathrm{d} t}{\mathrm{d}x} = \frac{\mathrm{d} y}{\mathrm{d}t} \big( \frac{\mathrm{d} x}{\mathrm{d}t} \big)^{-1}
```
From here we can find:
```{math}
\frac{\mathrm{d} y}{\mathrm{d}x} = \frac{-\sin(t)}{\sin(t) + t\cos(t)}
```
Next, we repeat the process once more, finding $\frac{\mathrm{d}^2 y}{\mathrm{d}x^2} = \frac{\mathrm{d}}{\mathrm{d}t} \big( \frac{\mathrm{d} y}{\mathrm{d}x} \big) \big( \frac{\mathrm{d} x}{\mathrm{d}t} \big)^{-1}$
```{math}
\frac{\mathrm{d}}{\mathrm{d}t}\big( \frac{\mathrm{d} y}{\mathrm{d}x} \big) = \frac{-\cos(t)}{\big( \sin(t) t \cos(t) \big)} + \frac{\sin(t)(2\cos(t) - t\sin(t))}{(\sin(t) + t\cos(t))^2}
```
And finally:
```{math}
\frac{\mathrm{d}^2 y}{\mathrm{d}x^2} = \frac{-\cos(t)}{( \sin(t) + t\cos(t))^2} + \frac{\sin(t)(2\cos(t) - t\sin(t))}{(\sin(t) + t\cos(t))^3}
```
Substituting in $t=1$, we find that $\frac{\mathrm{d}^2 y}{\mathrm{d}x^2} \approx -0.282985 + 0.076273 = -0.206712$.

### Implicit Differentiation - Q2
With $4 \mathrm{sinh}(xy) + y = 4$, find $\frac{\mathrm{d} y}{\mathrm{d}x}$ where $x = \ln(2)$, $y=1$.

Start by differentiating all w.r.t $x$:
```{math}
4y\mathrm{cosh}(xy) + 4x\frac{\mathrm{d} y}{\mathrm{d}x}\mathrm{cosh}(xy) + \frac{\mathrm{d} y}{\mathrm{d}x} = 0
```
Rearranging this, we can find $\frac{\mathrm{d} y}{\mathrm{d}x}$ on its own:
```{math}
\frac{\mathrm{d} y}{\mathrm{d}x} = \frac{-4y\mathrm{cosh}(xy)}{1+4x\mathrm{cosh}(xy)}
```
And substituting in $x = \ln(2)$, $y=1$ we find the answer to be:
```{math}
\frac{-5}{1+5\ln(2)} \approx -1.1196
```

### Integration by Substitution - Q3
Evaluate $I = \int_0^5 \frac{1}{25+9x^2} \mathrm{d}x$.

The first step here is finding the correct substitution to use. In this case, we work with $3x = 5\tan(u)$.
```{math}
3x = 5\tan(u) \implies 9x^2 = (5\tan(u))^2 = 25\tan^2(u) \implies \mathrm{d}x = \frac{5}{3} \sec^2(u) \mathrm{d}u
```
We also need to re-evaluate our limits $a_x=0$ and $b_x=5$:
```{math}
3(0) = 5\tan(u) \implies u = \arctan\big[\frac{3}{5}(0)\big] = 0 \textrm{   and   } 3(5) = 5\tan(u) \implies u = \arctan\big[\frac{3}{5}(5)\big] = \arctan(3)
```
Now we can put all of this back in to get our new expression for $I$:
```{math}
I = \int_0^{\arctan(3)} \frac{5}{3}\frac{\sec^2(u)}{25 + 25\tan^2(u)}\mathrm{d}u = \frac{1}{15} \int_0^{\arctan(3)} \frac{\sec^2(u)}{25 + 25\tan^2(u)}\mathrm{d}u
```
There is a trig identity that helps us out greatly here, and that is $1+\tan^2(x) = \sec^2(x)$:
```{math}
I=\frac{1}{15} \int_0^{\arctan(5)} \mathrm{d}u = \frac{1}{15} \big[ u \big]_0^{\arctan(3)} \approx 0.08326782
```

### Integration by Partial Fractions - Q4
Evaluate $I = \int_{-1/2}^{1/2} \frac{x^3-3}{x^2-1} \mathrm{d}x$.

First step is to use partial fractions to obtain:
```{math}
\frac{x^3-3}{x^2-1} = \frac{\mathrm{A}}{1} + \frac{\mathrm{B}}{x+1} + \frac{\mathrm{C}}{x-1}
```
```{math}
\mathrm{A}(x^2-1) + \mathrm{B}x + \mathrm{C}x - \mathrm{B} + \mathrm{C} = x^3 - 3
```
By subsituting in the roots ($x=1$ and $x=-1$), we can find that A$=x$, B$=2$ and C$=-1$. From here, we substitute back in to the integral:
```{math}
I = \int_{-1/2}^{1/2} \big[ x + \frac{2}{x+1} - \frac{1}{x-1} \big] \mathrm{d}x = \int_{-1/2}^{1/2} \big[ x + \frac{2}{x+1} + \frac{1}{1-x} \big] \mathrm{d}x
```
Which is not too bad to compute:
```{math}
I = \big[ \frac{x^2}{2} + 2\ln(x+1) + \ln(1-x) \big]_{-1/2}^{1/2} = \ln(3)
```

### Integration, Puzzle Questions




Let $p(x)=x^3-3x^2+x-3$

Then $p(3)=27-27+3-3=0$ so $x=3$ is a root of $p(x)$

Then $(x-3)$ is a factor

Write the other factor as $x^2+ax+b$

Then $(x-3)(x^2+ax+b)=x^3-3x^2+x-3$

Expanding out and comparing coefficients gives $a=0,\ b=1$

So we can write

$\frac{x+7}{x^3-3x^2+x-3}=\frac{A}{x-3}+\frac{Bx+C}{x^2+1}=\frac{A(x^2+1)+(Bx+C)(x-3)}{x^3-3x^2+x-3}$

The left and right sides can be made equal by taking $A=1,\ B=-1,\ C=-2$

So

$I=\int_0^2{\frac{1}{x-3}-\frac{x}{x^2+1}-\frac{2}{x^2+1}\mathrm{d}x}$

=$\left[\ln{|x-3|}-\frac{1}{2}\ln{(x^2+1)}-\tan^{-1}{x}\right]_0^2$

$=\left[0-\frac{1}{2}\ln{5}-\tan^{-1}{2}\right]-\left[\ln{3}-0-0\right]$

$=\ln{\frac{1}{3\sqrt{5}}}-2\tan^{-1}{2}$





-------------------


First we use a substitution $u=\sin{(x)}$ to obtain

$I=\int_{\sqrt{2}/2}^{1}{\frac{1}{u(u^2+1)}\mathrm{d}u}$

Then we employ partial fractions technique to write

$\frac{1}{u(u^2+1)}=\frac{A}{u}+\frac{(Bu+C)(u^2+1)}=\frac{A(u^2+1)+(Bu+C)u}{u(u^2-1)}$

To make the left and right sides equal, we can put

$A=1,\ B=-1,\ C=0$

Thus,

$I=\int_{\sqrt{2}/2}^{1}{\left(\frac{1}{u}-\frac{u}{u^2+1}\right)\mathrm{d}u$

$=\left[\ln{u}-\ln{\sqrt{u^2+1}}\right]_{\sqrt{2}/2}^{1}$

$=\ln{\sqrt{3}}-\ln{\sqrt{2}}=\frac{1}{2}\ln{\frac{3}{2}}$




------------------------------

The time averaged power is given by

$\bar{P}=\frac{1}{T}\int_0^T{I_0 V_0 \cos{(2\pi f t)}\cos{(2\pi f t +\delta)}\mathrm{d}t}$

$=\frac{I_0 V_0}{T}\int_0^T{\cos{(2\pi f t)}\left[\cos{(2\pi f t)}\cos{\delta}-\sin{(2\pi f t)}\sin{\delta}\right]\mathrm{d}t}$

$=\frac{I_0 V_0}{T}\int_0^T{\left[\cos^2{(2\pi f t)}\cos{\delta}-\sin{(2\pi f t)}\cos{(2\pi f t)}\sin{\delta}\right]\mathrm{d}t}$

$=\frac{I_0 V_0}{T}\int_0^T{\left[\frac{1}{2}(\cos{(4\pi f t)}+1)\cos{\delta}-\frac{1}{2}\sin{(4\pi f t)}\sin{\delta}\right]}$

$=\frac{I_0 V_0}{T}\left[ \left(\frac{1}{8\pi f}(\sin{(4\pi f t)})+\frac{t}{2}\right)\cos{\delta} -\frac{1}{8\pi f}\cos{(4\pi f t)}\sin{\delta} \right]_0^T$

$=\frac{I_0 V_0}{8\pi f T}\left[4\pi\cos{\delta}-\sin{\delta}+\sin{\delta}\right]$

$=\frac{I_0 V_0}{2}\cos{\delta}$



## Ordinary Differential Equations - 15/11/2021
### Integrating Factors - Q1
Find an integrating factor $\mu(x)$ for the problem $\frac{1}{y}\left(\frac{\mathrm{d}y}{\mathrm{d}x}-x^3\sin{(x)}\right)=2x\cot{(x^2)}$

This problem can be written in the form

```{math}
\frac{\mathrm{d}y}{\mathrm{d}x}+f(x)y=g(x)
\\
\frac{\mathrm{d}y}{\mathrm{d}x} - x^3 \sin(x) = 2xy\cot(x^2)
\\
\frac{\mathrm{d}y}{\mathrm{d}x} - 2xy\cot(x^2) =  x^3 \sin(x)
\\
\implies f(x)=-2x\cot{(x^2)}
```

We know that for problems of this type, an integrating factor is $\mu(x)=e^{\int{f(x)\mathrm{d}x}}$

In this case,

```{math}
\int{f(x)\mathrm{d}x} = -\int{\frac{2x\cos{(x^2)}}{\sin{(x^2)}}\mathrm{d}x} = -\ln{(\sin{(x^2)})} +\mathrm{const.}
```

so an integrating factor is

```{math}
\mu = e^{(-\ln{(\sin{(x^2)})})}=\frac{1}{\sin{(x^2)}}
```

### Integrating Factors - Q2
Find an integrating factor $\mu(x)$ for the problem $\cos{(x)}\frac{\mathrm{d}y}{\mathrm{d}x}-y\sin{(x)}=e^{2x}$

This problem can be written in the form

```{math}
\frac{\mathrm{d}y}{\mathrm{d}x}+f(x)y=g(x)
\\
\frac{\mathrm{d}y}{\mathrm{d}x} - y \frac{\sin(x)}{\cos(x)} = \frac{e^{2x}}{\cos(x)}
\\
\implies f(x)=-\frac{\sin{(x)}}{\cos{(x)}}
```

We know that for problems of this type, an integrating factor is $\mu=\exp{\int{f(x)\mathrm{d}x}}$

```{math}
\int-\frac{\sin{(x)}}{\cos{(x)}}\mathrm{d}x = -\int \tan(x) \mathrm{d}x = -\ln(\cos(x))
\\
\implies \mu(x) = e^{-\ln(cos(x))} = \frac{1}{\cos(x)}
```


### Integrating Factors - Q3
Find an integrating factor $\mu(x)$  for the problem $\cos^2{(x)}\frac{\mathrm{d}y}{\mathrm{d}x}+y\tan{(x)}=e^{x}$

This problem can be written in the form
```{math}
\frac{\mathrm{d}y}{\mathrm{d}x}+f(x)y=g(x)
\\
\frac{\mathrm{d}y}{\mathrm{d}x} + y \frac{\tan(x)}{\cos^2(x)} = \frac{e^x}{\cos^2(x)}
\\
\implies f(x)=\mathrm{sec}^2{(x)}\tan{(x)}
```

We know that for problems of this type, an integrating factor is $\mu=\exp{\int{f(x)\mathrm{d}x}}$

```{math}
\int \sec^2(x)\tan(x) \mathrm{d}x = \frac{\sec^2(x)}{2}
\\
\implies \mu(x) = e^{\frac{\sec^2(x)}{2}}
```

### Integrating Factors - Q4
Find an integrating factor $\mu(x)$  for the problem $\frac{1}{2}\frac{\mathrm{d}y}{\mathrm{d}x}-x=(\cos^2{x}-\sin^2{x})y$

This problem can be written in the form

```{math}
\frac{\mathrm{d}y}{\mathrm{d}x}+f(x)y=g(x)
\\
\frac{\mathrm{d}y}{\mathrm{d}x} - 2x = 2(\cos^2(x)-\sin^2(x))y
\\
\frac{\mathrm{d}y}{\mathrm{d}x} - 2(\cos^2(x)-\sin^2(x))y = 2x
\\
\implies f(x)=-2(\cos^2{x}-\sin^2{x})=-2\cos{(2x)}
```

We know that for problems of this type, an integrating factor is $\mu=\exp{\int{f(x)\mathrm{d}x}}$

```{math}
\int-2\cos{(2x)}\mathrm{d}x = -\sin(2x)
\\
\implies \mu(x) = e^{-\sin(2x)}
```

### Integrating Factors - Q5
Find an integrating factor $\mu(x)$  for the problem $\frac{1}{x}\frac{\mathrm{d}y}{\mathrm{d}x}-x=y\sqrt{x^2+2}$

This problem can be written in the form

```{math}
\frac{\mathrm{d}y}{\mathrm{d}x}+f(x)y=g(x)
\\
\frac{\mathrm{d}y}{\mathrm{d}x} - x^2 = xy\sqrt{x^2 + 2}
\\
\frac{\mathrm{d}y}{\mathrm{d}x} -xy\sqrt{x^2 + 2} = x^2
\\
\implies f(x)=-x\sqrt{x^2+2}
```

We know that for problems of this type, an integrating factor is $\mu=\exp{\int{f(x)\mathrm{d}x}}$

```{math}
\int-x\sqrt{x^2+2}\mathrm{d}x = -\frac{1}{3}(x^2+2)^\frac{3}{2}
\\
\implies \mu(x) = e^{-\frac{1}{3}(x^2+2)^\frac{3}{2}}
```

### Variable Exchange - Q6
Employ a change of variables $z=y^{-1}$ to solve the problem $x \frac{\mathrm{d}y}{\mathrm{d}x} +y = y^2x^2\ln{x},\ y(1)=1, \ x\in[1,2]$


The problem can be rewritten as
```{math}
\frac{\mathrm{d}y}{\mathrm{d}x}= y^2 x\ln{x}-\frac{1}{x}y
```
We introduce the variable change $z=y^{-1}$. Then

```{math}
\frac{\mathrm{d}z}{\mathrm{d}x} = \frac{\mathrm{d}z}{\mathrm{d}y}\frac{\mathrm{d}y}{\mathrm{d}x} =-y^{-2}\frac{\mathrm{d}y}{\mathrm{d}x}=-y^{-2}\left( y^2 x\ln{x}-\frac{1}{x}y \right)

=-x\ln{x} + \frac{1}{x}y^{-1}
```

That is,

```{math}
\frac{\mathrm{d}z}{\mathrm{d}x}-\frac{1}{x}z=-x\ln{x}
```

The modified problem can be solved by integrating factor $\mu = e^{\left(\int{-\frac{1}{x}\mathrm{d}x}\right)} = e^{(-\ln{x})}=\frac{1}{x}$

We obtain
```{math}
\frac{1}{x}\frac{\mathrm{d}z}{\mathrm{d}x}-\frac{1}{x^2}z=-\ln{x}
```
The left side is an exact derivative $\frac{\mathrm{d}}{\mathrm{d}x}(\mu z) = \frac{\mathrm{d}}{\mathrm{d}x}(\frac{z}{x})$.

We can write
```{math}
\frac{\mathrm{d}}{\mathrm{d}x}\left(\frac{1}{x}z\right) = -\ln{x}
```
Integrating both sides w.r.t $x$ gives
```{math}
\frac{1}{x}z=-\left[x\ln{x}+x\right]+k
```
where $k$ is a constant.

Rewriting in terms of the original variable $y$ gives
```{math}
\frac{1}{y}=x^2(1-\ln{x})+k x
```
and applying the condition $y(1)=1$ we find that $k=0$

Finally,
```{math}
y=\frac{1}{x^2(1-\ln{x})}
```

### Variable Exchange - Q7
Employ a change of variables $z=y^{-2}$ to solve the problem

$\frac{\mathrm{d}y}{\mathrm{d}x} = y\cot{(x)} +y^3\csc{(x)},\ y\left(-\frac{\pi}{2}\right)=-\frac{1}{4}, \ x\in\left[-\frac{\pi}{2},0\right] $

Using the given variable change,

$\frac{\mathrm{d}z}{\mathrm{d}x}=-2y^{-3}\frac{\mathrm{d}y}{\mathrm{d}x}=-2y^{-3}\left( y\cot{(x)} +y^3\csc{(x)} \right)$

$=-2y^{-2}\cot{(x)} - 2\csc{(x)}$

That is,

$\frac{\mathrm{d}z}{\mathrm{d}x}+(2\cot{(x)}) z=-2\csc{(x)}$

The modified problem can be solved by integrating factor

$\mu = \exp{\left(\int{2\frac{\cos{(x)}}{\sin{(x)}}\mathrm{d}x}\right)} = \exp{(2\ln{|\sin{(x)}|})}=\sin^2{(x)}$

We obtain

$\sin^2{x}\frac{\mathrm{d}z}{\mathrm{d}x}+2\sin{(x)}\cos{(x)}z=-2\sin{(x)}$

The left side is an exact derivative $\frac{\mathrm{d}}{\mathrm{d}x}(\mu z)$.

We can write

$\frac{\mathrm{d}}{\mathrm{d}x}\left(\sin^2{(x)}z\right) = -2\sin{(x)}$

Integrating both sides w.r.t $x$ gives

$(\sin^2{(x)})z=2\cos{(x)}+k$

where $k$ is a constant.

Rewriting in terms of the original variable $y$ gives

$\frac{1}{y^2}=\frac{k+2\cos{(x)}}{\sin^2{(x)}}$

and applying the condition $y\left(-\frac{\pi}{2}\right)=-\frac{1}{4}$ we find that $k=16$

Finally,

$y^2=\frac{\sin^2{(x)}}{16+2\cos{(x)}}$

We choose the positive root so that $y\left(-\frac{\pi}{2}\right)=-\frac{1}{4}$.

### Variable Exchange - Q8
Employ a change of variables $z=\frac{y}{x}$ to solve the problem

$(x+y)\frac{\mathrm{d}y}{\mathrm{d}x} -(4x+y)=0,\ y\left(1\right)=2, \ x\geq 1 $

This problem can be rewritten as

$\frac{\mathrm{d}y}{\mathrm{d}x} = \frac{4x+y}{x+y}=\frac{\frac{y}{x}+4}{\frac{y}{x}+1}$

We introduce the variable change $z=\frac{y}{x}$. Then 

$$\frac{\mathrm{d}z}{\mathrm{d}x}=-\frac{1}{x^2}y + \frac{1}{x}\frac{\mathrm{d}y}{\mathrm{d}x}=\frac{1}{x}\left(\frac{\mathrm{d}y}{\mathrm{d}x}-z\right)$$

$=\frac{1}{x}\left(\frac{z+4}{z+1}-\frac{z(z+1)}{z+1}\right) = \frac{1}{x}\left(\frac{4-z^2}{z+1}\right)$

This problem is separable:

$\int{\left(\frac{z+1}{4-z^2}\right)\mathrm{d}z}= \int{\frac{1}{x}\mathrm{d}x}$

The integral on the left can be solved using partial fractions:

$\frac{z+1}{z^2-4} = \frac{A}{z-2}+\frac{B}{z+2}$

Note that the denominator has been multiplied by $$-1$$ here, hence we introduce a $$-1$$ on the RHS also.

We obtain

$\frac{1}{4}\int{\left(\frac{3}{z-2}+\frac{1}{z+2}\right)\mathrm{d}z}=-\int{\frac{1}{x}\mathrm{d}x}$

That is,

$\frac{1}{4}\left[3\ln{|z-2|}+\ln{|z+2|}\right] = -\ln{|x|}+\mathrm{const}.$

$\ln{\left(|z-2|^3|z+2|\right)}=4\ln{\frac{\mathrm{const.}}{|x|}}$

$|z-2|^3|z+2| = \frac{\mathrm{const}.}{x^4}$

Rewriting in terms of the original variable, we obtain

$|y-2x|^3|y+2x|=\mathrm{const.}$

The condition $y(1)=2$ requires that the constant is zero and so we obtain

$(y-2x)^3(y+2x)=0$

This means that either $y=2x$ or $y=-2x$

The second solution does not satisfy the initial condition and so

$y=2x$
### Second Order - Q9
Solve the second order differential equation $2y^{\prime\prime}(x)+y^{\prime}(x)+3y(x)=0$, where $y(0)=1,\  y^{\prime}(0)=1$.

Answer:

**Ansatz**: $y = e^{\lambda x}$

**DE**: $e^{\lambda x}(2\lambda^2+\lambda + 3) = 0$

**Auxiliary equation**: $2\lambda^2+\lambda + 3=0$

The roots of this equation are found using the standard formula $x=\frac{-b \pm \sqrt{b^2 - 4ac}}{2a}$:
```{math}
\lambda = \frac{1}{4}(-1\pm i\sqrt{23})
```
Therefore the general solution is:
```{math}
y(x)=e^{-x/4}\left[A\cos{\left(\frac{\sqrt{23}}{4}x\right)}+B\sin{\left(\frac{\sqrt{23}}{4}x\right)}\right]
\\
y^{\prime}(x) = e^{-x/4}\left[\left(-\frac{1}{4}A+\frac{\sqrt{23}}{4}B\right)\cos{\left(\frac{\sqrt{23}}{4}x\right)}+\left(-\frac{1}{4}B-\frac{\sqrt{23}}{4}A\right)\sin{\left(\frac{\sqrt{23}}{4}x\right)}\right]
```

Applying the initial conditions:
```{math}
y(0)=1$ gives $A=1

y^{\prime}(0)=1 \implies -\frac{1}{4}A+\frac{\sqrt{23}}{4}B = 1
```

so $B=\frac{5}{\sqrt{23}}$

$y(x)=e^{-x/4}\left[\cos{\left(\frac{\sqrt{23}}{4}x\right)}+\frac{5\sqrt{23}}{23}\sin{\left(\frac{\sqrt{23}}{4}x\right)}\right]$

When $x=1$

$y = e^{-1/4}\left[\cos{\left(\frac{\sqrt{23}}{4}\right)}+\frac{5\sqrt{23}}{23}\sin{\left(\frac{\sqrt{23}}{4}\right)}\right]$
### Second Order - Q10
Solve the second order differential equation

$2y^{\prime\prime}(x)-2y^{\prime}(x)+3y(x)=0,$

$y(0)=1,\  y^{\prime}(0)=1$

Ansatz: $y = e^{\lambda x}$

Auxiliary equation: $2\lambda^2+-2\lambda + 3=0$

The roots of this equation are

$\lambda = \frac{1}{2}(1\pm i\sqrt{5})$

The general solution is

$y(x)=e^{x/2}\left[A\cos{\left(\frac{\sqrt{5}}{2}x\right)}+B\sin{\left(\frac{\sqrt{5}}{2}x\right)}\right]$

$y^{\prime}(x) = e^{x/2}\left[\left(\frac{1}{2}A+\frac{\sqrt{5}}{2}B\right)\cos{\left(\frac{\sqrt{5}}{2}x\right)}+\left(\frac{1}{2}B-\frac{\sqrt{5}}{2}A\right)\sin{\left(\frac{\sqrt{5}}{2}x\right)}\right]$

Applying the initial conditions

$y(0)=1$ gives $A=1$

$y^{\prime}(0)=1$ gives $\frac{1}{2}A+\frac{\sqrt{5}}{2}B = 1$

so $B=\frac{1}{\sqrt{5}}$

$y(x)=e^{x/2}\left[\cos{\left(\frac{\sqrt{5}}{2}x\right)}+\frac{\sqrt{5}}{5}\sin{\left(\frac{\sqrt{5}}{2}x\right)}\right]$

When $x=1$

$y =e^{1/2}\left[\cos{\left(\frac{\sqrt{5}}{2}\right)}+\frac{\sqrt{5}}{5}\sin{\left(\frac{\sqrt{5}}{2}\right)}\right]$
### Second Order - Q11
Solve the second order differential equation

$2y^{\prime\prime}(x)+3y(x)=0,$

$y(1)=0,\  y^{\prime}(1)=1$

Ansatz: $y = e^{\lambda x}$

Auxiliary equation: $2\lambda^2 + 3=0$

The roots of this equation are

$\lambda = \pm i\sqrt{\frac{3}{2}}$

The general solution is

$y(x)=A\cos{\left(\sqrt{\frac{3}{2}}x\right)}+B\sin{\left(\sqrt{\frac{3}{2}}x\right)}$

$y^{\prime}(x) = \sqrt{\frac{3}{2}}\left(B\cos{\left(\sqrt{\frac{3}{2}}x\right)}-A\sin{\left(\sqrt{\frac{3}{2}}x\right)}\right) $

Applying the initial conditions

$y(1)=0$ gives $A=-B\tan{\left(\sqrt{\frac{3}{2}}\right)}$

$y^{\prime}(1)=1$ gives $B\frac{\cos^2{\left(\sqrt{\frac{3}{2}}\right)}+\sin^2{\left(\sqrt{\frac{3}{2}}\right)}}{\cos{\left(\sqrt{\frac{3}{2}}\right)}} = \sqrt{\frac{2}{3}}$

so $B=\sqrt{\frac{2}{3}}\cos{\left(\sqrt{\frac{3}{2}}\right)},\     A=\sqrt{\frac{2}{3}}\sin{\left(\sqrt{\frac{3}{2}}\right)}$

$y(x)=\sqrt{\frac{2}{3}}\left[\sin{\left(\sqrt{\frac{3}{2}}\right)}\cos{\left(\sqrt{\frac{3}{2}}x\right)}+\cos{\left(\sqrt{\frac{3}{2}}\right)}\sin{\left(\sqrt{\frac{3}{2}}x\right)}\right]$

$=\sqrt{\frac{2}{3}}\sin{\left(\sqrt{\frac{3}{2}}(x-1)\right)}$

When $x=2$

$y = \sqrt{\frac{2}{3}}\sin{\left(\sqrt{\frac{3}{2}}\right)}$

Note: the algebra in this question would have been easier if we started by writing the general solution as

$y(x)=K\sin{\left(\sqrt{\frac{3}{2}}x+\phi\right)}$

Try it!
### Second Order - Q12
Solve the second order differential equation

$2y^{\prime\prime}(x)+y^{\prime}(x)+3y(x)=0,$

$y(0)=1,\  y^{\prime}(0)=1$

Ansatz: $y = e^{\lambda x}$

Auxiliary equation: $2\lambda^2+\lambda + 3=0$

The roots of this equation are

$\lambda = \frac{1}{4}(-1\pm i\sqrt{23})$

The general solution is

$y(x)=e^{-x/4}\left[A\cos{\left(\frac{\sqrt{23}}{4}x\right)}+B\sin{\left(\frac{\sqrt{23}}{4}x\right)}\right]$

$y^{\prime}(x) = e^{-x/4}\left[\left(-\frac{1}{4}A+\frac{\sqrt{23}}{4}B\right)\cos{\left(\frac{\sqrt{23}}{4}x\right)}+\left(-\frac{1}{4}B-\frac{\sqrt{23}}{4}A\right)\sin{\left(\frac{\sqrt{23}}{4}x\right)}\right]$

Applying the initial conditions

$y(0)=1$ gives $A=1$

$y^{\prime}(0)=1$ gives $-\frac{1}{4}A+\frac{\sqrt{23}}{4}B = 1$

so $B=\frac{5}{\sqrt{23}}$

$y(x)=e^{-x/4}\left[\cos{\left(\frac{\sqrt{23}}{4}x\right)}+\frac{5\sqrt{23}}{23}\sin{\left(\frac{\sqrt{23}}{4}x\right)}\right]$

When $x=1$

$y = e^{-1/4}\left[\cos{\left(\frac{\sqrt{23}}{4}\right)}+\frac{5\sqrt{23}}{23}\sin{\left(\frac{\sqrt{23}}{4}\right)}\right]$








