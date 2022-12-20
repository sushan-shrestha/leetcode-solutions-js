# PALINDROME NUMBER

## QUESTION

Given an integer x, return true if x is a
palindrome
, and false otherwise.

## EXAMPLES

### Example 1:

    Input: x = 121
    Output: true
    Explanation: 121 reads as 121 from left to right and from right to left.

### Example 2:

    Input: x = -121
    Output: false
    Explanation: From left to right, it reads -121. From right to left, it becomes 121-. Therefore it is not a palindrome.

### Example 3:

    Input: x = 10
    Output: false
    Explanation: Reads 01 from right to left. Therefore it is not a palindrome.

## ANSWER:

    /**
    * @param {number} x
    * @return {boolean}
    */
    var isPalindrome = function(x) {
        let num = x;
        console.log(x);
        let reverseNum = 0 ;
        while(num > 0){
            var currNum = num % 10;
            reverseNum = reverseNum * 10 + currNum;
            num = (num - currNum) / 10;
        }

        return (reverseNum === x)
    };
