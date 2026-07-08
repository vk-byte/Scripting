# M4: Variables (Tcl)

## 1. What is a Variable?

A variable is a named storage location used to store data.

Examples:

```tcl
set name "Vibhu"
set age 25
set slack -0.08
```

Here,

* `name`, `age`, `slack` → Variable names
* `"Vibhu"`, `25`, `-0.08` → Stored values

---

# 2. Creating a Variable

Tcl uses the `set` command.

Syntax:

```tcl
set variableName value
```

Example:

```tcl
set x 10
```

This creates variable `x` and stores `10`.

---

# 3. Reading a Variable

To access a variable, prefix it with `$`.

Example:

```tcl
set x 10
puts $x
```

Output

```text
10
```

Think of:

* `x` → Variable name
* `$x` → Value inside the variable

---

# 4. Updating a Variable

Assign a new value using `set`.

```tcl
set count 5
set count 10
puts $count
```

Output

```text
10
```

The old value is replaced.

---

# 5. Variables Can Store Any Type

Integer

```tcl
set num 100
```

Float

```tcl
set voltage 1.2
```

String

```tcl
set tool "Innovus"
```

List

```tcl
set gates {AND OR XOR}
```

---

# 6. Variable Names

Valid examples

```tcl
set count 10
set total_area 200
set slack_value -0.03
set x1 5
```

Avoid names beginning with numbers.

Incorrect

```tcl
set 2count 10
```

---

# 7. Variable Substitution

Whenever Tcl sees `$variable`, it replaces it with its value.

Example

```tcl
set tool PrimeTime
puts "Tool = $tool"
```

Output

```text
Tool = PrimeTime
```

---

# 8. Variables Inside Expressions

```tcl
set a 15
set b 20

puts [expr $a + $b]
```

Output

```text
35
```

Always use `$` inside `expr`.

---

# 9. Copying Variables

```tcl
set x 50
set y $x

puts $y
```

Output

```text
50
```

The value of `x` is copied into `y`.

---

# 10. Multiple Variables

```tcl
set width 10
set height 20
set area [expr $width * $height]

puts $area
```

Output

```text
200
```

---

# 11. Variables Inside Strings

```tcl
set cell NAND2_X1
set delay 0.12

puts "Cell $cell has delay $delay ns"
```

Output

```text
Cell NAND2_X1 has delay 0.12 ns
```

---

# 12. Common Beginner Mistakes

### Mistake 1

```tcl
puts x
```

Output

```text
x
```

Correct

```tcl
puts $x
```

---

### Mistake 2

```tcl
expr a + b
```

Correct

```tcl
expr $a + $b
```

---

### Mistake 3

Using an undefined variable.

```tcl
puts $count
```

If `count` has never been created, Tcl reports an error.

---

# Quick Summary

| Task            | Syntax         |
| --------------- | -------------- |
| Create variable | `set x 10`     |
| Read variable   | `$x`           |
| Update variable | `set x 20`     |
| Print value     | `puts $x`      |
| Arithmetic      | `expr $a + $b` |
| Copy value      | `set y $x`     |

---

# VLSI Relevance

Variables are the backbone of every Tcl automation script. They are commonly used to store:

* File names (`report.rpt`, `design.v`)
* Design names (`top_module`)
* Cell and pin names (`U123/A`)
* Slack, delay, area, frequency, and power values
* Loop counters and command results

Example:

```tcl
set design cpu_top
set report timing.rpt
set slack -0.072

puts "Worst slack for $design is $slack ns"
```

As your scripts become larger (especially in PrimeTime, Innovus, ICC2, Genus, or Design Compiler), variables will be used in almost every line of code.
