# LCS Algorithm

## 최장 공통 부분수열 (Longest Commom Subsequence)


### Pseudo Code

```
// LCS[i][j] 는 str_a의 i번째까지의 서브 문자열과 str_b의 j번째까지의 서브 문자열을 비교했을 때의 LCS이다.

if i == 0 or j == 0:
  LCS[i][j] = 0;
else if str_a[i] == str_b[j]:
  LCS[i][j] = LCS[i-1][j-1] + 1
else:
  LCS[i][j] = max(LCS[i-1][j], LCS[i][j-1])
```
