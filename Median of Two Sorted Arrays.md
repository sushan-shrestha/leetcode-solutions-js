# MEDIAN OF TWO SORTED ARRAYS

## QUESTION

Given two sorted arrays nums1 and nums2 of size m and n respectively, return the median of the two sorted arrays.

The overall run time complexity should be O(log (m+n)).

## EXAMPLES

### Example 1:

    Input: nums1 = [1,3], nums2 = [2]
    Output: 2.00000
    Explanation: merged array = [1,2,3] and median is 2.

### Example 2:

    Input: nums1 = [1,2], nums2 = [3,4]
    Output: 2.50000
    Explanation: merged array = [1,2,3,4] and median is (2 + 3) / 2 = 2.5.

## Constraints:

    - nums1.length == m
    - nums2.length == n
    - 0 <= m <= 1000
    - 0 <= n <= 1000
    - 1 <= m + n <= 2000
    - -10^6 <= nums1[i], nums2[i] <= 10^6

## ANSWER:

    /**
    * @param {number[]} nums1
    * @param {number[]} nums2
    * @return {number}
    */

    var findMedianSortedArrays = function(nums1, nums2) {


        nums1 = nums1.concat(nums2);

        nums1.sort((a,b) => a-b)

        const initialValue = 0;
        const sumWithInitial = nums1.reduce(
            (previousValue, currentValue) => previousValue + currentValue,
            initialValue
        );

        const median = nums1.length / 2;

        if(nums1.length % 2 !== 0) return nums1[Math.ceil(median) -1 ];

        return ((nums1[Math.floor(median) - 1] + nums1[Math.floor(median)]) /2)



    };
