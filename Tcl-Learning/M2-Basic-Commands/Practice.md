# Practice Questions

## Easy Level

### Q1

Print your name using `puts`.

---

### Q2

Print two messages on separate lines.

---

### Q3

Print two messages using only one line of code.

---

## Medium Level

### Q4

Store value `25` in variable `x` and print it.

---

### Q5

Calculate and print `15 + 20`.

---

### Q6

Print:

```text
Value of x is 50
```

using variable substitution.

---

## Hard Level

### Q7

Predict the output.

```tcl
set x 10
puts {$x}
puts "$x"
```

---

### Q8

Predict the output.

```tcl
puts [expr 2 + [expr 3 + 4]]
```


---

### Q9

Write a single line Tcl command that prints:

```text
Result is 30
```

without directly writing `30`.

---
# Solutions
### Q.1
```tcl
puts "Vibhu"
```
---
### Q.2

```tcl
puts "Learning Tcl"
puts "For VLSI Automation"
```
---

### Q.3

```tcl
puts "Hello"; puts "World"
```
---

### Q.4

```tcl
set x 25
puts $x
```
---

### Q.5

```tcl
puts [expr 15 + 20]
```
---
### Q.6 
```tcl
set x 50
puts "Value of x is $x"
```
### Q.7

Output:

```text
$x
10
```

Reason:

* `{}` disables substitution.
* `""` allows substitution.

### Q.8

Inner command executes first:

```tcl
expr 3 + 4 -> 7
expr 2 + 7 -> 9
```

Output:

```text
9
```
### Q.9

```tcl
puts "Result is [expr 10 + 20]"
```

Output:

```text
Result is 30
```

**Keep practicing, This is just the beginning !**
