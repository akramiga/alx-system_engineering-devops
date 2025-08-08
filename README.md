# 0x03. Shell, init files, variables and expansions

This project focuses on shell scripting, specifically working with variables, expansions, aliases, and arithmetic operations in Bash.



# a script that creates an alias:


**Explanation:** This creates an alias that replaces the `ls` command with `rm *`. When sourced, typing `ls` will execute `rm *` instead, which deletes all files in the current directory.

---

### 1. Hello you
**File:** `1-hello_you`

 script that prints "hello user", where user is the current Linux user.


**Explanation:** Uses the `$USER` environment variable to get the current username and prints a greeting message.

---

### 2. The path to success is to take massive, determined action
**File:** `2-path`


**Explanation:** Appends `/action` to the existing PATH variable, making it the last directory searched for executables.

---

### 3. If the path be beautiful, let us not ask where it leads
**File:** `3-paths`

script that counts the number of directories in the PATH.



**Explanation:** 
- `tr -s ':' '\n'` replaces colons with newlines, converting PATH into separate lines
- `wc -l` counts the number of lines, giving us the directory count

---

### 4. Global variables
**File:** `4-global_variables`

 a script that lists environment variables.

**Explanation:** The `printenv` command displays all environment variables and their values.

---

### 5. Local variables
**File:** `5-local_variables`

a script that lists all local variables, environment variables, and functions.
**Explanation:** The `set` command without arguments displays all shell variables (local and environment) and functions.

---

### 6. Local variable
**File:** `6-create_local_variable`

a script that creates a new local variable

**Explanation:** Creates a local variable `BEST` with the value "School". This variable is only available in the current shell session.

---

### 7. Global variable
**File:** `7-create_global_variable`

 a script that creates a new global variable

**Explanation:** Creates and exports the variable `BEST`, making it available to child processes as an environment variable.

---

### 8. Every addition to true knowledge is an addition to human power
**File:** `8-true_knowledge`

 a script that prints the result of adding 128 to the value stored in the environment variable `TRUEKNOWLEDGE`.

**Explanation:** Uses arithmetic expansion `$(())` to add 128 to the value of the `TRUEKNOWLEDGE` environment variable.

---

### 9. Divide and rule
**File:** `9-divide_and_rule`

a script that prints the result of `POWER` divided by `DIVIDE`.

**Explanation:** Uses arithmetic expansion to divide the `POWER` environment variable by the `DIVIDE` environment variable.

---

### 10. Love is anterior to life, posterior to death, initial of creation, and the exponent of breath
**File:** `10-love_exponent_breath`

 a script that displays the result of `BREATH` to the power of `LOVE`.

**Explanation:** Uses the exponentiation operator `**` in arithmetic expansion to calculate BREATH raised to the power of LOVE.

---

### 11. There are 10 types of people in the world -- Those who understand binary, and those who don't
**File:** `11-binary_to_decimal`

 a script that converts a number from base 2 to base 10. The binary number is stored in the environment variable `BINARY`.

**Explanation:** Uses base conversion in arithmetic expansion. The `2#` prefix tells the shell to interpret the following number as base 2.

---

### 12. Combination
**File:** `12-combinations`

a script that prints all possible combinations of two letters (aa to zz), except "oo". Must be alpha ordered and contain maximum 64 characters.



**Explanation:**
- `{a..z}{a..z}` generates all combinations from aa to zz
- `tr ' ' '\n'` converts spaces to newlines (one combination per line)
- `grep -v "oo"` excludes the "oo" combination

---

### 13. Floats
**File:** `13-print_float`

 a script that prints a number with two decimal places. The number is stored in the environment variable `NUM`.


**Explanation:** Uses `printf` with format specifier `%.2f` to display the number with exactly 2 decimal places, followed by a newline.

