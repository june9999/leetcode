### Two Sum

- [Hash](./src/001_twosum.js) ★★

```javascript
var twoSum = function (nums, target) {
  // brute force
  // let index = 0
  // for (index = 0; index < nums.length;index++) {
  //     let searchValue = target - nums[index]
  //     for (let i = index + 1; i < nums.length; i++) {
  //         if (searchValue === nums[i]) {
  //             return [index,i]
  //         }
  //     }
  // }
  let hashtable = new Map();
  for (let i = 0; i < nums.length; i++) {
    if (hashtable.has(target - nums[i])) {
      return [hashtable.get(target - nums[i]), i];
    }
    hashtable.set(nums[i], i);
  }
  return [];
};
```
