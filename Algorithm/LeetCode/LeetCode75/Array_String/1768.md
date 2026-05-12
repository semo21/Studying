# 1768. Merge Strings Alternately

## Difficulty
- Easy

## Point
- 

## Code
```c++
class Solution {
public:
    string mergeAlternately(string word1, string word2) {
        string result;

        int n = max(word1.size(), word2.size());

        for(int i = 0; i < n; ++i){
            if(i < word1.size()) result += word1[i];
            if(i < word2.size()) result += word2[i];
        }
        
        return result;
    }
};
```

### Constraints:
- 1 <= word1.length, word2.length <= 100
- word1 and word2 consist of lowercase English letters.

## Explanation
- 문자열의 길이가 서로 다를 수 있으므로 for 반복문 내부에서 인덱스가 각 문자열 범위 안에 있는지 확인한 후 결과에 문자를 추가