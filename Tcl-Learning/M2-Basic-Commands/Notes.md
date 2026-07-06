# Notes 
The commands and syntax for Tcl learning are for Windows users. Mac users should modify accordingly. 

## Getting Started 
Open the command prompt. Enter `tclsh` to start the Tcl shell. <br>
If `%` sign appears, then Tcl shell has started. Else check if tclsh is added to `PATH` system variable by below steps - <br>
1. Press Win + S
2. Search for Environment Variables
3. Open Edit the system environment variables
4. Click Environment Variables
5. Under System variables, select Path
6. Click Edit
7. If you see an entry containing something like: ...\Magicsplat\... or the folder containing tclsh.exe, then Tcl is in PATH. If Tcl is not in PATH, use Windows Search and look for "tclsh.exe", get its path, and add it as system variables using 1 to 6 steps above.<br>

Once Tcl shell has started and `%` sign appears, enter the below command to print a string- <br>
`puts "hello vlsi!"` <br>
The output should be : `hello vlsi!` <br>
To exit the Tcl shell, enter `exit`

## 1. What is a Command?

Everything in Tcl is essentially a **command**.

General syntax:

```tcl
command arg1 arg2 arg3 ...
```

Example:

```tcl
puts Hello
```

* `puts` → command
* `Hello` → argument

---

## 2. A Tcl line is a command

Each line is interpreted as one command.

```tcl
puts "First line"
puts "Second line"
```

Output:

```text
First line
Second line
```

---

## 3. Words are separated by spaces

```tcl
puts Hello World
```

This gives an error because Tcl treats `Hello` and `World` as separate arguments.

Correct:

```tcl
puts "Hello World"
```

---

## 4. Command substitution using `[ ]`

Tcl executes commands inside square brackets first.

```tcl
puts [expr 5 + 3]
```

Execution order:

1. Execute `expr 5 + 3`
2. Result becomes `8`
3. Execute:

```tcl
puts 8
```

Output:

```text
8
```

This is one of the most important Tcl concepts.

---

## 5. Comments

Single line comment:

```tcl
# This is a comment
puts Hello
```

---

## 6. Multi-line commands using `\`

Backslash continues command to next line.

```tcl
puts "This is a very long \
message"
```

Output:

```text
This is a very long message
```

---

## 7. Multiple commands in one line using `;`

```tcl
puts Hello; puts World
```

Output:

```text
Hello
World
```

---

## 8. Curly braces `{}`

Used to group words together and prevent substitutions.

```tcl
puts {Hello $name}
```

Output:

```text
Hello $name
```

Variable substitution does not happen inside braces.

---

## 9. Double quotes `" "`

Allow substitutions.

```tcl
set name Vibhu
puts "Hello $name"
```

Output:

```text
Hello Vibhu
```

---

## 10. Important beginner commands

### puts

Prints output.

```tcl
puts "Hello"
```

---

### set

Assigns or retrieves variable values.

```tcl
set x 10
puts $x
```

---

### expr

Performs calculations.

```tcl
puts [expr 10 + 20]
```

---

### exit

Exits Tcl shell.

```tcl
exit
```

---

## Quick Summary

| Concept              | Example             |
| -------------------- | ------------------- |
| Command syntax       | `command arg1 arg2` |
| Print output         | `puts "Hello"`      |
| Variable assignment  | `set x 10`          |
| Arithmetic           | `expr 5 + 3`        |
| Command substitution | `[expr 5+3]`        |
| Multiple commands    | `cmd1 ; cmd2`       |
| Comment              | `# comment`         |
| Line continuation    | `\`                 |
| No substitution      | `{}`                |
| Allow substitution   | `""`                |


# VLSI Relevance

Among all concepts in this module, the most frequently used in EDA scripts are:

* `set`
* `puts`
* `expr`
* command substitution `[ ]`
* braces `{ }`
* quotes `" "`

You will see these in almost every Tcl script written for tools such as synthesis, STA, P&R and DFT.




