# REVERSE INTEGER

## QUESTION

Given a signed 32-bit integer x, return x with its digits reversed. If reversing x causes the value to go outside the signed 32-bit integer range [-2^31, 2^31 - 1], then return 0.

Assume the environment does not allow you to store 64-bit integers (signed or unsigned).

## EXAMPLES

### Example 1:

    Input: x = 123
    Output: 321

### Example 2:

    Input: x = 120
    Output: 21

### Example 3:

    Input: x = -123
    Output: -321

## ANSWER:

    /**
    * @param {number} x
    * @return {number}
    */
    var reverse = function(x) {

        let reverseNum = 0 ;



        while(x != 0){
            var currNum = x % 10;
            reverseNum = reverseNum * 10 + currNum;
            x = (x - currNum) / 10;
        }

        if(Math.abs(reverseNum) > Math.pow(2,31) ){
            return 0;
        }

        return (reverseNum )
    };
