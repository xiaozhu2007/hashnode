---
title: "How to Get the Number of Days in a Month in Python"
seoTitle: "How to Get the Number of Days in a Month in Python"
seoDescription: "We can use this method to even check whether a year is a leap year or not."
datePublished: Sat Mar 04 2023 00:37:59 GMT+0000 (Coordinated Universal Time)
cuid: clf4o2w0b000109mb3n5vcofq
slug: how-to-get-the-number-of-days-in-a-month-in-python
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1678581448791/4189a298-d1d9-4818-a0c0-f77ba11740c6.png
tags: python, how-to, howtos

---

If you need to get the number of days in a month in [Python](https://www.python.org/?from=hackpig520.hashnode.dev), you can do that quite quickly.

We are going to do that using the `calendar` module.

First, import the `calendar` module and then call the method `monthrange()` which returns the `first_day` and also the `number_of_days` in a month.

Let us see this example:

```python
 import calendar
​
 # Get current month
 _, number_of_days = calendar.monthrange(2022, 12)
​
 print(number_of_days)  # 31
```

%%[post-xxxads] 

We can use this method to even check whether a year is a leap year or not:

```python
 import calendar
 ​
 # Get current month
 year = 2023
 ​
 while True:
     _, number_of_days = calendar.monthrange(year, 2)
 ​
     if number_of_days == 29:
         print("February has 29 days in {}".format(year))
         break
 ​
     year += 1
```

I hope you find this useful.

%%[post-xxxads]