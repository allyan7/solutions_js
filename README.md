# Longest Substring Without Repeating Characters

Given a string s, find the length of the **longest substring** without duplicate characters.

## Examples
**Example 1:**
> **Input:** s = "abcabcbb"  
> **Output**: 3  
> **Explanation:** The answer is "abc", with the length of 3.

**Example 2:**
> **Input:** s = "bbbbb"  
> **Output:** 1  
> **Explanation:** The answer is "b", with the length of 1.

**Example 3:**
> **Input:** s = "pwwkew"  
> **Output:** 3  
> **Explanation:** The answer is "wke", with the length of 3.  

## Constraints:
- `0 <= s.length <= 5 * 104`
- `s` consists of English letters, digits, symbols and spaces.

~~~~~~~~~~~~~solution~~~~~~~~~~~

const checkLongestString =(str)=>{
  const len = []
  const str2 = []
  let num = 0
  for(let i =0;i<str.length;i++){
    // if unique keep adding,
    // if not exit/ clean the array
    // then return len.length
    if(str2.includes(str[i])){
      len.push(num)
      num = 0
    }else{
      str2.push(str[i])
      num = num+1
    }
  }

  return len
}

console.log(checkLongestString('abcabcbb'))

console.log(checkLongestString('bbbbb'))

console.log(checkLongestString('pwwkew'))
