```
class HelloWorld {
    public static void main(String[] args) {
        int n1 = 100;
        int n2 = 400;
        int x1, n ;
        for(int i = n1+1;i<n2;i++){
            int x = i;
            n = 0;
            while(x!=0){
                x=x/10;
                ++n; 
            }
            int pow_sum = 0;
            x = i;
            while(x!=0){
                int digit = x % 10;
                pow_sum += Math.pow(digit,n);
                x=x/10;
            }
            if(pow_sum == i ){
                System.out.print(i + " ");
            }
        }
  }
}
```

```
153 370 371
```
 
### Steps in the Program:
1. **Range Definition:**  
   The program starts by calling the `findArmstrong` function with the range `100` to `400`.

2. **Loop through Range:**  
   The function loops through all numbers from `low + 1` to `high - 1`. Here, it loops through numbers from `101` to `399` (because the loop is exclusive of `high`).

3. **Count Digits:**  
   For each number, the program counts how many digits the number has. This count is stored in variable `n`.

4. **Sum of Powers of Digits:**  
   The program then calculates the sum of each digit raised to the power of `n`.

5. **Check Armstrong Condition:**  
   If the sum equals the original number, it prints the number because it's an Armstrong number.

### Detailed Iteration Example:
Let's go through a detailed example with one of the iterations:

#### Input Range: 100 to 400
We'll start with the first number in the range, `101`.

- **Iteration 1:**
  - **Step 1:** Set `i = 101`
  - **Step 2: Calculate number of digits (`n`)**
    - Initialize `x = 101`, `n = 0`.
    - While `x != 0`:
      - `x /= 10` → `x = 10`, `n = 1`
      - `x /= 10` → `x = 1`, `n = 2`
      - `x /= 10` → `x = 0`, `n = 3`
    - Now, `n = 3` (101 has 3 digits).
  - **Step 3: Calculate sum of nth power of digits**
    - Initialize `x = 101`, `pow_sum = 0`.
    - While `x != 0`:
      - `digit = x % 10` → `digit = 1`, `x /= 10` → `x = 10`
        - `pow_sum += Math.pow(1, 3)` → `pow_sum = 1`
      - `digit = x % 10` → `digit = 0`, `x /= 10` → `x = 1`
        - `pow_sum += Math.pow(0, 3)` → `pow_sum = 1`
      - `digit = x % 10` → `digit = 1`, `x /= 10` → `x = 0`
        - `pow_sum += Math.pow(1, 3)` → `pow_sum = 2`
    - Now, `pow_sum = 2`.
  - **Step 4: Check if `pow_sum` equals `i`**
    - Compare `pow_sum (2)` with `i (101)`:
      - Since `pow_sum != i`, 101 is **not** an Armstrong number.

- **Iteration 2:**
  - Next, consider `i = 153` (another number in the range):
  - **Step 1:** Set `i = 153`
  - **Step 2: Calculate number of digits (`n`)**
    - Initialize `x = 153`, `n = 0`.
    - While `x != 0`:
      - `x /= 10` → `x = 15`, `n = 1`
      - `x /= 10` → `x = 1`, `n = 2`
      - `x /= 10` → `x = 0`, `n = 3`
    - Now, `n = 3` (153 has 3 digits).
  - **Step 3: Calculate sum of nth power of digits**
    - Initialize `x = 153`, `pow_sum = 0`.
    - While `x != 0`:
      - `digit = x % 10` → `digit = 3`, `x /= 10` → `x = 15`
        - `pow_sum += Math.pow(3, 3)` → `pow_sum = 27`
      - `digit = x % 10` → `digit = 5`, `x /= 10` → `x = 1`
        - `pow_sum += Math.pow(5, 3)` → `pow_sum = 27 + 125 = 152`
      - `digit = x % 10` → `digit = 1`, `x /= 10` → `x = 0`
        - `pow_sum += Math.pow(1, 3)` → `pow_sum = 152 + 1 = 153`
    - Now, `pow_sum = 153`.
  - **Step 4: Check if `pow_sum` equals `i`**
    - Compare `pow_sum (153)` with `i (153)`:
      - Since `pow_sum == i`, 153 **is** an Armstrong number and it gets printed.

This process repeats for every number in the range from `101` to `399`. Numbers like `153`, `370`, `371`, and `407` are found to be Armstrong numbers in this range, so they will be printed.
