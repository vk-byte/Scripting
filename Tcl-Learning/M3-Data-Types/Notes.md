# M3: Data Types (Tcl)

## 1. Tcl Philosophy: "Everything is a String"

Unlike C, Java or Python, Tcl internally stores almost everything as a string.

Example:

```tcl
set x 10
set name "Vibhu"
set nums {1 2 3}
```

Internally, Tcl initially sees all of these as strings.

The command being used decides how to interpret the value.

---

## 2. Integer

Whole numbers.

```tcl
set a 10
set b -25
```

Examples:

```tcl
puts [expr $a + 5]
```

Output:

```text
15
```

---

## 3. Floating Point Numbers

Numbers containing decimal points.

```tcl
set pi 3.14
set voltage 1.8
```

Example:

```tcl
puts [expr $pi * 2]
```

Output:

```text
6.28
```

---

## 4. String

Text data.

```tcl
set name "Vibhu"
set tool "PrimeTime"
```

Example:

```tcl
puts "Tool used is $tool"
```

Output:

```text
Tool used is PrimeTime
```

---

## 5. Boolean Values

Tcl accepts several representations for true and false.

### True values

```text
1
true
yes
on
```

### False values

```text
0
false
no
off
```

Example:

```tcl
set enabled true
```

---

## 6. List

Ordered collection of values.

```tcl
set cells {AND2 OR2 XOR2 INV}
```

This is treated as a list when list commands are used.

Example:

```tcl
llength $cells
```

Output:

```text
4
```

Lists will be studied in detail in M9.

---

## 7. Array

Key-value storage similar to dictionaries.

```tcl
set timing(slack) -0.05
set timing(freq) 500
```

Access:

```tcl
puts $timing(slack)
```

Arrays are covered in M10.

---

## 8. Dictionary

Modern key-value data structure.

```tcl
set employee {name Vibhu age 25}
```

Access:

```tcl
dict get $employee name
```

Dictionaries are covered in M11.

---

## 9. How Tcl Determines Type

Tcl decides the type based on the command used.

Example:

```tcl
set x 10
```

As text:

```tcl
puts $x
```

As number:

```tcl
expr $x + 5
```

As string:

```tcl
string length $x
```

Same value, different interpretation.

---

## 10. Type Conversion Happens Automatically

Example:

```tcl
set x "10"
puts [expr $x + 5]
```

Output:

```text
15
```

Tcl automatically converts `"10"` into integer `10`.

---

## 11. Invalid Conversion

```tcl
set x "hello"
puts [expr $x + 5]
```

Output:

```text
can't use non-numeric string as operand
```

---

## Quick Summary

| Data Type  | Example         |
| ---------- | --------------- |
| Integer    | `10`            |
| Float      | `3.14`          |
| String     | `"Hello"`       |
| Boolean    | `true`, `false` |
| List       | `{a b c}`       |
| Array      | `arr(key)`      |
| Dictionary | `dict get`      |

---

# VLSI Relevance

In VLSI automation scripts you will most commonly work with:

* Integers → counts, indices, iterations
* Floats → delay, slack, frequency, area
* Strings → pin names, cell names, paths
* Lists → collections of cells, nets and ports
* Dictionaries and arrays → storing reports and attributes

Example:

```tcl
set slack -0.083
set endpoint U1234/D
set violating_paths {path1 path2 path3}
```

These kinds of data structures appear constantly in synthesis, STA and physical design scripts.
