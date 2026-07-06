# Practice Questions

## Easy Level

### Q1

Create an integer variable `age` having value `25` and print it.

---

### Q2

Create a floating point variable `voltage` having value `1.2`.

---

### Q3

Create a string variable `tool` containing `Innovus`.

---

## Medium Level

### Q4

Predict the output.

```tcl
set x "10"
puts [expr $x + 15]
```
---

### Q5

Predict the output.

```tcl
set x 12345
puts [string length $x]
```
---

### Q6

Create a list containing:

```text
NAND NOR XOR BUF
```

and print the number of elements.

---

## Hard Level

### Q7

Predict the output.

```tcl
set x "20"
puts [expr $x / 2]
puts [string length $x]
```
---

### Q8

Predict the output.

```tcl
set x "abc"
puts [string length $x]
puts [expr $x + 1]
```
---

### Q9

What type is `123` in Tcl?

---
# Solutions

### Q1

```tcl
set age 25
puts $age
```
---

### Q2

```tcl
set voltage 1.2
puts $voltage
```
---
### Q3

```tcl
set tool "Innovus"
puts $tool
```
---
### Q4

Output:

```text
25
```

Reason:
Tcl converts `"10"` into integer automatically.

---

### Q5

Output:

```text
5
```

Reason:
The number is treated as a string by `string length`.

---

### Q6

```tcl
set gates {NAND NOR XOR BUF}
puts [llength $gates]
```

Output:

```text
4
```
---

### Q7

Output:

```text
10
2
```

The first command treats `x` as a number.
The second command treats `x` as text.

### Q8

Output:

```text
3
can't use non-numeric string as operand
```
---
### Q9

There is no permanently fixed type attached to `123`.

Depending on the command, Tcl may treat it as:

* Integer
* String
* List element
* Dictionary value

This is one of the defining characteristics of Tcl.

**Keep Grinding !**

