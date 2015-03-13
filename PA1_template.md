# Reproducible Research: Peer Assessment 1


## Loading and preprocessing the data


```r
## File with all data
Steps <- read.csv("activity.csv")

## Agregatted by date
dataTotal <- aggregate(. ~ date, data=Steps, sum)

## total number of days with data to use on hist
lines <- nrow(dataTotal)
```

## What is mean total number of steps taken per day?

```r
## Asked histogram of steps per day
hist(dataTotal$steps, breaks = lines, col = "red", main = "Histogram Total Steps per day", xlab = "" )
```

![](PA1_template_files/figure-html/unnamed-chunk-2-1.png) 

```r
## mean of the steps per day
mean(dataTotal$steps)
```

```
## [1] 10766.19
```

```r
## median of the steps per day
median(dataTotal$steps)
```

```
## [1] 10765
```



## What is the average daily activity pattern?

```r
## Asked histogram of steps per day
hist(dataTotal$steps, breaks = lines, col = "red", main = "Histogram Total Steps per day", xlab = "" )
```

![](PA1_template_files/figure-html/unnamed-chunk-3-1.png) 

```r
## mean of the steps per day
mean(dataTotal$steps)
```

```
## [1] 10766.19
```

```r
## median of the steps per day
median(dataTotal$steps)
```

```
## [1] 10765
```


## Imputing missing values



## Are there differences in activity patterns between weekdays and weekends?
