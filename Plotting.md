gnuR
====

Basic plotting
--------------
Includes a nice theme and showcases some often-used possibilities of ggplot2 

### Legend Positioning


```r
a = c(1, 2, 3)
b = c(4, 5, 2)
df = data.frame(cbind(a, b))
require(ggplot2)
```

```
## Loading required package: ggplot2
```

```r
theme_set(theme_bw())
p = ggplot(df)
p = p + geom_line(aes(x = a, y = b))
p = p + geom_step(aes(x = a, y = b, color = b))
p = p + geom_point(aes(x = a, y = b, size = a))
print(p)
```

![plot of chunk test](figure/test1.png) 

```r

p = p + theme(legend.position = c(0.5, 0.5))
print(p)
```

![plot of chunk test](figure/test2.png) 

```r

p = p + theme(legend.position = "top")
print(p)
```

![plot of chunk test](figure/test3.png) 

```r

p = p + theme(legend.position = "bottom")
print(p)
```

![plot of chunk test](figure/test4.png) 





