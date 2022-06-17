## Two Sum
Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target.
You may assume that each input would have exactly one solution, and you may not use the same element twice.
You can return the answer in any order.

```
Input: nums = [2,7,11,15], target = 9
Output: [0,1]
Explanation: Because nums[0] + nums[1] == 9, we return [0, 1].
```

```php
class Solution {

    /**
     * @param Integer[] $nums
     * @param Integer $target
     * @return Integer[]
     */
    function twoSum($nums, $target) {
        
        $length = count($nums) - 1;
        
        for ($i = 0; $i <= $length; $i++) {
            for ($j = $i + 1; $j <= $length; $j++) {
                $sumResult = $nums[$i] + $nums[$j];
                if ($sumResult === $target) {
                    return [$i, $j];
                }
            }
        }
        return [];
        
    }
}
```
