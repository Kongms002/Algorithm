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

### 너무 좋은 참조글
<a href="https://velog.io/@emplam27/%EC%95%8C%EA%B3%A0%EB%A6%AC%EC%A6%98-%EA%B7%B8%EB%A6%BC%EC%9C%BC%EB%A1%9C-%EC%95%8C%EC%95%84%EB%B3%B4%EB%8A%94-LCS-%EC%95%8C%EA%B3%A0%EB%A6%AC%EC%A6%98-Longest-Common-Substring%EC%99%80-Longest-Common-Subsequence"></a>
