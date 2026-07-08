# Practice Questions

## Easy

### Q1

Create a variable `name` with value `"Vibhu"` and print it.

---

### Q2

Create a variable `count` with value `15` and print it.

---

### Q3

Create variables `tool = Innovus` and `version = 23.1`. Print:

```text
Innovus Version 23.1
```

---

## Medium

### Q4

Create variables `a = 20` and `b = 30`. Print their sum.

---

### Q5

Predict the output.

```tcl
set x 10
set y $x
set x 20

puts $y
puts $x
```

---

### Q6

Predict the output.

```tcl
set city Delhi
puts city
puts $city
```

---

## Hard

### Q7

Predict the output.

```tcl
set x 5
puts [expr $x * 4 + 2]
```

---

### Q8

Write Tcl code to calculate the area of a rectangle using variables `length = 25` and `width = 8`.

Print:

```text
Area = 200
```

---

### Q9

Predict the output.

```tcl
set a 5
set b 10
set c [expr $a + $b]

puts "Sum = $c"
```

---

# Solutions

## Solution to Q1

```tcl
set name "Vibhu"
puts $name
```

---

## Solution to Q2

```tcl
set count 15
puts $count
```

---

## Solution to Q3

```tcl
set tool Innovus
set version 23.1

puts "$tool Version $version"
```

---

## Solution to Q4

```tcl
set a 20
set b 30

puts [expr $a + $b]
```

Output

```text
50
```

---

## Solution to Q5

Output

```text
10
20
```

Explanation:

`y` stores a copy of `x`'s value (`10`). Updating `x` later does not affect `y`.

---

## Solution to Q6

Output

```text
city
Delhi
```

Explanation:

* `puts city` prints the literal text `city`.
* `puts $city` prints the value stored in the variable.

---

## Solution to Q7

Output

```text
22
```

Calculation:

```
5 × 4 + 2 = 22
```

---

## Solution to Q8

```tcl
set length 25
set width 8

set area [expr $length * $width]

puts "Area = $area"
```

---

## Solution to Q9

Output

```text
Sum = 15
```

Explanation:

`expr` evaluates `5 + 10` to `15`, which is stored in `c`.

---

**Keep hustling !**
