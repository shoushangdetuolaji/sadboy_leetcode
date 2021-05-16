# sadboypark_leetcode

> 每日刷题
>
> b站： [CatRacket](https://space.bilibili.com/1553592118)
>
> 感谢猫打球姐姐讲解js算法题 
>
> 以下的题目来源与leetcode的
>
> 思路都是根据猫打球姐姐的思维！

## 1. Two Sum

```
给定一个整数数组 nums 和一个整数目标值 target，请你在该数组中找出 和为目标值 的那 两个 整数，并返回它们的数组下标。

你可以假设每种输入只会对应一个答案。但是，数组中同一个元素在答案里不能重复出现。

你可以按任意顺序返回答案。

Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target.

You may assume that each input would have exactly one solution, and you may not use the same element twice.

You can return the answer in any order.


示例 1：

输入：nums = [2,7,11,15], target = 9
输出：[0,1]
解释：因为 nums[0] + nums[1] == 9 ，返回 [0, 1] 。

来源：力扣（LeetCode）
链接：https://leetcode-cn.com/problems/two-sum
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。
```

```javascript
/**
 * @param {number[]} nums
 * @param {number} target
 * @param {number[]}
 */

var twoSum = function(nums, target) {
  var map = {};
  for(var i = 0; i<nums.length; i++) {
    var m = target - nums[i];
    if(map[m] !== undefined) {
      return [map[m], i];
    }
    map[nums[i]] = i;
  }
}
```

