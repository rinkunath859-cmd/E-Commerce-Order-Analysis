# DAX Measures

## Total Sales

```DAX
Total Sales =
SUM(Orders[Order Value])
```

---

## Total Orders

```DAX
Total Orders =
COUNT(Orders[Order ID])
```

---

## Total Customers

```DAX
Total Customers =
DISTINCTCOUNT(Orders[Customer ID])
```

---

## Target Achievement %

```DAX
Achievement % =
DIVIDE([Total Sales],[Sales Target])
```

---

## Sales Gap

```DAX
Sales Gap =
[Sales Target]-[Total Sales]
```

---

## Target Status

```DAX
Target Status =
SWITCH(
TRUE(),
[Total Sales]<[Sales Target],"Target Not Met",
[Total Sales]=[Sales Target],"Target Met",
"Exceeded Target")
```
