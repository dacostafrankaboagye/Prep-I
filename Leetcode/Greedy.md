
1221. Split a String in Balanced Strings

Balanced strings are those that have an equal quantity of 'L' and 'R' characters.

Given a balanced string s, split it into some number of substrings such that:

Each substring is balanced.
Return the maximum number of balanced strings you can obtain.


Example 1:
  
  Input: s = "RLRRLLRLRL"
  Output: 4
  Explanation: s can be split into "RL", "RRLL", "RL", "RL", 
  each substring contains same number of 'L' and 'R'.

Example 2:

  Input: s = "RLRRRLLRLL"
  Output: 2
  Explanation: s can be split into "RL", "RRRLLRLL", each substring contains same number of 'L' and 'R'.

Note that s cannot be split into "RL", "RR", "RL", "LR", "LL", because the 
2nd and 5th substrings are not balanced.

Example 3:

  Input: s = "LLLLRRRR"
  Output: 1
  Explanation: s can be split into "LLLLRRRR".
 
Constraints:

  2 <= s.length <= 1000
  s[i] is either 'L' or 'R'.
  s is a balanced string.

```java

class Solution {
    static int checkBalance(int balance, int result){
        if(balance == 0){
            return result +1;
        }
        return result;
    }
    public int balancedStringSplit(String s) {
        int balance = 0;
        int result  = 0;
        for(char i : s.toCharArray()){
            if(i == 'L'){
                balance -=1;
            }else{
                balance +=1;
            }
            // or // balance += (i == 'L') ? 1 : -1
            result = checkBalance(balance, result);
        }
        return result;
        
    }
}


// Alternative

class Solution {
    public int balancedStringSplit(String s) {
        int result = 0;
        int sum = 0;
        
        for (char letter : s.toCharArray()) {
            sum += (letter == 'R' ? 1 : -1);
            if (sum == 0) {
                result++;
            }
        }
        
        return result;
    }

```
